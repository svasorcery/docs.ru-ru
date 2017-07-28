---
title: "Пример. Упорядочение элементов управления в формах Windows Forms с помощью элемента FlowLayoutPanel | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-winforms"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "jsharp"
helpviewer_keywords: 
  - "FlowLayoutPanel — элемент управления [Windows Forms], пошаговые руководства"
  - "элементы управления Windows Forms, упорядочение"
  - "элементы управления [Windows Forms], упорядочение с помощью FlowLayoutPanel"
  - "макет [Windows Forms], пошаговые руководства"
ms.assetid: a1744323-0316-49c2-992e-ebfc0a976b85
caps.latest.revision: 22
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 22
---
# Пример. Упорядочение элементов управления в формах Windows Forms с помощью элемента FlowLayoutPanel
В некоторых приложениях требуется форма, макет которой изменяется надлежащим образом при изменении размера формы или содержимого. Если необходим динамический макет и вы не хотите обрабатывать события <xref:System.Windows.Forms.Control.Layout> явно в коде, рассмотрите возможность использования панели макета.  
  
 Элементы управления <xref:System.Windows.Forms.FlowLayoutPanel> и <xref:System.Windows.Forms.TableLayoutPanel> предоставляют удобные способы упорядочения элементов управления в форме. Они обеспечивают автоматическую настраиваемую возможность управления относительным положением содержащихся в них дочерних элементов управления и предоставляют функции динамического макета во время выполнения и таким образом могут изменять размер и положение дочерних элементов управления по мере измерения размеров родительской формы. Панели макета могут быть вложенными в других панелях макета, что позволяет реализовывать сложные пользовательские интерфейсы.  
  
 Элемент управления <xref:System.Windows.Forms.TableLayoutPanel> упорядочивает свое содержимое в сетке, обеспечивая функциональные возможности, аналогичные возможностям элемента HTML \<table\>. Его ячейки организованы в строки и столбцы, и они могут быть разного размера. Для получения дополнительной информации см. [Пошаговое руководство. Упорядочение элементов управления в формах Windows Forms с помощью элемента TableLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md).  
  
 Элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> упорядочивает свое содержимое в определенном направлении, горизонтальном или вертикальном. Его содержимое может быть перенесено из одной строки в следующую или из одного столбца в следующий. Кроме того, вместо переноса содержимое может обрезаться. В данном пошаговом руководстве представлены следующие задачи.  
  
-   Создание проекта Windows Forms  
  
-   Упорядочивание элементов управления по горизонтали и по вертикали  
  
-   Изменение направления потока  
  
-   Вставка разрывов потока  
  
-   Упорядочивание элементов управления с использованием отбивки и полей  
  
-   Вставка элементов управления двойным щелчком по ним в панели элементов  
  
-   Вставка элемента управления путем рисования его контура  
  
-   Вставка элементов управления с помощью курсора  
  
-   Переназначение существующих элементов управления другим родительским элементам  
  
 После завершения вы будете понимать роль, которую играют эти важные функции макета.  
  
