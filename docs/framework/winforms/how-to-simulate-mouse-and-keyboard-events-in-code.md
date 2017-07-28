---
title: "Практическое руководство. Имитация событий мыши и клавиатуры в коде | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-winforms"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "jsharp"
helpviewer_keywords: 
  - "клавиатуры, моделирование событий"
  - "ввод пользователя, моделирование"
  - "SendKeys, использование"
  - "щелчки мышью, моделирование"
  - "мышь, моделирование событий"
ms.assetid: 6abcb67e-3766-4af2-9590-bf5dabd17e41
caps.latest.revision: 14
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 14
---
# Практическое руководство. Имитация событий мыши и клавиатуры в коде
В Windows Forms предоставляется несколько возможностей для программной имитации ввода данных с помощью мыши и клавиатуры. В этом разделе приведен обзор этих возможностей.  
  
## Имитация ввода с помощью мыши  
 Наилучшим способом имитации событий мыши является вызов метода `On`*EventName*, в результате чего происходит событие мыши, которое требуется имитировать. Этот вариант обычно возможен только в пределах пользовательских элементов управления и форм, так как методы, которые вызывают события, защищены и недоступны вне элемента управления или формы. Например, ниже показано, как имитировать нажатие правой кнопки мыши в коде.  
  
#### Чтобы нажать правую кнопку мыши программными средствами, выполните указанные ниже действия.  
  
1.  Создайте объект <xref:System.Windows.Forms.MouseEventArgs> и установите для его свойства <xref:System.Windows.Forms.MouseEventArgs.Button%2A> значение <xref:System.Windows.Forms.MouseButtons?displayProperty=fullName>.  
  
2.  Вызовите метод <xref:System.Windows.Forms.Control.OnMouseClick%2A> с этим объектом <xref:System.Windows.Forms.MouseEventArgs> в качестве аргумента.  
  
 Дополнительные сведения о пользовательских элементах управления см. в разделе [Создание элементов управления Windows Forms во время разработки](../../../docs/framework/winforms/controls/developing-windows-forms-controls-at-design-time.md).  
  
 Существуют другие способы имитировать ввод с помощью мыши. Например, можно программно установить свойство элемента управления, которое представляет состояние, обычно устанавливаемое с помощью ввода мыши \(например, свойство <xref:System.Windows.Forms.CheckBox.Checked%2A> элемента управления <xref:System.Windows.Forms.CheckBox>\), или напрямую вызвать делегат, связанный с событием, которое нужно имитировать.  
  
## Имитация ввода с клавиатуры  
 Хотя ввод данных с клавиатуры можно имитировать с помощью подходов, описанных выше для ввода с помощью мыши, Windows Forms также предоставляет класс <xref:System.Windows.Forms.SendKeys> для отправки нажатий клавиш в активное приложение.  
  
> [!CAUTION]
>  Если приложение предназначено для международного использования с различными клавиатурами, применение метода <xref:System.Windows.Forms.SendKeys.Send%2A?displayProperty=fullName> может иметь непредсказуемые результаты и его следует избегать.  
  
> [!NOTE]
>  Класс <xref:System.Windows.Forms.SendKeys> был обновлен в .NET Framework 3.0, что позволило использовать его в приложениях, работающих в Windows Vista. Усиленная система безопасности Windows Vista \(известная как контроль учетных записей или UAC\) не позволяет предыдущей реализации работать должным образом.  
>   
>  Класс <xref:System.Windows.Forms.SendKeys> подвержен проблемам со временем, которые пришлось решать некоторым разработчикам. Обновленная реализация по\-прежнему подвержена этим проблемам, но она работает немного быстрее, поэтому существующие решения может потребоваться переработать. Класс <xref:System.Windows.Forms.SendKeys> сначала пытается использовать предыдущую реализацию, и если это не удается, использует новую реализацию. В результате класс <xref:System.Windows.Forms.SendKeys> может работать по\-разному в разных операционных системах. Кроме того, при использовании новой реализации класса <xref:System.Windows.Forms.SendKeys> метод <xref:System.Windows.Forms.SendKeys.SendWait%2A> не будет дожидаться обработки сообщений, если они отправляются другому процессу.  
>   
>  Если необходимо обеспечить согласованное поведение приложения независимо от операционной системы, можно заставить класс <xref:System.Windows.Forms.SendKeys> использовать новую реализацию, добавив указанный ниже параметр приложения в файл app.config.  
>   
>  `<appSettings>`  
>   
>  `<add key="SendKeys" value="SendInput"/>`  
>   
>  `</appSettings>`  
>   
>  Для принудительного использования классом <xref:System.Windows.Forms.SendKeys> предыдущей реализации задайте значение `"JournalHook"`.  
  
