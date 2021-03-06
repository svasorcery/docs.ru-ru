---
title: Трассировка данных в ADO.NET
ms.date: 03/30/2017
ms.assetid: a6a752a5-d2a9-4335-a382-b58690ccb79f
ms.openlocfilehash: ac9e290d4c9209cbf8ccf5eb3acdeceb68f9021b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54721933"
---
# <a name="data-tracing-in-adonet"></a>Трассировка данных в ADO.NET
ADO.NET появились новые встроенные функции трассировки данных, поддерживаемые поставщиками данных .NET для SQL Server, Oracle, OLE DB и ODBC, а также ADO.NET <xref:System.Data.DataSet>, а также сетевые протоколы SQL Server.  
  
 Трассировка вызовов API-интерфейсов для доступа к данным может помочь в выявлении следующих проблем:  
  
-   несоответствие схемы между клиентской программой и базой данных;  
  
-   недоступность базы данных или проблемы с сетевой библиотекой;  
  
-   неверный SQL-код, фиксированный или сформированный приложением;  
  
-   неверная программная логика;  
  
-   проблемы, возникающие вследствие взаимодействия нескольких компонентов ADO.NET или компонентов ADO.NET и собственных компонентов.  
  
 Трассировка является расширяемой для поддержки разных методов трассировки, поэтому разработчик может отслеживать проблемы на любом уровне стека приложений. Хотя трассировка не является возможностью только ADO.NET, поставщики Майкрософт пользуются преимуществами обобщенных API трассировки и инструментария.  
  
 Дополнительные сведения об установке и настройке управляемой трассировки в ADO.NET см. в разделе [трассировка доступа к данным](https://msdn.microsoft.com/library/hh880086.aspx).  
  
## <a name="accessing-diagnostic-information-in-the-extended-events-log"></a>Доступ к диагностической информации в расширенном журнале событий  
 В [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] поставщик данных для SQL Server, доступ к данным трассировки ([трассировка доступа к данным](https://msdn.microsoft.com/library/hh880086.aspx)) был обновлен для упрощения проще коррелировать события клиента с диагностической информацией — ошибками соединения, из сервера кольцевой буфер и приложение производительности сведения о подключении в журнале расширенных событий. Дополнительные сведения о чтении журнала расширенных событий см. в разделе [данные сеанса событий представления](https://msdn.microsoft.com/library/hh710068\(SQL.110\).aspx).  
  
 Для операций соединения ADO.NET передает идентификатор соединения клиента. Если подключение отсутствует, можно воспользоваться кольцевого буфера ([Устранение неполадок подключения в SQL Server 2008 с помощью кольцевого буфера](https://go.microsoft.com/fwlink/?LinkId=207752)) и найти `ClientConnectionID` поле и получить диагностическую информацию Ошибка соединения. Идентификаторы соединения клиента регистрируются в кольцевом буфере только при возникновении ошибки. (Если установление соединения завершилось неудачно перед отправкой пакета предварительного согласования, то идентификатор соединения клиента не будет сформирован.) Идентификатор соединения клиента - это 16-байтное значение идентификатора GUID. Можно также найти идентификатор соединения клиента в расширенном выводе целевых событий, если целевое действие `client_connection_id` добавляется в события в расширенном сеансе событий. Если необходима дополнительная помощь по устранению неполадок драйвера клиента, можно включить трассировку для доступа к данным, повторно запустить команду соединения и проверить поле `ClientConnectionID` в трассировке доступа к данным.  
  
 Можно получить идентификатор соединения клиента программно через свойство `SqlConnection.ClientConnectionID`.  
  
 Идентификатор `ClientConnectionID` доступен для объекта <xref:System.Data.SqlClient.SqlConnection>, который успешно устанавливает соединение. Если попытка соединения завершилась ошибкой, то `ClientConnectionID` можно попробовать получить через `SqlException.ToString`.  
  
 ADO.NET также отправляет идентификатор действия, определенный для потока. Идентификатор действия захватывается в сеансах расширенных событий, если сеансы запускаются с включенным параметром TRACK_CAUSAILITY. Для устранения проблем производительности с активным соединением можно получить идентификатор действия из трассировки клиента для доступа к данным (поле `ActivityID`), а затем найти идентификатор действия в выходных данных расширенных событий. Идентификатор действия в расширенных событиях представляет собой 16-байтовый GUID (не совпадает с идентификатором GUID для идентификатора соединения клиента) с добавленным к нему четырехбайтовым порядковым номером. Порядковый номер представляет собой порядковый номер запроса в потоке и указывает относительное упорядочение инструкций пакета RPC для потока. Идентификатор `ActivityID` в настоящее время (необязательно) отправляется для инструкций пакета SQL и запросов RPC, если включена трассировка доступа к данным и включен 18-й бит в слове настройки трассировки доступа к данным.  
  
 Далее приведен образец, в котором используется [!INCLUDE[tsql](../../../../includes/tsql-md.md)] для запуска расширенного сеанса событий, который будет сохранен в кольцевом буфере и будет регистрировать идентификатор действия, отправленный с клиента в операциях RPC и пакета.  
  
```  
create event session MySession on server   
add event connectivity_ring_buffer_recorded,   
add event sql_statement_starting (action (client_connection_id)),   
add event sql_statement_completed (action (client_connection_id)),   
add event rpc_starting (action (client_connection_id)),   
add event rpc_completed (action (client_connection_id))  
add target ring_buffer with (track_causality=on)  
```  
  
## <a name="see-also"></a>См. также
- [Трассировка сети в .NET Framework](../../../../docs/framework/network-programming/network-tracing.md)
- [Трассировка и инструментирование приложений](../../../../docs/framework/debug-trace-profile/tracing-and-instrumenting-applications.md)
- [Центр разработчиков наборов данных и управляемых поставщиков ADO.NET](https://go.microsoft.com/fwlink/?LinkId=217917)
