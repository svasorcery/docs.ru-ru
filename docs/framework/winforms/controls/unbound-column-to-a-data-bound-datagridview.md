---
title: Как выполнить Добавление несвязанного столбца к элементу управления DataGridView с привязкой к данным Windows Forms
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- columns [Windows Forms], unbound data
- data grids [Windows Forms], adding unbound columns
- DataGridView control [Windows Forms], unbound data
ms.assetid: f7bdc4d8-ba8e-421b-ad62-82d936f01372
ms.openlocfilehash: e877545f93fb57b636fd2e1559f52b4ad70a0b4e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722768"
---
# <a name="how-to-add-an-unbound-column-to-a-data-bound-windows-forms-datagridview-control"></a>Как выполнить Добавление несвязанного столбца к элементу управления DataGridView с привязкой к данным Windows Forms
Данные, отображаемые в элементе управления <xref:System.Windows.Forms.DataGridView>, обычно берутся из какого-либо источника данных, однако может потребоваться отобразить столбец данных, которые получены не из источника данных. Такой столбец называется непривязанным. Непривязанные столбцы могут принимать различные формы. Как правило, они используются для предоставления доступа к сведениям о строке данных.  
  
 В следующем примере кода демонстрируется создание несвязанного столбца **сведения** кнопки для отображения дочерней таблицы, связанные с определенной строкой в родительской таблице, при реализации сценария «основной/подробности». Для реакции на нажатия кнопок реализован обработчик событий <xref:System.Windows.Forms.DataGridView.CellClick?displayProperty=nameWithType>, который отображает форму, содержащую дочернюю таблицу.  
  
 Эта задача поддерживается в Visual Studio.  Также см. раздел [Как Добавлять и удалять столбцы в элементе управления DataGridView формы Windows с помощью конструктора](https://msdn.microsoft.com/library/dyyesckz\(v=vs.110\))  
  
## <a name="example"></a>Пример  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#010](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#010)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#010](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#010)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Для этого примера требуются:  
  
-   элемент управления <xref:System.Windows.Forms.DataGridView> с именем `dataGridView1`;  
  
-   ссылки на сборки <xref:System?displayProperty=nameWithType> и <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>См. также
- <xref:System.Windows.Forms.DataGridView>
- [Отображение данных с помощью элемента управления DataGridView в Windows Forms](../../../../docs/framework/winforms/controls/displaying-data-in-the-windows-forms-datagridview-control.md)
- [Режимы отображения данных в элементе управления DataGridView в Windows Forms](../../../../docs/framework/winforms/controls/data-display-modes-in-the-windows-forms-datagridview-control.md)