> [!NOTE]
>  Отображаемые диалоговые окна и команды меню могут отличаться от описанных в справке в зависимости от текущих параметров или выпуска. Чтобы изменить параметры, выберите в меню **Сервис** пункт **Импорт и экспорт параметров**. Дополнительные сведения см. в статье [Настройка параметров разработки в Visual Studio](http://msdn.microsoft.com/ru-ru/22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
## Создание проекта  
 Первым шагом является создание проекта и настройка формы.  
  
#### Создание проекта  
  
1.  Создайте проект приложения Windows с именем FlowLayoutPanelExample. Для получения дополнительной информации см. [How to: Create a Windows Application Project](http://msdn.microsoft.com/ru-ru/b2f93fed-c635-4705-8d0e-cf079a264efa).  
  
2.  Выберите форму в **конструкторе форм**.  
  
## Упорядочивание элементов управления по горизонтали и по вертикали  
 Элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> позволяет размещать элементы управления в строках или столбцах без необходимости точного указания положения каждого отдельного элемента управления.  
  
 Элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> может изменять размер или положение своих дочерних элементов управления по мере измерения размеров родительской формы.  
  
#### Размещение элементов управления по горизонтали или по вертикали с помощью FlowLayoutPanel  
  
1.  Перетащите элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> из **панели элементов** в свою форму.  
  
2.  Перетащите элемент управления <xref:System.Windows.Forms.Button> из **панели элементов** в <xref:System.Windows.Forms.FlowLayoutPanel>. Обратите внимание, что он автоматически перемещается в левый верхний угол элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
3.  Перетащите другой элемент управления <xref:System.Windows.Forms.Button> из **панели элементов** в <xref:System.Windows.Forms.FlowLayoutPanel>. Обратите внимание, что элемент управления <xref:System.Windows.Forms.Button> автоматически перемещается в место рядом с первым элементом управления <xref:System.Windows.Forms.Button>. Если ваша панель <xref:System.Windows.Forms.FlowLayoutPanel> слишком узка для размещения двух элементов управления в одной строке, то новый элемент управления <xref:System.Windows.Forms.Button> автоматически переносится на следующую строку.  
  
4.  Перетащите еще несколько элементов управления <xref:System.Windows.Forms.Button> из **панели элементов** в <xref:System.Windows.Forms.FlowLayoutPanel>. Продолжайте размещать элементы управления <xref:System.Windows.Forms.Button>, пока один из них не переместится в следующую строку.  
  
5.  Измените значение свойства <xref:System.Windows.Forms.FlowLayoutPanel.WrapContents%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> на `false`. Обратите внимание, что дочерние элементы управления больше не помещаются в следующую строку. Вместо этого они перемещаются в первую строку и обрезаются.  
  
6.  Измените значение свойства <xref:System.Windows.Forms.FlowLayoutPanel.WrapContents%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> на `true`. Обратите внимание, что дочерние элементы управления снова переносятся в следующую строку.  
  
7.  Уменьшите ширину элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>, пока все элементы управления <xref:System.Windows.Forms.Button> не переместятся в первый столбец.  
  
8.  Увеличьте ширину элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>, пока все элементы управления <xref:System.Windows.Forms.Button> не переместятся в первую строку. Может потребоваться изменить размер формы, чтобы она вмещала большую ширину.  
  
## Изменение направления потока  
 Свойство <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A> позволяет изменить направление расположения элементов управления. Вы можете размещать дочерние элементы управления слева направо, справа налево, сверху вниз или снизу вверх.  
  
#### Изменение направления потока в элементе управления FlowLayoutPanel  
  
1.  Измените значение свойства <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> на <xref:System.Windows.Forms.FlowDirection>. Обратите внимание, что дочерние элементы управления перестраиваются в один или несколько столбцов, в зависимости от высоты данного элемента управления.  
  
2.  Измените размер <xref:System.Windows.Forms.FlowLayoutPanel>, чтобы его высота была меньше, чем столбец элементов управления <xref:System.Windows.Forms.Button>. Обратите внимание, что <xref:System.Windows.Forms.FlowLayoutPanel> перестраивает дочерние элементы управления, чтобы они перешли в следующий столбец. Продолжайте уменьшать высоту и обратите внимание, что дочерние элементы управления перемещаются в последующие столбцы. Измените значение свойства <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> на <xref:System.Windows.Forms.FlowDirection>. Обратите внимание, что позиции дочерних элементов управления изменяются в обратном направлении. Проследите за макетом при изменении значения свойства <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A> на <xref:System.Windows.Forms.FlowDirection>.  
  
## Вставка разрывов потока  
 Элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> предоставляет свойство FlowBreak своим дочерним элементам управления. Если свойству FlowBreak присвоено значение `true`, элементы управления внутри элемента <xref:System.Windows.Forms.FlowLayoutPanel> перестают размещаться в текущем направлении и переносятся на следующую строку или в следующий столбец.  
  
#### Вставка разрывов потока  
  
1.  Измените значение свойства <xref:System.Windows.Forms.FlowLayoutPanel.FlowDirection%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> на <xref:System.Windows.Forms.FlowDirection>.  
  
2.  Выберите один из элементов управления <xref:System.Windows.Forms.Button> в середине самого левого столбца.  
  
3.  Измените значение свойства FlowBreak элемента управления <xref:System.Windows.Forms.Button> на `true`. Обратите внимание, что столбец разрывается, и элементы управления, следующие за выбранным элементом управления <xref:System.Windows.Forms.Button>, переносятся в следующий столбец. Задайте для свойства FlowBreak элемента управления <xref:System.Windows.Forms.Button> значение `false`, чтобы вернуться к исходному поведению.  
  
## Размещение элементов управления с использованием закрепления и привязки  
 Функциональные возможности закрепления и привязки дочерних элементов управления отличаются от их функциональных возможностей в других контейнерных элементах управления. И закрепление, и привязка относятся к самому крупному элементу управления в направлении потока.  
  
#### Размещение элементов управления с использованием закрепления и привязки  
  
1.  Увеличивайте размер <xref:System.Windows.Forms.FlowLayoutPanel>, пока все элементы управления <xref:System.Windows.Forms.Button> не будут расположены в столбце.  
  
2.  Выберите верхний элемент управления <xref:System.Windows.Forms.Button>. Увеличьте его ширину, чтобы он стал примерно вдвое шире других элементов управления <xref:System.Windows.Forms.Button>.  
  
3.  Выберите второй элемент управления <xref:System.Windows.Forms.Button>. Измените значение его свойства <xref:System.Windows.Forms.Control.Anchor%2A> на <xref:System.Windows.Forms.AnchorStyles>. Обратите внимание, что он перемещается так, чтобы его правая граница выровнялась с правой границей первого элемента управления <xref:System.Windows.Forms.Button>.  
  
4.  Измените значение его свойства <xref:System.Windows.Forms.Control.Anchor%2A> на <xref:System.Windows.Forms.AnchorStyles> и <xref:System.Windows.Forms.AnchorStyles>. Обратите внимание, что он принимает ту же ширину, что и первый элемент управления <xref:System.Windows.Forms.Button>.  
  
5.  Выберите третий элемент управления <xref:System.Windows.Forms.Button>. Измените значение его свойства <xref:System.Windows.Forms.Control.Dock%2A> на <xref:System.Windows.Forms.DockStyle>. Обратите внимание, что он принимает ту же ширину, что и первый элемент управления <xref:System.Windows.Forms.Button>.  
  
## Упорядочивание элементов управления с использованием отбивки и полей  
 Можно также упорядочивать элементы управления в вашем элементе управления <xref:System.Windows.Forms.FlowLayoutPanel>, изменяя свойства <xref:System.Windows.Forms.Control.Padding%2A> и <xref:System.Windows.Forms.Control.Margin%2A>.  
  
 Свойство <xref:System.Windows.Forms.Control.Padding%2A> позволяет управлять расположением элементов управления в ячейке <xref:System.Windows.Forms.FlowLayoutPanel> элемента управления. Оно задает расстояние между дочерними элементами управления и границей элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
 Свойство <xref:System.Windows.Forms.Control.Margin%2A> позволяет управлять расстоянием между элементами управления.  
  
#### Размещение элементов управления с помощью свойств Padding и Margin  
  
1.  Измените значение свойства <xref:System.Windows.Forms.Control.Dock%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> на <xref:System.Windows.Forms.DockStyle>. Если ваша форма достаточно большая, элементы управления <xref:System.Windows.Forms.Button> будут перемещены в первый столбец элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
2.  Измените значение свойства <xref:System.Windows.Forms.Control.Padding%2A> элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>, развернув запись <xref:System.Windows.Forms.Control.Padding%2A> в окне **Свойства** и установив для свойства <xref:System.Windows.Forms.Padding.All%2A> значение **20**. Дополнительные сведения см. в разделе [Пошаговое руководство. Создание структуры элементов управления Windows Forms с помощью свойств "Padding", "Margins" и "AutoSize"](../../../../docs/framework/winforms/controls/windows-forms-controls-padding-autosize.md). Обратите внимание, что дочерние элементы управления перемещаются к центру элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>. Увеличенное значение свойства <xref:System.Windows.Forms.Control.Padding%2A> отодвигает дочерние элементы управления от границ элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
3.  Выберите все элементы управления <xref:System.Windows.Forms.Button> в <xref:System.Windows.Forms.FlowLayoutPanel> и задайте в свойстве <xref:System.Windows.Forms.Control.Margin%2A> значение **20**. Обратите внимание, что расстояние между элементами управления <xref:System.Windows.Forms.Button> увеличивается, поэтому они раздвигаются. Может потребоваться изменить размер элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>, чтобы увидеть все дочерние элементы управления.  
  
## Вставка элементов управления двойным щелчком по ним в панели элементов  
 Вы можете заполнять свой элемент управления <xref:System.Windows.Forms.FlowLayoutPanel>, дважды щелкая элементы управления в **панели элементов**.  
  
#### Вставка элементов управления двойным щелчком по ним в панели элементов  
  
1.  Дважды щелкните значок элемента управления <xref:System.Windows.Forms.Button> в **панели элементов**. Обратите внимание, что в элементе управления <xref:System.Windows.Forms.FlowLayoutPanel> появился новый элемент управления <xref:System.Windows.Forms.Button>.  
  
2.  Дважды щелкните несколько других элементов управления в **панели элементов**. Обратите внимание, что новые элементы управления последовательно появляются в элементе управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
## Вставка элемента управления путем рисования его контура  
 Вы можете вставить элемент управления в элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> и задать его размер, нарисовав его контур в ячейке.  
  
#### Вставка элемента управления путем рисования его контура  
  
1.  В **панели элементов** щелкните значок элемента управления <xref:System.Windows.Forms.Button>. Не перетаскивайте его в форму.  
  
2.  Наведите указатель мыши на элемент управления <xref:System.Windows.Forms.FlowLayoutPanel>. Обратите внимание, что указатель превратился в перекрестие с прикрепленным значком элемента управления <xref:System.Windows.Forms.Button>.  
  
3.  Нажмите и удерживайте кнопку мыши.  
  
4.  Перемещайте указатель мыши, чтобы нарисовать контур элемента управления <xref:System.Windows.Forms.Button>. Когда вас устроит размер, отпустите кнопку мыши. Обратите внимание, что элемент управления <xref:System.Windows.Forms.Button> создается в следующем пустом месте элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
## Вставка элементов управления с помощью полосы вставки  
 Вы можете вставлять элементы управления в определенном месте в элементе управления <xref:System.Windows.Forms.FlowLayoutPanel>. При перетаскивании элемента управления в клиентскую область элемента управления <xref:System.Windows.Forms.FlowLayoutPanel> появляется полоса вставки, указывающая место, куда будет вставлен элемент управления.  
  
#### Вставка элемента управления с помощью курсора  
  
1.  Перетащите элемент управления <xref:System.Windows.Forms.Button> из **панели элементов** в элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> и укажите место между двумя элементами управления <xref:System.Windows.Forms.Button>. Обратите внимание, что выводится полоса вставки, показывающая, где будет размещен <xref:System.Windows.Forms.Button> при его вставке в элемент управления<xref:System.Windows.Forms.FlowLayoutPanel>. Прежде чем вставить новый элемент управления <xref:System.Windows.Forms.Button> в элемент управления <xref:System.Windows.Forms.FlowLayoutPanel>, перемещайте указатель мыши, чтобы понаблюдать за перемещением полосы вставки.  
  
2.  Вставьте новый элемент управления <xref:System.Windows.Forms.Button> в элемент управления <xref:System.Windows.Forms.FlowLayoutPanel>. Обратите внимание, что новый элемент управления <xref:System.Windows.Forms.Button> не выравнивается с другими, так как его свойство <xref:System.Windows.Forms.Control.Margin%2A> имеет другое значение.  
  
## Переназначение существующих элементов управления другим родительским элементам  
 Вы можете назначать элементы управления, существующие в вашей форме, новому элементу управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
#### Изменение родительского объекта существующих элементов управления  
  
1.  Перетащите три элемента управления <xref:System.Windows.Forms.Button> с **панели элементов** в форму. Расположите их рядом друг с другом, но не выравнивайте.  
  
2.  В **панели элементов** щелкните значок элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>. Не перетаскивайте его в форму.  
  
3.  Переместите указатель мыши к трем элементам управления <xref:System.Windows.Forms.Button>. Обратите внимание, что указатель превратился в перекрестие с прикрепленным значком элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
4.  Нажмите и удерживайте кнопку мыши.  
  
5.  Перемещайте указатель мыши, чтобы нарисовать контур элемента управления <xref:System.Windows.Forms.FlowLayoutPanel>. Обведите таким образом три элемента управления <xref:System.Windows.Forms.Button>.  
  
6.  Отпустите кнопку мыши. Теперь эти три элемента управления <xref:System.Windows.Forms.Button> вставлены в элемент управления <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
## Следующие действия  
 Используя сочетание панелей макета и элементов управления, можно создавать сложные макеты. Рекомендуется также дополнительно исследовать следующие моменты.  
  
-   Увеличьте размер элемента управления <xref:System.Windows.Forms.Button> и отметьте, как это отразится на макете.  
  
-   Панели макета могут содержать другие панели макета. Попробуйте вставить элемент управления <xref:System.Windows.Forms.TableLayoutPanel> в существующий элемент управления.  
  
-   Закрепите элемент управления <xref:System.Windows.Forms.FlowLayoutPanel> в родительской форме. Измените размер этой формы и обратите внимание, как это отражается на макете.  
  
-   Задайте для свойства <xref:System.Windows.Forms.Control.Visible%2A> одного из элементов управления значение `false` и обратите внимание, как в ответ перестраивается <xref:System.Windows.Forms.FlowLayoutPanel>.  
  
## См. также  
 <xref:System.Windows.Forms.FlowLayoutPanel>   
 <xref:System.Windows.Forms.TableLayoutPanel>   
 [Пошаговое руководство. Упорядочение элементов управления в формах Windows Forms с помощью элемента TableLayoutPanel](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)   
 [Пример. Упорядочение элементов управления в формах Windows Forms с помощью линий привязки](../../../../docs/framework/winforms/controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)   
 [Взаимодействие с пользователем в Microsoft Windows, официальные рекомендации для разработчиков и конструкторов пользовательских интерфейсов. Redmond, WA: Microsoft Press, 1999 г. \(USBN: 0\-7356\-0566\-1\)](http://www.microsoft.com/mspress/southpacific/books/book11588.htm)   
 [Свойство AutoSize](../../../../docs/framework/winforms/controls/autosize-property-overview.md)   
 [Практическое руководство. Закрепление элементов управления в формах Windows Forms.](../../../../docs/framework/winforms/controls/how-to-dock-controls-on-windows-forms.md)   
 [Практическое руководство. Привязка элементов управления в формах Windows Forms](../../../../docs/framework/winforms/controls/how-to-anchor-controls-on-windows-forms.md)   
 [Пошаговое руководство. Создание структуры элементов управления Windows Forms с помощью свойств "Padding", "Margins" и "AutoSize"](../../../../docs/framework/winforms/controls/windows-forms-controls-padding-autosize.md)