---
title: Как выполнить Вращение объекта
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], rotating objects [WPF]
- rotating objects [WPF]
ms.assetid: ee3466cd-e66f-4e8f-8a5a-71d77bc1e390
ms.openlocfilehash: b44ce71f91962806704eb05a9cbec53638856b3e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54525434"
---
# <a name="how-to-rotate-an-object"></a>Как выполнить Вращение объекта
В данном примере показано, как можно вращать объект. В примере сначала создается <xref:System.Windows.Media.RotateTransform> и затем задает его <xref:System.Windows.Media.RotateTransform.Angle%2A> в градусах.  
  
 В следующем примере Ломаная <xref:System.Windows.Shapes.Polyline> объекта 45 градусов относительно его верхнего левого угла.  
  
## <a name="example"></a>Пример  
 [!code-xaml[Transforms_snip#RotatePolylineAboutTopLeft](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineabouttopleft)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineabouttopleft)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutTopLeft](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineabouttopleft)]  
  
 <xref:System.Windows.Media.RotateTransform.CenterX%2A> И <xref:System.Windows.Media.RotateTransform.CenterY%2A> свойства <xref:System.Windows.Media.RotateTransform> укажите точку, вокруг которой будет поворачиваться объект. Это центральная точка выражается в пространстве координат преобразуемого элемента. По умолчанию поворот выполняется относительно точки (0,0), которая является верхним левым углом объекта для преобразования.  
  
 В следующем примере Ломаная <xref:System.Windows.Shapes.Polyline> объекта по часовой стрелке на 45 градусов относительно точки (25,50).  
  
 [!code-xaml[Transforms_snip#RotatePolylineAboutCenter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_snip/CS/RotateTransformExample.xaml#rotatepolylineaboutcenter)]  
  
 [!code-csharp[Transforms_Procedural_snip#RotatePolylineAboutCenter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Transforms_Procedural_snip/CSharp/RotateTransformExample.cs#rotatepolylineaboutcenter)]
 [!code-vb[Transforms_Procedural_snip#RotatePolylineAboutCenter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/Transforms_Procedural_snip/VisualBasic/RotateTransformExample.vb#rotatepolylineaboutcenter)]  
  
 На следующем рисунке показан результат применения <xref:System.Windows.Media.Transform> к двум объектам.  
  
 ![Поворот на 45 градусов вокруг различных точек](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-rotatetransform45degrees.gif "wcpsdk_graphicsmm_rotatetransform45degrees")  
Два объекта, повернутые на 45 градусов, с разными центрами вращения  
  
 <xref:System.Windows.Shapes.Polyline> В предыдущих примерах является <xref:System.Windows.UIElement>. При применении <xref:System.Windows.Media.Transform> для <xref:System.Windows.UIElement.RenderTransform%2A> свойство <xref:System.Windows.UIElement>, можно использовать <xref:System.Windows.UIElement.RenderTransformOrigin%2A> свойство для указания источника для каждого <xref:System.Windows.Media.Transform> , примененные к элементу. Так как <xref:System.Windows.UIElement.RenderTransformOrigin%2A> свойство использует относительные координаты, преобразование можно применять к центру элемента, даже если вы не знаете его размер. Дополнительные сведения и пример см. в разделе [задание источника преобразования с помощью относительных значений](../../../../docs/framework/wpf/graphics-multimedia/how-to-specify-the-origin-of-a-transform-by-using-relative-values.md).  
  
 Полный пример см. в разделе [Примеры двумерных преобразований](https://go.microsoft.com/fwlink/?LinkID=158252).  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Media.Transform>
- [Общие сведения о классах Transform](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [Разделы практического руководства](../../../../docs/framework/wpf/graphics-multimedia/transformations-how-to-topics.md)
