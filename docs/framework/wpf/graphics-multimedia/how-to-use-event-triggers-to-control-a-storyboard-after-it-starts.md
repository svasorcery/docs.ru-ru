---
title: Как выполнить Использование триггеров событий для управления раскадровкой после ее запуска
ms.date: 03/30/2017
helpviewer_keywords:
- triggers [WPF], controlling Storyboards
- event triggers [WPF], controlling Storyboards
- Storyboards [WPF], controlling after start
ms.assetid: 3b115594-6a93-4972-b24d-61aa16f1c15f
ms.openlocfilehash: e4cfaf2352c3cca2b67a8e6a5d4c933399583e5a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54663652"
---
# <a name="how-to-use-event-triggers-to-control-a-storyboard-after-it-starts"></a>Как выполнить Использование триггеров событий для управления раскадровкой после ее запуска
В этом примере показано, как управлять <xref:System.Windows.Media.Animation.Storyboard> после ее запуска. Чтобы запустить <xref:System.Windows.Media.Animation.Storyboard> с помощью [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], использовать <xref:System.Windows.Media.Animation.BeginStoryboard>, которая распределяет анимации объектов и свойств и затем запускает раскадровку. Если вы предоставите <xref:System.Windows.Media.Animation.BeginStoryboard> имя, указав его <xref:System.Windows.Media.Animation.BeginStoryboard.Name%2A> свойство, можно упростить управляемой раскадровки. Вы можете затем интерактивно управлять раскадровкой после ее запуска.  
  
 Используйте следующие действия раскадровки вместе с <xref:System.Windows.EventTrigger> объектов для управления раскадровкой.  
  
-   <xref:System.Windows.Media.Animation.PauseStoryboard>: Приостанавливает раскадровку.  
  
-   <xref:System.Windows.Media.Animation.ResumeStoryboard>: Возобновляет приостановленную раскадровку.  
  
-   <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>: Изменяет скорость раскадровки.  
  
-   <xref:System.Windows.Media.Animation.SkipStoryboardToFill>: Перемещает раскадровку в конец ее периода заполнения, если он имеется.  
  
-   <xref:System.Windows.Media.Animation.StopStoryboard>: Останавливает раскадровку.  
  
-   <xref:System.Windows.Media.Animation.RemoveStoryboard>: Удаляет раскадровку, освобождает ресурсы.  
  
## <a name="example"></a>Пример  
 В следующем примере действий для управляемой раскадровки для интерактивного управления раскадровкой.  
  
 **Примечание.** Пример управления раскадровкой с помощью кода, см. в разделе [управления раскадровки после он начинается с помощью его интерактивных методов](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md).  
  
 [!code-xaml[timingbehaviors_snip#ControlStoryboardExampleUsingWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/ControlStoryboardExample.xaml#controlstoryboardexampleusingwholepage)]  
  
 Дополнительные примеры см. в разделе [Коллекция примеров анимации](https://go.microsoft.com/fwlink/?LinkID=159969).  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Media.Animation.ResumeStoryboard>
- <xref:System.Windows.Media.Animation.SetStoryboardSpeedRatio>
- <xref:System.Windows.Media.Animation.SkipStoryboardToFill>
- <xref:System.Windows.Media.Animation.PauseStoryboard>
- <xref:System.Windows.Media.Animation.StopStoryboard>
- <xref:System.Windows.Media.Animation.SeekStoryboard>
- [Управление раскадровкой после ее запуска с помощью интерактивных методов](../../../../docs/framework/wpf/graphics-multimedia/how-to-control-a-storyboard-after-it-starts.md)
- [Общие сведения об эффектах анимации](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Общие сведения о раскадровке](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md)
