---
title: Как выполнить Использование методов прокрутки содержимого ScrollViewer
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- IScrollInfo interface [WPF]
- scrolling methods [WPF]
- ScrollViewer control [WPF], scrolling methods
ms.assetid: 4708cc65-6510-45f8-82e6-30b0d3e30045
ms.openlocfilehash: 0f2ed1c0ac0d29a47ab98e0329ff161fd54daba6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547044"
---
# <a name="how-to-use-the-content-scrolling-methods-of-scrollviewer"></a>Как выполнить Использование методов прокрутки содержимого ScrollViewer
В этом примере показано использование методов прокрутки <xref:System.Windows.Controls.ScrollViewer> элемент. Эти методы предоставляют добавочные прокрутку содержимого строки или страницы, в <xref:System.Windows.Controls.ScrollViewer>.  
  
## <a name="example"></a>Пример  
 В следующем примере создается <xref:System.Windows.Controls.ScrollViewer> с именем `sv1`, который содержит дочерний <xref:System.Windows.Controls.TextBlock> элемент. Так как <xref:System.Windows.Controls.TextBlock> больше, чем у родительского объекта <xref:System.Windows.Controls.ScrollViewer>, появляются полосы прокрутки, чтобы включить прокрутку. <xref:System.Windows.Controls.Button> элементы, представляющие различные методы прокрутки закрепляются в левой части в отдельном <xref:System.Windows.Controls.StackPanel>. Каждый <xref:System.Windows.Controls.Button> в [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] файл вызывает связанный пользовательский метод, который управляет поведением прокрутки в <xref:System.Windows.Controls.ScrollViewer>.  
  
 [!code-xaml[ScrollViewerMethods#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ScrollViewerMethods/CSharp/Window1.xaml#1)]  
  
 В следующем примере используется <xref:System.Windows.Controls.ScrollViewer.LineUp%2A> и <xref:System.Windows.Controls.ScrollViewer.LineDown%2A> методы.  
  
 [!code-csharp[ScrollViewerMethods#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ScrollViewerMethods/CSharp/Window1.xaml.cs#2)]
 [!code-vb[ScrollViewerMethods#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/ScrollViewerMethods/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Controls.ScrollViewer>
- <xref:System.Windows.Controls.StackPanel>
