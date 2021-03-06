---
title: Как выполнить Задать размер панели строки состояния
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- StatusBar control [Windows Forms], panel size
- status bars [Windows Forms], setting panel size
- panels [Windows Forms], setting size in status bars
ms.assetid: a01bee43-d9eb-4954-84e6-45a93532d08d
ms.openlocfilehash: be1f216af61c1e7b77e84c584dc9d965a97c56b2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54539666"
---
# <a name="how-to-set-the-size-of-status-bar-panels"></a>Как выполнить Задать размер панели строки состояния
> [!NOTE]
>  Элемент управления <xref:System.Windows.Forms.ToolStripStatusLabel> заменяет элемент управления <xref:System.Windows.Forms.StatusBar> и расширяет его функциональные возможности; однако при необходимости элемент управления <xref:System.Windows.Forms.StatusBar> можно сохранить для обратной совместимости и использования в будущем.  
  
 Каждый экземпляр <xref:System.Windows.Forms.StatusBarPanel> класса в [элемента управления StatusBar](../../../../docs/framework/winforms/controls/statusbar-control-windows-forms.md) элемент управления имеет ряд динамических свойств, определяющих его ширину и изменение размеров во время выполнения.  
  
### <a name="to-set-the-size-of-a-panel"></a>Чтобы задать размер панели  
  
1.  В процедуре, задайте <xref:System.Windows.Forms.StatusBarPanel.AutoSize%2A>, <xref:System.Windows.Forms.StatusBarPanel.MinWidth%2A>, и <xref:System.Windows.Forms.StatusBarPanel.Width%2A> свойства (или любое подмножество этой последовательности) для строки состояния панели, с помощью индекса передать <xref:System.Windows.Forms.StatusBar.Panels%2A> свойство <xref:System.Windows.Forms.StatusBarPanel> коллекции.  
  
    ```vb  
    Public Sub SetStatusBarPanelSize()  
    ' Create panel and set text property.  
       StatusBar1.Panels.Add("One")  
    ' Set properties of panels.  
       StatusBar1.Panels(0).AutoSize = StatusBarPanelAutoSize.Spring  
       StatusBar1.Panels(0).Width = 200  
    ' Enable the StatusBar control to display panels.  
       StatusBar1.ShowPanels = True  
        End Sub  
    ```  
  
    ```csharp  
    public void SetStatusBarPanelSize()  
    {  
       // Create panel and set text property.  
       statusBar1.Panels.Add("One");  
       // Set properties of panels.  
       statusBar1.Panels[0].AutoSize = StatusBarPanelAutoSize.Spring;  
       statusBar1.Panels[0].Width = 200;  
       statusBar1.ShowPanels = true;  
    }  
    ```  
  
    ```cpp  
    public:  
       void SetStatusBarPanelSize()  
       {  
          // Create panel and set text property.  
          statusBar1->Panels->Add("One");  
          // Set properties of panels.  
          statusBar1->Panels[0]->AutoSize =  
             StatusBarPanelAutoSize::Spring;  
          statusBar1->Panels[0]->Width = 200;  
          statusBar1->ShowPanels = true;  
       }  
    ```  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.StatusBar>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- [Пошаговое руководство: Обновление строки состояния во время выполнения](../../../../docs/framework/winforms/controls/walkthrough-updating-status-bar-information-at-run-time.md)
- [Практическое руководство. Определить, какая из панелей в элемент управления Windows Forms StatusBar была нажата](../../../../docs/framework/winforms/controls/determine-which-panel-wf-statusbar-control-was-clicked.md)
- [Общие сведения об элементе управления StatusBar](../../../../docs/framework/winforms/controls/statusbar-control-overview-windows-forms.md)
