---
title: Элемент &lt;certificate&gt;
ms.date: 03/30/2017
ms.assetid: 9b3d9233-ef35-477a-bf5d-efd1e80a52f4
ms.openlocfilehash: d1449cc6c40ae16190bacf378df3bd60c49d060c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54538327"
---
# <a name="ltcertificategt-element"></a>Элемент &lt;certificate&gt;
Задает сертификат X.509, используемый для подписи и шифрования сообщений для клиентов одноранговых сетей.  
  
 \<system.ServiceModel>  
\<варианты поведения >  
\<endpointBehaviors>  
\<поведение >  
\<clientCredentials>  
\<Одноранговый >  
\<сертификат >  
  
## <a name="syntax"></a>Синтаксис  
  
```xml  
<certificate findValue="String"
             storeLocation="LocalMachine/CurrentUser"
             storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"
             X509FindType="FindByThumbPrint/FindBySubjectName/FindBySubjectDistinguishedName/FindByIssuerName/FindByIssuerDistinguishedName/FindBySerialNumber/FindByTimeValid/FindByTimeNotYetValid/FindByTemplateName/FindByApplicationPolicy/FindByCertificatePolicy/FindByExtension/FindByKeyUsage/FindBySubjectKeyIdentifier" />
```  
  
## <a name="attributes-and-elements"></a>Атрибуты и элементы  
 В следующих разделах описаны атрибуты, дочерние и родительские элементы.  
  
### <a name="attributes"></a>Атрибуты  
  
|Атрибут|Описание|  
|---------------|-----------------|  
|`findValue`|Строка, содержащая значение для поиска в хранилище сертификатов X.509. Тип, указанный в этом атрибуте, должен отвечать требованиям заданного значения `x509FindType`. Значение по умолчанию - пустая строка.|  
|`storeLocation`|Задает расположение хранилища сертификатов Х.509, которое клиент может использовать для проверки сертификата однорангового узла. Допустимы следующие значения:<br /><br /> -LocalMachine: хранилище сертификатов, назначенное локальному компьютеру.<br />-CurrentUser: хранилище сертификатов, назначенное текущему пользователю.<br /><br /> Значение по умолчанию - LocalMachine.|  
|`storeName`|Задает имя открываемого хранилища сертификатов X.509. Допустимы следующие значения:<br /><br /> -AddressBook: Хранилище сертификатов для других пользователей.<br />-AuthRoot: Хранилище сертификатов для сторонних сертификации (ЦС).<br />-CertificateAuthority: Хранилище сертификатов для промежуточных центров сертификации (ЦС).<br />-Запрещается использовать следующее: Хранилище сертификатов для отозванных сертификатов.<br />— My: Хранилище сертификатов для личных сертификатов.<br />-Root: Хранилище сертификатов для доверенных корневых центров сертификации (ЦС).<br />-TrustedPeople: Хранилище сертификатов для непосредственно доверенных лиц и ресурсов.<br />-TrustedPublisher: Хранилище сертификатов для непосредственно доверенных издателей.<br /><br /> Значение по умолчанию - My.|  
|`X509FindType`|Определяет тип поиска сертификата X.509. Допустимы следующие значения:<br /><br /> -FindByThumbPrint<br />-FindBySubjectName<br />-FindBySubjectDistinguishedName<br />-FindByIssuerName<br />-FindByIssuerDistinguishedName<br />-FindBySerialNumber<br />-FindByTimeValid<br />-FindByTimeNotYetValid<br />-FindByTemplateName<br />-FindByApplicationPolicy<br />-FindByCertificatePolicy<br />-FindByExtension<br />-FindByKeyUsage<br />-FindBySubjectKeyIdentifier<br /><br /> Тип, указанный в атрибуте `findValue`, должен отвечать требованиям заданного значения `X509FindType`.<br /><br /> Значение по умолчанию - FindBySubjectDistinguishedName.|  
  
### <a name="child-elements"></a>Дочерние элементы  
 Отсутствует.  
  
### <a name="parent-elements"></a>Родительские элементы  
  
|Элемент|Описание:|  
|-------------|-----------------|  
|[\<Одноранговый >](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-clientcredentials-element.md)|Задает учетные данные, используемые при проверке подлинности одноранговых клиентов.|  
  
## <a name="remarks"></a>Примечания  
 Этот элемент конфигурации содержит экземпляр X509Certificate2, используемый при проверке подлинности соседей в сетке узлов.  
  
 Дополнительные сведения о программировании peer-to-peer см. в разделе [сети Peer-to-Peer](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md).  
  
## <a name="example"></a>Пример  
 В следующем примере кода показывается, как найти сертификат, используемый в сценарии с одноранговой сетью.  
  
```xml  
<behaviors>
  <endpointBehaviors>
    <behavior name="MyEndpointBehavior">
      <clientCredentials>
        <peer>
          <certificate findValue="www.contoso.com"
                       storeLocation="LocalMachine"
                       x509FindType="FindByIssuerName" />
        </peer>
      </clientCredentials>
    </behavior>
  </endpointBehaviors>
</behaviors>
```  
  
## <a name="see-also"></a>См. также
- <xref:System.ServiceModel.Configuration.PeerCredentialElement>
- <xref:System.ServiceModel.Configuration.PeerCredentialElement.Certificate%2A>
- <xref:System.ServiceModel.Configuration.X509PeerCertificateElement>
- <xref:System.ServiceModel.Security.PeerCredential.Certificate%2A>
- [Работа с сертификатами](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)
- [Одноранговая сеть](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)
- [Проверка подлинности сообщений однорангового канала](https://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)
- [Нестандартной проверки подлинности одноранговых каналов](https://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)
- [Защита приложений одноранговых каналов](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
