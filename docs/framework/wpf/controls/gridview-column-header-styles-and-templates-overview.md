---
title: Общие сведения о стилях заголовков столбцов GridView и шаблонах
ms.date: 03/30/2017
helpviewer_keywords:
- column headers [WPF], customizing
- ListView controls [WPF], GridView column header styles
- controls [WPF], ListView
- headers [WPF], customizing
- GridView view mode [WPF], customizing column headers
ms.assetid: 74835674-a39e-4ab5-9418-ad7f6ab7b956
ms.openlocfilehash: 7cc758760075746971dd0d397568c64e7baf8b67
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590907"
---
# <a name="gridview-column-header-styles-and-templates-overview"></a>Общие сведения о стилях заголовков столбцов GridView и шаблонах
В этом обзоре рассматривается порядок приоритета для свойств, которые позволяют настроить заголовок столбца в <xref:System.Windows.Controls.GridView> режим просмотра <xref:System.Windows.Controls.ListView> элемента управления.  
  
## <a name="customizing-a-column-header-in-a-gridview"></a>Настройка заголовка столбца в элементе управления GridView  
 Свойства, определяющие содержимое, макет и стиль заголовка столбца в <xref:System.Windows.Controls.GridView> находятся на множество связанных классов. Некоторые из этих свойств имеют функциональные возможности, схожие или же.  
  
 Строки в следующей таблице представляют собой группы свойств, которые выполняют ту же функцию. Эти свойства можно использовать для настройки заголовков столбцов в <xref:System.Windows.Controls.GridView>. Порядок приоритета для связанных свойств — справа налево, в которой свойство в крайнем правом столбце имеет наивысший приоритет. Например если <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> устанавливается на <xref:System.Windows.Controls.GridViewColumnHeader> объекта и <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A> набор в связанном <xref:System.Windows.Controls.GridViewColumn>, <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> имеет более высокий приоритет. В этом случае <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A> не оказывает влияния.  
  
 **Связанные свойства для заголовков столбцов в элементе управления GridView**  
  
|||||  
|-|-|-|-|  
|**Классы**|<xref:System.Windows.Controls.GridView>|<xref:System.Windows.Controls.GridViewColumn>|<xref:System.Windows.Controls.GridViewColumnHeader>|  
|**Свойства контекстного меню**|<xref:System.Windows.Controls.GridView.ColumnHeaderContextMenu%2A>|Неприменимо|<xref:System.Windows.FrameworkElement.ContextMenu%2A>|  
|**ToolTip**<br /><br /> **Свойства**|<xref:System.Windows.Controls.GridView.ColumnHeaderToolTip%2A>|Неприменимо|<xref:System.Windows.FrameworkElement.ToolTip%2A>|  
|**Шаблон заголовка**<br /><br /> **Свойства**|<xref:System.Windows.Controls.GridView.ColumnHeaderTemplate%2A> <sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.GridView.ColumnHeaderTemplateSelector%2A>|<xref:System.Windows.Controls.GridViewColumn.HeaderTemplate%2A> <sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.GridViewColumn.HeaderTemplateSelector%2A>|<xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> <sup>1</sup>/<br /><br /> <xref:System.Windows.Controls.ContentControl.ContentTemplateSelector%2A>|  
|**Свойства стиля**|<xref:System.Windows.Controls.GridView.ColumnHeaderContainerStyle%2A>|<xref:System.Windows.Controls.GridViewColumn.HeaderContainerStyle%2A>|<xref:System.Windows.FrameworkElement.Style%2A>|  
  
 <sup>1</sup>для **свойства шаблона заголовка**, если выбрать шаблон и свойства селектор шаблона, имеет приоритет свойства шаблона. Например, если установить оба <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> и <xref:System.Windows.Controls.ContentControl.ContentTemplateSelector%2A> свойства, <xref:System.Windows.Controls.ContentControl.ContentTemplate%2A> свойство имеет более высокий приоритет.  
  
## <a name="see-also"></a>См. также
- [Разделы практического руководства](../../../../docs/framework/wpf/controls/listview-how-to-topics.md)
- [Общие сведения об элементе управления ListView](../../../../docs/framework/wpf/controls/listview-overview.md)
- [Общие сведения о GridView](../../../../docs/framework/wpf/controls/gridview-overview.md)
