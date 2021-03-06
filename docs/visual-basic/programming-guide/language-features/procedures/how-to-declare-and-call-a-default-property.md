---
title: Как выполнить Объявление и вызов свойства по умолчанию в Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- defaults [Visual Basic], properties
- properties [Visual Basic], default
- procedures [Visual Basic], defining
- default properties [Visual Basic], in Visual Basic
- Visual Basic code, procedures
- Visual Basic code, properties
- default properties
ms.assetid: 68b4026e-09ef-4613-808e-f6287494ff63
ms.openlocfilehash: ca282acbe6831f2189d83faa2f83d32d420d9b53
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640970"
---
# <a name="how-to-declare-and-call-a-default-property-in-visual-basic"></a>Как выполнить Объявление и вызов свойства по умолчанию в Visual Basic
Объект *свойство по умолчанию* — это свойство класса или структуры, которое ваш код может получить доступ без указания его. Если вызывающий код задает класс или структуру, но не свойство и контекст разрешает доступ к свойству, Visual Basic разрешает доступ для этого класса или структуры свойство по умолчанию, если он существует.  
  
 Класс или структура может иметь не более одного свойства по умолчанию. Тем не менее можно перегружать свойство по умолчанию и иметь более одной версии.  
  
 Дополнительные сведения см. в разделе [по умолчанию](../../../../visual-basic/language-reference/modifiers/default.md).  
  
### <a name="to-declare-a-default-property"></a>Чтобы объявить свойство по умолчанию  
  
1.  Объявите свойство обычным способом. Не указывайте `Shared` или `Private` ключевое слово.  
  
2.  Включить `Default` ключевое слово в объявлении свойства.  
  
3.  Укажите хотя бы один параметр для свойства. Нельзя определить свойство по умолчанию, которая не принимает хотя бы один аргумент.  
  
     [!code-vb[VbVbcnProcedures#17](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_1.vb)]  
  
### <a name="to-call-a-default-property"></a>Чтобы вызвать свойство по умолчанию  
  
1.  Объявите переменную типа содержащего класса или структуры.  
  
     [!code-vb[VbVbcnProcedures#16](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_2.vb)]  
  
2.  Используйте имя переменной отдельно в выражении, где вы обычно содержит имя свойства.  
  
     [!code-vb[VbVbcnProcedures#21](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_3.vb)]  
  
3.  После имени переменной список аргументов в скобках. Свойство по умолчанию необходимо выполнить хотя бы один аргумент.  
  
     [!code-vb[VbVbcnProcedures#20](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_4.vb)]  
  
4.  Чтобы получить значение свойства по умолчанию, используйте имя переменной, списку аргументов в выражении или после равенства (`=`) войдите в операторе присваивания.  
  
     [!code-vb[VbVbcnProcedures#15](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_5.vb)]  
  
5.  Чтобы задать значение свойства по умолчанию, используйте имя переменной со списком аргументов, в левой части оператора присваивания.  
  
     [!code-vb[VbVbcnProcedures#14](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_6.vb)]  
  
6.  Всегда можно указать имя свойства по умолчанию, а также имя переменной, так же, как это делается для доступа к любому другому свойству.  
  
     [!code-vb[VbVbcnProcedures#19](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_7.vb)]  
  
## <a name="example"></a>Пример  
 В следующем примере объявляется свойство по умолчанию для класса.  
  
 [!code-vb[VbVbcnProcedures#12](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_8.vb)]  
  
## <a name="example"></a>Пример  
 Следующий пример демонстрирует вызов свойства по умолчанию `myProperty` класса `class1`. Три оператора присваивания сохраняют значения в `myProperty`и <xref:Microsoft.VisualBasic.Interaction.MsgBox%2A> вызов считывает значения.  
  
 [!code-vb[VbVbcnProcedures#13](./codesnippet/VisualBasic/how-to-declare-and-call-a-default-property_9.vb)]  
  
 Наиболее распространенное использование свойства по умолчанию является <xref:Microsoft.VisualBasic.Collection.Item%2A> свойство для различных классов коллекций.  
  
## <a name="robust-programming"></a>Отказоустойчивость  
 Свойства по умолчанию может привести к небольшому сокращению символы исходного кода, но они могут сделать код более трудным для чтения. Если вызывающий код не знакомы с класса или структуры, когда он ссылается на имя класса или структуры, он не может быть определенные ли такая ссылка обращается к классу или структуре или свойство по умолчанию. Это может привести к ошибкам компилятора или ошибки слабая логики времени выполнения.  
  
 Отчасти можно уменьшить вероятность возникновения ошибки свойства по умолчанию, используя [оператор Option Strict](../../../../visual-basic/language-reference/statements/option-strict-statement.md) тип компилятора, проверки для `On`.  
  
 Если вы планируете использовать предварительно определенный класс или структура в коде, необходимо определить, имеет ли он свойство по умолчанию и если да, что ее имя —.  
  
 Из-за эти недостатки можно не определять свойства по умолчанию. Для удобства чтения кода следует также учитывать всегда относятся ко всем свойствам явным образом, даже свойства по умолчанию.  
  
## <a name="see-also"></a>См. также
- [Процедуры свойств](./property-procedures.md)
- [Параметры и аргументы процедуры](./procedure-parameters-and-arguments.md)
- [Оператор Property](../../../../visual-basic/language-reference/statements/property-statement.md)
- [Default](../../../../visual-basic/language-reference/modifiers/default.md)
- [Различия между свойствами и переменными в Visual Basic](./differences-between-properties-and-variables.md)
- [Практическое руководство. Создать свойство](./how-to-create-a-property.md)
- [Практическое руководство. Объявление свойства со смешанным уровнем доступа](./how-to-declare-a-property-with-mixed-access-levels.md)
- [Практическое руководство. Вызов процедуры свойства](./how-to-call-a-property-procedure.md)
- [Практическое руководство. Запись значения в свойство](./how-to-put-a-value-in-a-property.md)
- [Практическое руководство. Получение значения из свойства](./how-to-get-a-value-from-a-property.md)
