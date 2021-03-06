---
title: Как выполнить Отображение элементов с использованием визуального стиля
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- visual themes [Windows Forms], applying to elements of Windows Forms applications
- professional appearance [Windows Forms], applying to elements of Windows Forms applications
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: a207781b-1baa-4ce9-b788-1e951bd4b5df
ms.openlocfilehash: 42e165d74628450adb8641bddcc7e8850b2af0a8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54526864"
---
# <a name="how-to-render-a-visual-style-element"></a>Как выполнить Отображение элементов с использованием визуального стиля
<xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Пространство имен предоставляет <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> элементы пользовательского интерфейса, поддерживаемого стилями оформления интерфейса объекты, представляющие пользователя Windows. В этом разделе демонстрируется использование <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> класс для подготовки к просмотру <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> , представляющий **Выход** и **завершение работы** кнопок, меню «Пуск».  
  
### <a name="to-render-a-visual-style-element"></a>Для подготовки к просмотру элемента визуального стиля  
  
1.  Создание <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> и присвойте ему значение для рисования элемента. Обратите внимание на использование <xref:System.Windows.Forms.Application.RenderWithVisualStyles%2A?displayProperty=nameWithType> свойство и <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.IsElementDefined%2A?displayProperty=nameWithType> метод; <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.%23ctor%2A> конструктор выдаст исключение, если стили оформления отключены или элемент не определен.  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#4)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#4)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#4)]  
  
2.  Вызовите <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.DrawBackground%2A> способ визуализации элемента, который <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> в данный момент представляет.  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#6)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#6)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#6)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   Пользовательские элементы управления, производные от <xref:System.Windows.Forms.Control> класса.  
  
-   Объект <xref:System.Windows.Forms.Form> , на котором размещается пользовательский элемент управления.  
  
-   Ссылки на <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, <xref:System.Windows.Forms?displayProperty=nameWithType>, и <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> пространства имен.  
  
## <a name="see-also"></a>См. также
- [Отрисовка элементов управления с применением визуальных стилей](../../../../docs/framework/winforms/controls/rendering-controls-with-visual-styles.md)
