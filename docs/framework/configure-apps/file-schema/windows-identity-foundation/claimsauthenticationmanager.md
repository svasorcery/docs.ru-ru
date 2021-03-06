---
title: '&lt;claimsAuthenticationManager&gt;'
ms.date: 03/30/2017
ms.assetid: 6d30a450-6d13-4671-81a8-77e0204500c5
author: BrucePerlerMS
ms.openlocfilehash: b0cee2fedb5f90ca2a1f7e379e199cfee66ee745
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2018
ms.locfileid: "50190974"
---
# <a name="ltclaimsauthenticationmanagergt"></a>&lt;claimsAuthenticationManager&gt;
Регистрирует диспетчер аутентификации утверждений для входящих утверждений.  
  
 \<system.identityModel >  
\<identityConfiguration >  
\<claimsAuthenticationManager >  
  
## <a name="syntax"></a>Синтаксис  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <claimsAuthenticationManager type=xs:string>  
      <optionalConfigurationElements />  
    </claimsAuthenticationManager>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>Атрибуты и элементы  
 В следующих разделах описаны атрибуты, дочерние и родительские элементы.  
  
### <a name="attributes"></a>Атрибуты  
  
|Атрибут|Описание|  
|---------------|-----------------|  
|type|Задает пользовательский тип, производный от <xref:System.Security.Claims.ClaimsAuthenticationManager> класса. Дополнительные сведения о способах указания `type` атрибут, см. в разделе [пользовательский тип ссылки].|  
  
### <a name="child-elements"></a>Дочерние элементы  
 Если не `type` атрибут, или если `type` ссылки на атрибуты <xref:System.Security.Claims.ClaimsAuthenticationManager> класс, `<claimsAuthenticationManager>` элемент выполняет только дочерние элементы; тем не менее, классы, производные от <xref:System.Security.Claims.ClaimsAuthenticationManager> можно определить дочерние элементы конфигурации.  
  
### <a name="parent-elements"></a>Родительские элементы  
  
|Элемент|Описание|  
|-------------|-----------------|  
|[\<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|Указывает параметры уровня службы идентификации.|  
  
## <a name="remarks"></a>Примечания  
 Поведение по умолчанию, предоставляемых <xref:System.Security.Claims.ClaimsAuthenticationManager> класс выводит входящие утверждения. Если не `type` атрибут указан или если `type` атрибут задает <xref:System.Security.Claims.ClaimsAuthenticationManager> класс, `<claimsAuthenticationManager>` элемент выполняет только дочерние элементы. Можно указать `type` атрибут для регистрации типа производным от <xref:System.Security.Claims.ClaimsAuthenticationManager> класса, чтобы реализовать пользовательское поведение. Производные классы могут поддерживает настройку с помощью дочерних элементов `<claimsAuthenticationManager>` элемент путем переопределения <xref:System.Security.Claims.ClaimsAuthenticationManager.LoadCustomConfiguration%2A> метод для обработки этих элементов. В схеме, определенной для дочерних элементов зависит от конструктора класса.  
  
 `<claimsAuthenticationManager>` Наборов элементов <xref:System.IdentityModel.Configuration.IdentityConfiguration.ClaimsAuthenticationManager%2A?displayProperty=nameWithType> свойство.  
  
## <a name="example"></a>Пример  
  
```xml  
<system.identityModel>  
    <identityConfiguration name="MyIdentity">  
      <claimsAuthenticationManager type="MyNamespace.CustomClaimsAuthenticationManager, MyAssembly"/>          
    </identityConfiguration>  
</system.identityModel>  
```