#### Отправка нажатия клавиши в то же приложение  
  
1.  Вызовите метод <xref:System.Windows.Forms.SendKeys.Send%2A> или <xref:System.Windows.Forms.SendKeys.SendWait%2A> класса <xref:System.Windows.Forms.SendKeys>. Указанные нажатия клавиш будут получены активным элементом управления приложения. В примере кода ниже метод <xref:System.Windows.Forms.SendKeys.Send%2A> используется для имитации нажатия клавиши ВВОД, когда пользователь дважды щелкает по поверхности формы. В этом примере используется форма <xref:System.Windows.Forms.Form> с одним элементом управления <xref:System.Windows.Forms.Button>, имеющим индекс перехода по клавише TAB, равный 0.  
  
     [!code-cpp[System.Windows.Forms.SimulateKeyPress#10](../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/cpp/form1.cpp#10)]
     [!code-csharp[System.Windows.Forms.SimulateKeyPress#10](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/CS/form1.cs#10)]
     [!code-vb[System.Windows.Forms.SimulateKeyPress#10](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/VB/form1.vb#10)]  
  
#### Отправка нажатия клавиши в другое приложение  
  
1.  Активируйте окно приложения, которое будет получать нажатия клавиш, а затем вызовите метод <xref:System.Windows.Forms.SendKeys.Send%2A> или <xref:System.Windows.Forms.SendKeys.SendWait%2A>. Из\-за отсутствия управляемого метода активации другого приложения необходимо использовать собственные методы Windows для принудительной установки фокуса на другие приложения. В примере кода ниже с помощью вызова неуправляемого кода вызываются методы `FindWindow` и `SetForegroundWindow` для активации окна приложения "Калькулятор", а затем вызывается метод <xref:System.Windows.Forms.SendKeys.SendWait%2A> для проведения ряда вычислений в этом приложении.  
  
    > [!NOTE]
    >  Параметры вызова `FindWindow` для определения положения Калькулятора зависят от версии Windows.  Приведенный ниже код находит Калькулятор в [!INCLUDE[win7](../../../includes/win7-md.md)]. В [!INCLUDE[windowsver](../../../includes/windowsver-md.md)] измените первый параметр на SciCalc. Для определения нужных параметров можно использовать средство Spy\+\+, входящее в состав Visual Studio.  
  
     [!code-cpp[System.Windows.Forms.SimulateKeyPress#5](../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/cpp/form1.cpp#5)]
     [!code-csharp[System.Windows.Forms.SimulateKeyPress#5](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/CS/form1.cs#5)]
     [!code-vb[System.Windows.Forms.SimulateKeyPress#5](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/VB/form1.vb#5)]  
  
## Пример  
 В примере ниже полностью представлено приложение для предыдущих примеров кода.  
  
 [!code-cpp[System.Windows.Forms.SimulateKeyPress#0](../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/cpp/form1.cpp#0)]
 [!code-csharp[System.Windows.Forms.SimulateKeyPress#0](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/CS/form1.cs#0)]
 [!code-vb[System.Windows.Forms.SimulateKeyPress#0](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.SimulateKeyPress/VB/form1.vb#0)]  
  
## Компиляция кода  
 Для этого примера требуются:  
  
-   ссылки на сборки System, System.Drawing и System.Windows.Forms.  
  
 Дополнительные сведения о выполнении сборки этого примера из командной строки для [!INCLUDE[vbprvb](../../../includes/vbprvb-md.md)] или [!INCLUDE[csprcs](../../../includes/csprcs-md.md)] см. в разделе [Построение из командной строки](../Topic/Building%20from%20the%20Command%20Line%20\(Visual%20Basic\).md) или [Построение из командной строки с помощью csc.exe](../../../ocs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Чтобы выполнить сборку этого примера в [!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)], можно также вставить код в новый проект.  См. также [Практическое руководство. Компиляция и выполнение откомпилированного примера кода формы Windows Forms с помощью Visual Studio](http://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## См. также  
 [User Input in Windows Forms](../../../docs/framework/winforms/user-input-in-windows-forms.md)