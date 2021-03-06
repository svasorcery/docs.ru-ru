---
title: Как выполнить Привязка к веб-службе
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- binding data [WPF], Web service
- Web service binding [WPF]
- data binding [WPF], Web service
ms.assetid: 77e2d373-69ba-4cbd-b6f5-2c83c38fc98b
ms.openlocfilehash: 0a738d52cfb01fff1cb21d0e6ebb8f1b7b28d57f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695771"
---
# <a name="how-to-bind-to-a-web-service"></a>Как выполнить Привязка к веб-службе
В этом примере показано, как выполнить привязку для объектов, возвращенных вызовов метода веб-службы.  
  
## <a name="example"></a>Пример  
 В этом примере используется [службы содержимого MSDN или TechNet Publishing System (MTPS)](https://go.microsoft.com/fwlink/?LinkId=95677) для получения списка языков, поддерживаемых указанного документа.  
  
 Перед вызовом метода веб-службы, необходимо создать ссылку на него. Для создания веб-ссылки MTPS службе, используя [!INCLUDE[TLA#tla_visualstu](../../../../includes/tlasharptla-visualstu-md.md)], выполните следующие действия:  
  
1.  Откройте проект в [!INCLUDE[TLA2#tla_visualstu](../../../../includes/tla2sharptla-visualstu-md.md)].  
  
2.  Из **проекта** меню, щелкните **Add Web Reference**.  
  
3.  В диалоговом окне задайте **URL-адрес** для [ http://services.msdn.microsoft.com/contentservices/contentservice.asmx?wsdl ](https://services.msdn.microsoft.com/contentservices/contentservice.asmx?wsdl).  
  
4.  Нажмите клавишу **Go** и затем **добавьте ссылку на**.  
  
 Затем вызовите метод веб-службы и задайте <xref:System.Windows.FrameworkElement.DataContext%2A> соответствующий элемент управления или окно, чтобы возвращенный объект. **GetContent** метод службы MTPS принимает ссылку на **getContentRequest** объекта. Таким образом в следующем примере сначала задается объект запроса:  
  
 [!code-csharp[BindToWebService#Namespace](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindToWebService/CSharp/Window1.xaml.cs#namespace)]
 [!code-vb[BindToWebService#Namespace](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BindToWebService/VisualBasic/Window1.xaml.vb#namespace)]  
[!code-csharp[BindToWebService#WebServiceCall](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindToWebService/CSharp/Window1.xaml.cs#webservicecall)]
[!code-vb[BindToWebService#WebServiceCall](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/BindToWebService/VisualBasic/Window1.xaml.vb#webservicecall)]  
  
 После <xref:System.Windows.FrameworkElement.DataContext%2A> задано значение, можно создать привязку к свойствам объекта, <xref:System.Windows.FrameworkElement.DataContext%2A> было присвоено. В этом примере <xref:System.Windows.FrameworkElement.DataContext%2A> присваивается **getContentResponse** объект, возвращаемый **GetContent** метод. В следующем примере <xref:System.Windows.Controls.ItemsControl> привязывается к и отображает **языкового стандарта** значения **availableVersionsAndLocales** из **getContentResponse**.  
  
 [!code-xaml[BindToWebService#Binding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/BindToWebService/CSharp/Window1.xaml#binding)]  
  
 Сведения о структуре **getContentResponse**, см. в разделе [документации службы содержимого](https://services.msdn.microsoft.com/ContentServices/ContentService.asmx).  
  
## <a name="see-also"></a>См. также
- [Общие сведения о привязке данных](../../../../docs/framework/wpf/data/data-binding-overview.md)
- [Общие сведения об источниках привязки](../../../../docs/framework/wpf/data/binding-sources-overview.md)
- [Обеспечение доступности данных для привязки в XAML](../../../../docs/framework/wpf/data/how-to-make-data-available-for-binding-in-xaml.md)
