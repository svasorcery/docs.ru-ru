---
title: Как выполнить Возвращение значения из процедуры (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- procedures [Visual Basic], returning from
- procedures [Visual Basic], returning a value
ms.assetid: 4bcc4724-2b4e-4df8-9b4b-16054607f87d
ms.openlocfilehash: 38b0673f5725077eec9253021eec4216e66504a2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54615261"
---
# <a name="how-to-return-a-value-from-a-procedure-visual-basic"></a>Как выполнить Возвращение значения из процедуры (Visual Basic)
Объект `Function` процедура возвращает значение вызывающему коду, выполнив `Return` инструкции или путем добавления `Exit Function` или `End Function` инструкции.  
  
### <a name="to-return-a-value-using-the-return-statement"></a>Для возврата значения с помощью инструкции Return  
  
1.  Поместите `Return` инструкции в точке, где процедуры завершения.  
  
2.  Выполните `Return` ключевое слово с выражением, возвращающего значение, который необходимо вернуть вызывающему коду.  
  
3.  В одной и той же процедуре можно использовать несколько операторов `Return`.  
  
     Следующие `Function` процедура рассчитывается самая длинная сторона, гипотенуза прямоугольного треугольника и возвращает его вызывающему коду.  
  
     [!code-vb[VbVbcnProcedures#1](./codesnippet/VisualBasic/how-to-return-a-value-from-a-procedure_1.vb)]  
  
     В следующем примере показано типичный вызов `hypotenuse`, который сохраняет возвращаемое значение.  
  
     [!code-vb[VbVbcnProcedures#6](./codesnippet/VisualBasic/how-to-return-a-value-from-a-procedure_2.vb)]  
  
### <a name="to-return-a-value-using-exit-function-or-end-function"></a>Для возврата значения с помощью Exit Function или End Function  
  
1.  В по крайней мере в одном месте в `Function` процедуры, назначить значение для имени процедуры.  
  
2.  При выполнении `Exit Function` или `End Function` инструкция, Visual Basic возвращает наиболее недавно значение имени процедуры.  
  
3.  В одной и той же процедуре можно использовать несколько операторов `Exit Function` и одновременно использовать операторы `Return` и `Exit Function`.  
  
4.  Может иметь только один `End Function` инструкции в `Function` процедуры.  
  
     Дополнительные сведения и пример см. в разделе «Возвращают значение» в [инструкции Function](../../../../visual-basic/language-reference/statements/function-statement.md).  
  
## <a name="see-also"></a>См. также
- [Процедуры](./index.md)
- [Подпрограммы](./sub-procedures.md)
- [Процедуры свойств](./property-procedures.md)
- [Процедуры операторов](./operator-procedures.md)
- [Параметры и аргументы процедуры](./procedure-parameters-and-arguments.md)
- [Оператор Function](../../../../visual-basic/language-reference/statements/function-statement.md)
- [Оператор Return](../../../../visual-basic/language-reference/statements/return-statement.md)
- [Практическое руководство. Создание процедуры, возвращающей значение](./how-to-create-a-procedure-that-returns-a-value.md)
- [Практическое руководство. Вызов процедуры, возвращающей значение](./how-to-call-a-procedure-that-returns-a-value.md)
