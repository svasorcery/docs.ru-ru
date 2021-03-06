---
title: Как выполнить Назначение средства визуализации компоненту ToolStrip для приложения
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Renderer property [Windows Forms]
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStrip control [Windows Forms]
- MenuStrip control [Windows Forms]
- toolbars [Windows Forms], customizing
ms.assetid: 46acef3e-9844-4ae8-9a2e-3006fe99cadf
ms.openlocfilehash: 2eaa917ff903c1d9e1579ac9c9caa3f3db516afb
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577222"
---
# <a name="how-to-set-the-toolstrip-renderer-for-an-application"></a>Как выполнить Назначение средства визуализации компоненту ToolStrip для приложения
Настройка внешнего вида элементов управления <xref:System.Windows.Forms.ToolStrip> может производиться отдельно для каждого из них или для всех элементов управления <xref:System.Windows.Forms.ToolStrip>, используемых в приложении.  
  
## <a name="example"></a>Пример  
 В примере кода ниже показано, как выборочно применить пользовательское средство отрисовки к элементу управления <xref:System.Windows.Forms.ToolStrip> и элементу управления <xref:System.Windows.Forms.MenuStrip>.  
  
 Чтобы использовать этот пример, скомпилируйте и запустите приложение, а затем выберите область пользовательской отрисовки в элементе управления <xref:System.Windows.Forms.ComboBox>. Нажмите **Применить**, чтобы задать средство отрисовки.  
  
 Чтобы увидеть пользовательскую отрисовку элемента меню, выберите <xref:System.Windows.Forms.MenuStrip> параметр из <xref:System.Windows.Forms.ComboBox> управлять, щелкните **применить**, а затем откройте **файл** пункта меню.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#70](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#70)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#70](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#70)]  
  
 Чтобы применить пользовательское средство отрисовки ко всем элементам управления <xref:System.Windows.Forms.ToolStrip>, используемым в приложении, задайте свойство <xref:System.Windows.Forms.ToolStripManager.Renderer%2A?displayProperty=nameWithType>.  
  
 Чтобы применить пользовательское средство отрисовки к отдельному элементу управления <xref:System.Windows.Forms.ToolStrip>, задайте свойство <xref:System.Windows.Forms.ToolStrip.Renderer%2A?displayProperty=nameWithType>.  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   ссылки на сборки System.Design, System.Drawing и System.Windows.Forms.  
  
 Сведения о выполнении сборки этого примера из командной строки для visual Basic или Visual C#, см. в разделе [построение из командной строки](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) или [командной строки создания с помощью csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). Можно также сборке этого примера в Visual Studio путем вставки кода в новый проект.  Также см. раздел [Как Компиляция и выполнение примера кода завершения Windows Forms с помощью Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.ToolStripManager>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripProfessionalRenderer>
- [Элемент управления ToolStrip](../../../../docs/framework/winforms/controls/toolstrip-control-windows-forms.md)
