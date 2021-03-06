---
title: '&lt;comContracts&gt;'
ms.date: 03/30/2017
ms.assetid: 42e74148-223d-4888-a8ed-1d928527eb09
ms.openlocfilehash: 2374155011b98822d47998cd1e4b8935db234752
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54731534"
---
# <a name="ltcomcontractsgt"></a>&lt;comContracts&gt;
Раздел конфигурации `comContracts` содержит элементы, которые позволяют задавать различные свойства контракта службы интеграции COM+.  
  
## <a name="specifying-namespace-and-contract"></a>Задание пространства имен и контракта  
 Контракты службы интеграции COM +, в настоящее время ограничены `http://tempuri.org` пространства имен, а имя контракта является производным от поддерживающего COM-интерфейса. Однако можно указать альтернативы, используя раздел `comContracts` в файле конфигурации.  
  
 Например, для указания пространства имен, имени контракта службы и параметра для принудительного использования сеансовых привязок можно использовать следующую конфигурацию.  
  
```xml  
<comContracts>
  <comContract contract="{5163B1E7-F0CF-4B6A-9A02-4AB654F34284}"
               namespace="http://tempuri.org/5163B1E7-F0CF-4B6A-9A02-4AB654F34284"
               name="_Broker"
               requireSession="true">
  </comContract>
</comContracts>
```  
  
 После инициализации службы указанные пространства имен и имена контрактов применяются к созданным описаниям служб.  
  
 Если раздел пуст, при инициализации службы применяется пространство имен по умолчанию и имя контракта, взятое из идентификатора поддерживающего COM-интерфейса.  
  
 Кроме того, можно использовать [ \<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md) элемент для задания методов COM +, которые предоставляются при предоставлении интерфейса компонента COM + предоставляется как веб-службы. Можно также использовать [ \<persistableTypes >](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md) для задания неизменных типов, используемых в интеграции. Наконец, вы можете использовать [ \<userDefinedType >](../../../../../docs/framework/configure-apps/file-schema/wcf/userdefinedtype.md) элемент для включения пользовательских типов (UDT), должны быть включены в контракте службы.  
  
## <a name="see-also"></a>См. также
- <xref:System.ServiceModel.Configuration.ComContractElementCollection>
- <xref:System.ServiceModel.Configuration.ComContractElement>
- [\<exposedMethod >](../../../../../docs/framework/configure-apps/file-schema/wcf/exposedmethod.md)
- [\<persistableTypes >](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)
- [\<userDefinedType >](../../../../../docs/framework/configure-apps/file-schema/wcf/userdefinedtype.md)
- [\<comContract >](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontract.md)
- [Интеграция с приложениями COM+](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
- [Практическое руководство. Настройка параметров службы COM +](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
