---
title: Как выполнить Открыть диалоговое окно
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- opening dialog boxes [WPF]
- dialog boxes [WPF], opening
ms.assetid: 6b1557d2-da98-4ef4-9f68-4089f04ab9ea
ms.openlocfilehash: 0ed41d212eee74d0c3eed1d3341d64a6abc876a5
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54638149"
---
# <a name="how-to-open-a-dialog-box"></a>Как выполнить Открыть диалоговое окно
В этом примере показано, как открыть диалоговое окно.  
  
## <a name="example"></a>Пример  
 Диалоговое окно является окном, которое открывается путем создания экземпляра <xref:System.Windows.Window> и вызов <xref:System.Windows.Window.ShowDialog%2A> метод. <xref:System.Windows.Window.ShowDialog%2A> Открывает окно и не отвечала до новое диалоговое окно было закрыто. Этот тип окна называется также *модального* окно и ограничивает ввод данных пользователем.  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewdialogboxcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewdialogboxcode)]  
  
## <a name="net-framework-security"></a>Безопасность платформы .NET Framework  
 Вызов <xref:System.Windows.Window.ShowDialog%2A> требуется разрешение на использование все окна и события пользовательского ввода без ограничений.  
  
## <a name="see-also"></a>См. также
- [Возвращение результата диалогового окна](../../../../docs/framework/wpf/app-development/how-to-return-a-dialog-box-result.md)
