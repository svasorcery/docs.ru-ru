---
title: Как выполнить Создание SecurityBindingElement для заданного режима проверки подлинности
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: a7c7747a-5b8c-463f-8493-7266dac75066
ms.openlocfilehash: 62006397db3155d26a2c7bd327251b870a3b8460
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54619932"
---
# <a name="how-to-create-a-securitybindingelement-for-a-specified-authentication-mode"></a>Как выполнить Создание SecurityBindingElement для заданного режима проверки подлинности
Windows Communication Foundation (WCF) предоставляет несколько режимов, по которым клиенты и службы проверяют подлинность друг друга. Для этих режимов проверки подлинности можно создать привязки безопасности с помощью статических методов класса <xref:System.ServiceModel.Channels.SecurityBindingElement> или с помощью конфигурации, как показано в следующем примере кода.  
  
 Дополнительные сведения о 18 режимов проверки подлинности, см. в разделе [режимы проверки подлинности SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md).  
  
## <a name="example"></a>Пример  
 В следующем примере кода показаны методы создания привязок для различных методов проверки подлинности.  
  
> [!NOTE]
>  После создания объекта <xref:System.ServiceModel.Channels.SecurityBindingElement> некоторые свойства являются неизменяемыми, такие как <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters.KeyType%2A> и <xref:System.ServiceModel.Channels.SecurityBindingElement.MessageSecurityVersion%2A>. Вызов `set` для этих свойств не изменяет их.  
  
 [!code-csharp[c_CustomBindingsAuthMode#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombindingsauthmode/cs/source.cs#2)]
 [!code-vb[c_CustomBindingsAuthMode#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_custombindingsauthmode/vb/source.vb#2)]  
  
## <a name="see-also"></a>См. также
- [Режимы проверки подлинности SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md)
- [Практическое руководство. Создание пользовательской привязки с использованием элемента SecurityBindingElement](../../../../docs/framework/wcf/feature-details/how-to-create-a-custom-binding-using-the-securitybindingelement.md)
