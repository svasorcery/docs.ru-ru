---
title: Общие сведения об элементе управления ToolBar (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- ToolBar
helpviewer_keywords:
- toolbars [Windows Forms], about toolbars
- ToolBar control [Windows Forms], about ToolBar controls
ms.assetid: d426b203-0216-4dbe-b834-1641e50a9c29
ms.openlocfilehash: 42c3d9c681da9ca87125a274fa12af623269bd70
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54745252"
---
# <a name="toolbar-control-overview-windows-forms"></a>Общие сведения об элементе управления ToolBar (Windows Forms)
> [!NOTE]
>  Элемент управления <xref:System.Windows.Forms.ToolStrip> заменяет элемент управления <xref:System.Windows.Forms.ToolBar> и расширяет его функциональные возможности; однако при необходимости элемент управления <xref:System.Windows.Forms.ToolBar> можно сохранить для обратной совместимости и использования в будущем.  
  
 Элемент управления Windows Forms <xref:System.Windows.Forms.ToolBar> используется в формах в качестве панели управления, на которой выводится ряд раскрывающихся меню и кнопок с растровыми изображениями, активирующих команды. То есть нажатие кнопки на панели инструментов может быть эквивалентно выбору команды в меню. Для кнопок можно настроить режим поведения кнопок, раскрывающихся меню или разделителей. Обычно на панели инструментов содержатся кнопки и меню, соответствующие элементам в структуре меню приложения, которые предоставляют быстрый доступ к наиболее часто используемым в приложении функциям и командам.  
  
## <a name="working-with-the-toolbar-control"></a>Работа с элементом управления ToolBar  
 Объект <xref:System.Windows.Forms.ToolBar> обычно «прикреплен данный элемент управления» в верхней части родительского окна, но его можно также закрепить с любой стороны окна. На панели инструментов могут отображаться подсказки, когда пользователь наводит указатель мыши на кнопку. Всплывающая подсказка представляет собой небольшое всплывающее окно с кратким описанием назначения кнопки или меню. Для отображения подсказки, <xref:System.Windows.Forms.ToolBar.ShowToolTips%2A> свойству должно быть присвоено `true`.  
  
> [!NOTE]
>  В некоторых приложениях представлены элементы управления, очень похожие на панель инструментов, они могут "плавать" над окном приложения, кроме того, их можно перемещать. Элемент управления панели инструментов Windows Forms не может выполнять такие действия.  
  
 Когда <xref:System.Windows.Forms.ToolBar.Appearance%2A> свойству <xref:System.Windows.Forms.ToolBarAppearance>, кнопки панели инструментов отображаются приподнятыми и трехмерными. Можно задать <xref:System.Windows.Forms.ToolBar.Appearance%2A> свойства панели инструментов, чтобы <xref:System.Windows.Forms.ToolBarAppearance> плоскими панели инструментов и ее кнопок. При наведении указателя мыши на плоскую кнопку она становится объемной. Кнопки панели инструментов можно разделить на логические группы с помощью разделителя. Разделитель — кнопка панели инструментов с <xref:System.Windows.Forms.ToolBarButton.Style%2A> свойство значение <xref:System.Windows.Forms.ToolBarButtonStyle>. Он отображается как пустое место на панели инструментов. Если панель инструментов отображается плоской, разделители кнопок изображаются как линии, а не пустые пространства между кнопками.  
  
 <xref:System.Windows.Forms.ToolBar> Элемент управления позволяет создавать панели инструментов, добавив <xref:System.Windows.Forms.Button> объектов <xref:System.Windows.Forms.ToolBar.Buttons%2A> коллекции. Можно использовать редактор коллекции для добавления кнопок <xref:System.Windows.Forms.ToolBar> элемента управления, каждый из которых <xref:System.Windows.Forms.Button> объекта должен быть текст или изображение назначена, несмотря на то, что можно назначить обе. Изображение предоставляется связанным компонентом [ImageList](../../../../docs/framework/winforms/controls/imagelist-component-windows-forms.md). Во время выполнения, можно добавить или удалить кнопки из <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection> с помощью <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection.Add%2A> и <xref:System.Windows.Forms.ToolBar.ToolBarButtonCollection.Remove%2A> методы. Для программирования кнопок <xref:System.Windows.Forms.ToolBar>, добавьте код для <xref:System.Windows.Forms.ToolBar.ButtonClick> события <xref:System.Windows.Forms.ToolBar>, с использованием <xref:System.Windows.Forms.ToolBarButtonClickEventArgs.Button%2A> свойство <xref:System.Windows.Forms.ToolBarButtonClickEventArgs> класс, чтобы определить, какая кнопка была нажата.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.ToolBar>
- [Элемент управления ToolBar](../../../../docs/framework/winforms/controls/toolbar-control-windows-forms.md)
- [Практическое руководство. Добавление кнопок в элемент управления ToolBar](../../../../docs/framework/winforms/controls/how-to-add-buttons-to-a-toolbar-control.md)
- [Практическое руководство. Определение значка для кнопки панели инструментов](../../../../docs/framework/winforms/controls/how-to-define-an-icon-for-a-toolbar-button.md)
- [Практическое руководство. Триггер событий меню для кнопок панели инструментов](../../../../docs/framework/winforms/controls/how-to-trigger-menu-events-for-toolbar-buttons.md)
