---
title: Как выполнить Установка длительности анимации
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], duration
- Timelines [WPF], description
- duration of animations [WPF]
ms.assetid: 155034ef-7d00-4416-a73c-b1713992d2eb
ms.openlocfilehash: 7a2edbd953f648d5555e5dc50469211a6da066de
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54497935"
---
# <a name="how-to-set-a-duration-for-an-animation"></a>Как выполнить Установка длительности анимации
Объект <xref:System.Windows.Media.Animation.Timeline> представляет сегмент времени и длина этого сегмента определяется временной шкалы <xref:System.Windows.Duration>. Когда <xref:System.Windows.Media.Animation.Timeline> достигает окончания своей длительности, воспроизведение прекращается. Если <xref:System.Windows.Media.Animation.Timeline> имеет дочерние временные шкалы, их воспроизведение также останавливается. В случае анимации <xref:System.Windows.Duration> указывает, сколько требуется для анимации перехода от начального к конечному значению.  
  
 Можно указать <xref:System.Windows.Duration> с определенным, ограниченным временем или специальных значений <xref:System.Windows.Duration.Automatic%2A> или <xref:System.Windows.Duration.Forever%2A>. Длительность анимации должна включать значение времени, так как анимации всегда должны иметь определенную, ограниченную длину — в противном случае анимации не известно, как выполнять переход между значениями. Временные шкалы контейнера (<xref:System.Windows.Media.Animation.TimelineGroup> объекты), такие как <xref:System.Windows.Media.Animation.Storyboard> и <xref:System.Windows.Media.Animation.ParallelTimeline>, имеют по умолчанию продолжительность <xref:System.Windows.Duration.Automatic%2A>, то есть они автоматически завершаются после последнего дочернего останавливает воспроизведение.  
  
 В следующем примере, ширину, высоту и заливки цвет <xref:System.Windows.Shapes.Rectangle> анимируется. Длительность, установленная для временных шкал анимации и контейнер, приводит к эффекты анимации, включая управление скоростью анимации и переопределение продолжительность дочерних шкал времени длительностью временной шкалы контейнера.  
  
## <a name="example"></a>Пример  
 [!code-xaml[timingbehaviors_snip#DurationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/DurationExample.xaml#durationexamplewholepage)]  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Duration>
- [Общие сведения об эффектах анимации](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
