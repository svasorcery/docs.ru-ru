---
title: Создание таблицы данных
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: eecf9d78-60e3-4fdc-8de0-e56c13a89414
ms.openlocfilehash: f40a04156bee5ceee7490cf7bd941dc11a99b880
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54608323"
---
# <a name="creating-a-datatable"></a>Создание таблицы данных
Объект <xref:System.Data.DataTable>, который представляет одну таблицу находящихся в памяти реляционных данных, может создаваться и использоваться независимо или использоваться другими объектами .NET Framework, чаще всего как член <xref:System.Data.DataSet>.  
  
 Можно создать **DataTable** объекта, используя соответствующую **DataTable** конструктор. Вы можете добавить его **набора данных** с помощью **добавить** метод, чтобы добавить его **DataTable** объекта **таблиц** коллекции.  
  
 Вы также можете создать **DataTable** объектов в рамках **набора данных** с помощью **заполнения** или **FillSchema** методы  **DataAdapter** объекта, или из предварительно определенных или выводимым XML-схемы с помощью **ReadXml**, **ReadXmlSchema**, или **InferXmlSchema** методы **набора данных**. Обратите внимание, что после добавления **DataTable** членом **таблиц** коллекцию из одного **набора данных**, не может добавить его в коллекцию таблиц любые другие **Набора данных**.  
  
 При первом создании **DataTable**, он не имеет схемы (т. е. структуры). Чтобы определить схему таблицы, необходимо создать и добавить <xref:System.Data.DataColumn> объектов **столбцы** коллекции таблицы. Можно также определить столбец первичного ключа для таблицы и создать и добавить **ограничение** объектов **ограничения** коллекции таблицы. После определения схемы для **DataTable**, можно добавлять строки данных в таблицу, добавив **DataRow** объектов **строк** коллекции таблицы.  
  
 Вы не обязаны предоставить значение для <xref:System.Data.DataTable.TableName%2A> свойства при создании **DataTable**; можно указать свойство в другое время, или оставить его пустым. Тем не менее, при добавлении таблицы без **TableName** значение **набора данных**, будет присвоено имя по умолчанию — таблица*N*, начиная с «Table» для Table0.  
  
> [!NOTE]
>  Мы рекомендуем избегать» таблицы*N*"соглашение об именовании, при указании **TableName** , поскольку к. предоставляемое имя может конфликтовать с существующим именем таблицы по умолчанию в значение **набора данных** . Если указанное имя уже существует, вызывается исключение.  
  
 В следующем примере создается экземпляр **DataTable** , которому присваивается имя «Customers».  
  
```vb  
Dim workTable as DataTable = New DataTable("Customers")  
```  
  
```csharp  
DataTable workTable = new DataTable("Customers");  
```  
  
 В следующем примере создается экземпляр **DataTable** путем добавления его в **таблиц** коллекцию **набора данных**.  
  
```vb  
Dim customers As DataSet = New DataSet  
Dim customersTable As DataTable = _  
   customers.Tables.Add("CustomersTable")  
```  
  
```csharp  
DataSet customers = new DataSet();  
DataTable customersTable = customers.Tables.Add("CustomersTable");  
```  
  
## <a name="see-also"></a>См. также
- <xref:System.Data.DataTable>
- <xref:System.Data.DataTableCollection>
- [DataTables](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/datatables.md)
- [Заполнение набора данных с помощью адаптера данных DataAdapter](../../../../../docs/framework/data/adonet/populating-a-dataset-from-a-dataadapter.md)
- [Загрузка DataSet из XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-a-dataset-from-xml.md)
- [Загрузка сведений о схеме DataSet из XML](../../../../../docs/framework/data/adonet/dataset-datatable-dataview/loading-dataset-schema-information-from-xml.md)
- [Центр разработчиков наборов данных и управляемых поставщиков ADO.NET](https://go.microsoft.com/fwlink/?LinkId=217917)
