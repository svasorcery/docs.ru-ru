---
title: '&lt;issuerMetadata&gt; для &lt;issuedTokenParameters&gt;'
ms.date: 03/30/2017
ms.assetid: 1a85ca37-496d-4fa3-8d44-d6c9383d735c
ms.openlocfilehash: 74f5c1275eb7ef6a89d355b5ea279363ae6b8026
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54546206"
---
# <a name="ltissuermetadatagt-of-ltissuedtokenparametersgt"></a>&lt;issuerMetadata&gt; для &lt;issuedTokenParameters&gt;
\<system.serviceModel>  
\<привязки >  
\<customBinding >  
\<Привязка >  
\<Безопасность >  
\<issuedTokenParameters>  
\<issuerMetadata>  
  
## <a name="syntax"></a>Синтаксис  
  
```xml  
<issuerMetaData address="String" />
```  
  
## <a name="attributes-and-elements"></a>Атрибуты и элементы  
 В следующих разделах описаны атрибуты, дочерние и родительские элементы.  
  
### <a name="attributes"></a>Атрибуты  
  
|Атрибут|Описание|  
|---------------|-----------------|  
|address|Обязательный. Строка, задающая адрес конечной точки. Адрес должен быть абсолютным универсальным кодом ресурса (URI). Значение по умолчанию - пустая строка.|  
  
### <a name="child-elements"></a>Дочерние элементы  
  
|Элемент|Описание|  
|-------------|-----------------|  
|[\<заголовки >](../../../../../docs/framework/configure-apps/file-schema/wcf/headers-element.md)|Коллекция заголовков адреса.|  
|[\<удостоверение >](../../../../../docs/framework/configure-apps/file-schema/wcf/identity.md)|Удостоверение, обеспечивающее проверку подлинности конечной точки другими конечными точками, которые обмениваются с ней сообщениями.|  
  
### <a name="parent-elements"></a>Родительские элементы  
  
|Элемент|Описание:|  
|-------------|-----------------|  
|[\<issuedTokenParameters>](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|Задает параметры маркера безопасности, выданного в федеративном сценарии безопасности.|  
  
## <a name="see-also"></a>См. также
- <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>
- <xref:System.ServiceModel.Configuration.IssuedTokenParametersElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [Идентификация и проверка подлинности службы](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)
- [Федерация и выданные маркеры](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [Возможности безопасности при использовании пользовательских привязок](../../../../../docs/framework/wcf/feature-details/security-capabilities-with-custom-bindings.md)
- [Федерация и выданные маркеры](../../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md)
- [Привязки](../../../../../docs/framework/wcf/bindings.md)
- [Расширение привязок](../../../../../docs/framework/wcf/extending/extending-bindings.md)
- [Пользовательские привязки](../../../../../docs/framework/wcf/extending/custom-bindings.md)
- [\<customBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/custombinding.md)
- [Практическое руководство. Создание пользовательской привязки с использованием элемента SecurityBindingElement](../../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
- [Безопасность пользовательской привязки](../../../../../docs/framework/wcf/samples/custom-binding-security.md)
