---
title: Как выполнить Набор толщины и выравнивания пера
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pens [Windows Forms], setting width
- pens [Windows Forms], setting alignment
ms.assetid: a202af36-4d31-4401-a126-b232f51db581
ms.openlocfilehash: d1a465fb7c1cd6d4064a077e592daefebf590714
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54564829"
---
# <a name="how-to-set-pen-width-and-alignment"></a>Как выполнить Набор толщины и выравнивания пера
При создании <xref:System.Drawing.Pen>, указать толщину пера в качестве одного из аргументов конструктора. Можно также изменить ширину пера <xref:System.Drawing.Pen.Width%2A> свойство <xref:System.Drawing.Pen> класса.  
  
 Теоретической линии имеет ширину 0. При рисовании линии, одну точку, пиксели центрируются по теоретической линии. Если нарисовать линию, является более чем одному пикселю, пиксели либо центрируются по теоретической линии появятся или к одной стороне от теоретической линии. Можно задать свойство выравнивания из <xref:System.Drawing.Pen> чтобы определить положение точек, рисуемых при помощи этого пера по отношению к теоретической линии.  
  
 Значения <xref:System.Drawing.Drawing2D.PenAlignment.Center>, <xref:System.Drawing.Drawing2D.PenAlignment.Outset>, и <xref:System.Drawing.Drawing2D.PenAlignment.Inset> , отображаемые в следующих примерах кода являются членами <xref:System.Drawing.Drawing2D.PenAlignment> перечисления.  
  
 В следующем примере кода рисует линию дважды: один раз черным пером толщиной в 1 и один раз с помощью зеленого пера шириной 10.  
  
### <a name="to-vary-the-width-of-a-pen"></a>Для изменения ширины пера  
  
-   Установите для параметра <xref:System.Drawing.Pen.Alignment%2A> свойства <xref:System.Drawing.Drawing2D.PenAlignment.Center> (по умолчанию) будет что рисование зеленым пером пикселей по теоретической линии. Ниже показан итоговый строки.  
  
     ![Перья](../../../../docs/framework/winforms/advanced/media/pens1a.gif "pens1A")  
  
     В следующем примере рисуется прямоугольник дважды: один раз черным пером толщиной в 1 и один раз с помощью зеленого пера шириной 10.  
  
     [!code-csharp[System.Drawing.UsingAPen#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#41)]
     [!code-vb[System.Drawing.UsingAPen#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#41)]  
  
### <a name="to-change-the-alignment-of-a-pen"></a>Изменение выравнивания пера  
  
-   Установите для параметра <xref:System.Drawing.Pen.Alignment%2A> свойства <xref:System.Drawing.Drawing2D.PenAlignment.Center> будет что рисование зеленым пером пикселей по границ прямоугольника.  
  
     На следующем рисунке показан полученный прямоугольник.  
  
     ![Перья](../../../../docs/framework/winforms/advanced/media/pens2.gif "pens2")  
  
     [!code-csharp[System.Drawing.UsingAPen#42](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#42)]
     [!code-vb[System.Drawing.UsingAPen#42](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#42)]  
  
### <a name="to-create-an-inset-pen"></a>Для создания вложенного пера  
  
-   Измените выравнивание зеленого пера, изменив третья инструкция в предыдущем примере кода следующим образом:  
  
     [!code-csharp[System.Drawing.UsingAPen#43](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#43)]
     [!code-vb[System.Drawing.UsingAPen#43](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#43)]  
  
     Теперь пикселов в ширину зеленая линия отображаются внутри прямоугольника, как показано на следующем рисунке.  
  
     ![Перья](../../../../docs/framework/winforms/advanced/media/pens3.gif "pens3")  
  
## <a name="see-also"></a>См. также
- [Рисование линий и фигур с помощью пера](../../../../docs/framework/winforms/advanced/using-a-pen-to-draw-lines-and-shapes.md)
- [Объекты Graphics и Drawing в Windows Forms](../../../../docs/framework/winforms/advanced/graphics-and-drawing-in-windows-forms.md)
