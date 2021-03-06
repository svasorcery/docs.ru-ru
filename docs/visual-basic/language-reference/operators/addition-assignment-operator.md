---
title: Оператор += (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.+=
helpviewer_keywords:
- += operator [Visual Basic]
- assignment statements [Visual Basic], compound
- statements [Visual Basic], compound assignment
- += operator [Visual Basic], appending strings
- compound assignment statements [Visual Basic]
ms.assetid: d3e959f4-85d4-4e47-87c4-77b62335a5b3
ms.openlocfilehash: cfe987929099fc73ba3af9fe92b5871275c5396e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54617555"
---
# <a name="-operator-visual-basic"></a>Оператор += (Visual Basic)
Добавляет значение числового выражения к значению числовой переменной или свойства и присваивает результат переменной или свойству. Можно также использовать для объединения `String` выражение `String` переменная или свойство и назначает полученное значение переменной или свойству.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
variableorproperty += expression  
```  
  
## <a name="parts"></a>Части  
 `variableorproperty`  
 Обязательный. Любой числовой или `String` переменной или свойству.  
  
 `expression`  
 Обязательный. Любой числовой или `String` выражение.  
  
## <a name="remarks"></a>Примечания  
 Элемент, на левой стороне `+=` оператор может быть простой скалярной переменной, свойства или элемента массива. Не может быть переменной или свойству [ReadOnly](../../../visual-basic/language-reference/modifiers/readonly.md).  
  
 `+=` Оператор добавляет значение справа переменной или свойству слева от него и присваивает результат переменной или свойству слева от него. `+=` Оператор может также использоваться для сцепления `String` выражение, право на `String` переменной или свойства на слева и назначает полученное значение переменной или свойства слева от него.  
  
> [!NOTE]
>  При использовании `+=` оператора, может не появиться возможность определить, произойдет ли объединение строк или сложение операция. Используйте `&=` для объединения оператор устранения неоднозначности и выполнять код.  
  
 Этот оператор присваивания производит неявное не сужающие преобразования, если среда требует строгую семантику. Дополнительные сведения об этих преобразованиях см. в разделе [Widening and Narrowing Conversions](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md). Дополнительные сведения о строгой и см. в разделе [оператор Option Strict](../../../visual-basic/language-reference/statements/option-strict-statement.md).  
  
 Если разрешено семантика разрешений, `+=` оператор неявно выполняет различные строковые и числовые преобразования, которые идентичны функциям `+` оператор. Дополнительные сведения об этих преобразований, см. в разделе [оператором "+"](../../../visual-basic/language-reference/operators/addition-operator.md).  
  
## <a name="overloading"></a>Перегрузка  
 `+` Оператор может быть *перегружены*, что означает, что класс или структура может переопределить его поведение, если операнд имеет тип этого класса или структуры. Перегрузка `+` оператор влияет на поведение `+=` оператор. Если код использует `+=` для класса или структуры, перегружающей `+`, убедитесь, что его переопределенное. Для получения дополнительной информации см. [Operator Procedures](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md).  
  
## <a name="example"></a>Пример  
 В следующем примере используется `+=` оператор для объединения значений переменной типа с другим. Первая часть использует `+=` для числовых переменных, чтобы добавить одного значения к другому. Вторая часть использует `+=` с `String` переменные для добавления одной строки с другим. В обоих случаях результат назначается первой переменной.  
  
 [!code-vb[VbVbalrOperators#7](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addition-assignment-operator_1.vb)]  
  
 [!code-vb[VbVbalrOperators#8](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/addition-assignment-operator_2.vb)]  
  
 Значение `num1` 13, а значение `str1` становится «103».  
  
## <a name="see-also"></a>См. также
- [Оператор +](../../../visual-basic/language-reference/operators/addition-operator.md)
- [Операторы присваивания](../../../visual-basic/language-reference/operators/assignment-operators.md)
- [Арифметические операторы](../../../visual-basic/language-reference/operators/arithmetic-operators.md)
- [Операторы объединения](../../../visual-basic/language-reference/operators/concatenation-operators.md)
- [Порядок применения операторов в Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Список операторов, сгруппированных по функциональному назначению](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Операторы](../../../visual-basic/programming-guide/language-features/statements.md)
