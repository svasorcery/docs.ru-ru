---
title: Как выполнить Группа элементов управления RadioButton Windows Forms выступать в качестве набора
ms.date: 03/30/2017
helpviewer_keywords:
- radio buttons [Windows Forms], grouping
- controls [Windows Forms], grouping
- Windows Forms controls, grouping
- RadioButton control [Windows Forms], grouping
ms.assetid: 58f8fe34-50b7-49d8-a2be-c271be3c6b32
ms.openlocfilehash: 2758ff2380431668b2c908dbddd5dbe2094ccd0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54569340"
---
# <a name="how-to-group-windows-forms-radiobutton-controls-to-function-as-a-set"></a>Как выполнить Группа элементов управления RadioButton Windows Forms выступать в качестве набора
Windows Forms <xref:System.Windows.Forms.RadioButton> элементы управления позволяют пользователям для выбора между двумя или несколькими параметрами, в которых можно назначить только один для процедуры или объекта. Например, группы <xref:System.Windows.Forms.RadioButton> элементов управления может отображать выбор способа доставки заказа, но только один способ будет использоваться. Таким образом, только один <xref:System.Windows.Forms.RadioButton> за раз можно выбрать, даже если он является частью функциональной группы.  
  
 Группы переключателей путем их рисования внутри контейнеров, таких как <xref:System.Windows.Forms.Panel> управления <xref:System.Windows.Forms.GroupBox> управления или форма. Всех переключателей, которые добавляются напрямую в одну группу становятся формы. Чтобы добавить отдельные группы, необходимо разместить их внутри элементов управления или групп. Дополнительные сведения о панелях и группах, см. в разделе [Обзор элемента управления панели](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md) или [Обзор элемента управления GroupBox](../../../../docs/framework/winforms/controls/groupbox-control-overview-windows-forms.md).  
  
### <a name="to-group-radiobutton-controls-as-a-set-to-function-independently-of-other-sets"></a>Чтобы сгруппировать элементы управления RadioButton как набор функции, независимо от других наборов  
  
1.  Перетащите <xref:System.Windows.Forms.GroupBox> или <xref:System.Windows.Forms.Panel> управления из **Windows Forms** вкладке **элементов** на форму.  
  
2.  Рисование <xref:System.Windows.Forms.RadioButton> элементов управления в <xref:System.Windows.Forms.GroupBox> или <xref:System.Windows.Forms.Panel> элемента управления.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.RadioButton>
- [Общие сведения об элементе управления RadioButton](../../../../docs/framework/winforms/controls/radiobutton-control-overview-windows-forms.md)
- [Общие сведения об элементе управления Panel](../../../../docs/framework/winforms/controls/panel-control-overview-windows-forms.md)
- [Общие сведения об элементе управления GroupBox](../../../../docs/framework/winforms/controls/groupbox-control-overview-windows-forms.md)
- [Общие сведения об элементе управления CheckBox](../../../../docs/framework/winforms/controls/checkbox-control-overview-windows-forms.md)
- [Элемент управления RadioButton](../../../../docs/framework/winforms/controls/radiobutton-control-windows-forms.md)
