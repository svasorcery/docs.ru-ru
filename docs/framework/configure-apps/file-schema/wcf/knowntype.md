---
title: '&lt;knownType&gt;'
ms.date: 03/30/2017
ms.assetid: ee2b7be3-7148-4a3a-b861-48e7330615e5
ms.openlocfilehash: cb36a0d1d1ceb13a6db902904783ee15b14e673b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54541070"
---
# <a name="ltknowntypegt"></a>&lt;knownType&gt;
Задает тип, используемый <xref:System.Runtime.Serialization.DataContractSerializer> во время десериализации. Элемент задает «известный тип», возвращаемый полем или свойством «объявленного типа». Дополнительные сведения см. в разделе [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md).  
  
 \<system.runtime.serialization>  
\<dataContractSerializer >  
\<declaredTypes > элемент  
\<Добавить > из \<declaredTypes >  
\<knownType > элемент  
  
## <a name="syntax"></a>Синтаксис  
  
```xml  
<knownType type="String">
  <parameter index="Integer"
             type="String" />
</knownType>
```  
  
## <a name="type"></a>Тип  
 `string`  
  
## <a name="attributes-and-elements"></a>Атрибуты и элементы  
 В следующих разделах описаны атрибуты, дочерние и родительские элементы.  
  
### <a name="attributes"></a>Атрибуты  
  
|Атрибут|Описание|  
|---------------|-----------------|  
|тип|Задает тип (в том числе пространство имен), имя сборки, версию, язык и региональные параметры и маркер открытого ключа.|  
  
### <a name="child-elements"></a>Дочерние элементы  
  
|Элемент|Описание:|  
|-------------|-----------------|  
|[\<Параметр >](../../../../../docs/framework/configure-apps/file-schema/wcf/parameter.md)|Задает индекс параметра в том случае, если объявленный тип является универсальным типом.|  
  
### <a name="parent-elements"></a>Родительские элементы  
  
|Элемент|Описание:|  
|-------------|-----------------|  
|[\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)|Добавляет объявленный тип в коллекцию объявленных типов.|  
  
## <a name="remarks"></a>Примечания  
 Дополнительные сведения об известных типах см. в разделе [Data Contract Known Types](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md) и <xref:System.Runtime.Serialization.DataContractSerializer>.  
  
 См. в разделе [ \<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md) пример использования этого элемента.  
  
## <a name="example"></a>Пример  
  
```xml  
<add type="MyCompany.Library.Shape,
           MyAssembly, Version=2.0.0.0, Culture=neutral,
           PublicKeyToken=XXXXXX, processorArchitecture=MSIL">
  <knownType type="MyCompany.Library.Circle,
                   MyAssembly, Version=2.0.0.0, Culture=neutral,
                   PublicKeyToken=XXXXXX,
                   processorArchitecture=MSIL"/>
</add>
```  
  
## <a name="see-also"></a>См. также
- <xref:System.Runtime.Serialization.DataContractSerializer>
- [Известные типы контрактов данных](../../../../../docs/framework/wcf/feature-details/data-contract-known-types.md)
- [\<dataContractSerializer >](../../../../../docs/framework/configure-apps/file-schema/wcf/datacontractserializer-element.md)
- [\<add>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-declaredtypes-element.md)
