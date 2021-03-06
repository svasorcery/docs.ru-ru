---
title: Как выполнить Отображение определенных дней полужирным шрифтом с Windows Forms в элементе управления MonthCalendar
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- calendars [Windows Forms], displaying dates in bold
- examples [Windows Forms], calendar controls
- GetDayBold event
- MonthCalendar control [Windows Forms], dates displayed in bold
ms.assetid: 8b20db5b-8118-4825-90e8-2c45c186ac7d
ms.openlocfilehash: f310d5e30acffdd358bc5108f39102387289562e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54547791"
---
# <a name="how-to-display-specific-days-in-bold-with-the-windows-forms-monthcalendar-control"></a>Как выполнить Отображение определенных дней полужирным шрифтом с Windows Forms в элементе управления MonthCalendar
Windows Forms <xref:System.Windows.Forms.MonthCalendar> элемент управления может отображать дней полужирным шрифтом, либо как даты в единственном числе, либо на периодической основе. Это может сделать для привлечения внимания к особые даты, такие как праздники и выходные.  
  
 Три свойства определяют эту функцию. <xref:System.Windows.Forms.MonthCalendar.BoldedDates%2A> Свойство содержит отдельные даты. <xref:System.Windows.Forms.MonthCalendar.AnnuallyBoldedDates%2A> Свойство содержит даты, которые отображаются полужирным шрифтом каждый год. <xref:System.Windows.Forms.MonthCalendar.MonthlyBoldedDates%2A> Свойство содержит даты, которые отображаются полужирным шрифтом каждый месяц. Каждое из этих свойств содержит массив <xref:System.DateTime> объектов. Чтобы добавить или удалить дату из одного из этих списков, необходимо добавить или удалить <xref:System.DateTime> объекта.  
  
### <a name="to-make-a-date-appear-in-bold-type"></a>Полужирным шрифтом даты  
  
1.  Создание <xref:System.DateTime> объектов.  
  
    ```vb  
    Dim myVacation1 As Date = New DateTime(2001, 6, 10)  
    Dim myVacation2 As Date = New DateTime(2001, 6, 17)  
    ```  
  
    ```csharp  
    DateTime myVacation1 = new DateTime(2001, 6, 10);  
    DateTime myVacation2 = new DateTime(2001, 6, 17);  
    ```  
  
    ```cpp  
    DateTime myVacation1 = DateTime(2001, 6, 10);  
    DateTime myVacation2 = DateTime(2001, 6, 17);  
    ```  
  
2.  Выделение полужирным шрифтом дату путем вызова <xref:System.Windows.Forms.MonthCalendar.AddBoldedDate%2A>, <xref:System.Windows.Forms.MonthCalendar.AddAnnuallyBoldedDate%2A>, или <xref:System.Windows.Forms.MonthCalendar.AddMonthlyBoldedDate%2A> метод <xref:System.Windows.Forms.MonthCalendar> элемента управления.  
  
    ```vb  
    MonthCalendar1.AddBoldedDate(myVacation1)  
    MonthCalendar1.AddBoldedDate(myVacation2)  
    ```  
  
    ```csharp  
    monthCalendar1.AddBoldedDate(myVacation1);  
    monthCalendar1.AddBoldedDate(myVacation2);  
    ```  
  
    ```cpp  
    monthCalendar1->AddBoldedDate(myVacation1);  
    monthCalendar1->AddBoldedDate(myVacation2);  
    ```  
  
     – или –  
  
     Выделите дат полужирным за один раз, создав массив <xref:System.DateTime> объектов и присваивается одно из свойств.  
  
    ```vb  
    Dim VacationDates As DateTime() = {myVacation1, myVacation2}  
    MonthCalendar1.BoldedDates = VacationDates  
    ```  
  
    ```csharp  
    DateTime[] VacationDates = {myVacation1, myVacation2};  
    monthCalendar1.BoldedDates = VacationDates;  
    ```  
  
    ```cpp  
    Array<DateTime>^ VacationDates = {myVacation1, myVacation2};  
    monthCalendar1->BoldedDates = VacationDates;  
    ```  
  
### <a name="to-make-a-date-appear-in-the-regular-font"></a>Отображается обычным шрифтом даты  
  
1.  Один выделенный полужирным шрифтом даты отображается обычным шрифтом, вызвав <xref:System.Windows.Forms.MonthCalendar.RemoveBoldedDate%2A>, <xref:System.Windows.Forms.MonthCalendar.RemoveAnnuallyBoldedDate%2A>, или <xref:System.Windows.Forms.MonthCalendar.RemoveMonthlyBoldedDate%2A> метод.  
  
    ```vb  
    MonthCalendar1.RemoveBoldedDate(myVacation1)  
    MonthCalendar1.RemoveBoldedDate(myVacation2)  
    ```  
  
    ```csharp  
    monthCalendar1.RemoveBoldedDate(myVacation1);  
    monthCalendar1.RemoveBoldedDate(myVacation2);  
    ```  
  
    ```cpp  
    monthCalendar1->RemoveBoldedDate(myVacation1);  
    monthCalendar1->RemoveBoldedDate(myVacation2);  
    ```  
  
     – или –  
  
     Удалите все выделенные полужирным шрифтом даты из одной из трех списков, вызвав <xref:System.Windows.Forms.MonthCalendar.RemoveAllBoldedDates%2A>, <xref:System.Windows.Forms.MonthCalendar.RemoveAllAnnuallyBoldedDates%2A>, или <xref:System.Windows.Forms.MonthCalendar.RemoveAllMonthlyBoldedDates%2A> метод.  
  
    ```vb  
    MonthCalendar1.RemoveAllBoldedDates()  
    ```  
  
    ```csharp  
    monthCalendar1.RemoveAllBoldedDates();  
    ```  
  
    ```cpp  
    monthCalendar1->RemoveAllBoldedDates();  
    ```  
  
2.  Обновить внешний вид шрифта, вызвав <xref:System.Windows.Forms.MonthCalendar.UpdateBoldedDates%2A> метод.  
  
    ```vb  
    MonthCalendar1.UpdateBoldedDates()  
    ```  
  
    ```csharp  
    monthCalendar1.UpdateBoldedDates();  
    ```  
  
    ```cpp  
    monthCalendar1->UpdateBoldedDates();  
    ```  
  
## <a name="see-also"></a>См. также
- [Элемент управления MonthCalendar](../../../../docs/framework/winforms/controls/monthcalendar-control-windows-forms.md)
- [Практическое руководство. Выбор диапазона дат в элементе управления Windows Forms MonthCalendar](../../../../docs/framework/winforms/controls/how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control.md)
- [Практическое руководство. Изменение внешнего вида управления Windows Forms MonthCalendar](../../../../docs/framework/winforms/controls/how-to-change-monthcalendar-control-appearance.md)
- [Практическое руководство. Отображение более чем одного месяца в элементе управления Windows Forms MonthCalendar](../../../../docs/framework/winforms/controls/display-more-than-one-month-wf-monthcalendar-control.md)
