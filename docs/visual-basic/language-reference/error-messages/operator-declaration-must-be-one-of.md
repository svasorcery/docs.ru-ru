---
title: 'Объявлении оператора должен быть одним из: +,-, *,-, -, ^, &amp;, например, Mod и, Or, Xor, не, &lt; &lt;, &gt; &gt;, =, &lt; &gt;, &lt;, &lt;=, &gt; , &gt;=, CType, IsTrue, IsFalse'
ms.date: 07/20/2015
f1_keywords:
- bc33000
- vbc33000
helpviewer_keywords:
- BC33000
ms.assetid: 15c5d8eb-3a8c-4141-8f41-33151afabf97
ms.openlocfilehash: f32935dd4aaccd3040655b418badc13c1988c1b8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54622277"
---
# <a name="operator-declaration-must-be-one-of----amp-like-mod-and-or-xor-not-ltlt-gtgt"></a>Объявлении оператора должен быть одним из: +,-, *,\,/, ^, &amp;, например, Mod и, Or, Xor, не, &lt; &lt;, &gt; &gt;...
Можно объявить только оператор, который подходит для перегрузки. В следующей таблице перечислены операторы, которые можно объявить.  
  
|Тип|Операторы|  
|----------|---------------|  
|Унарный|`+`, `-`, `IsFalse`, `IsTrue`, `Not`|  
|Binary|`+`, `-`, `*`, `/`, `\`, `&`, `^`, `>>`, `<<`, `=`, `<>`, `>`, `>=`, `<`, `<=`, `And`, `Like`, `Mod`, `Or`, `Xor`|  
|Преобразование (унарный)|`CType`|  
  
 Обратите внимание, что `=` оператор в списке бинарных операторов является оператором сравнения, не оператором присваивания.  
  
 **Идентификатор ошибки:** BC33000  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
1.  Выберите оператор из набора перегружаемых операторов.  
  
2.  Если требуется возможность перегрузки оператора, который нельзя перегрузить непосредственно, создайте процедуру `Function` , которая принимает соответствующие параметры и возвращает соответствующее значение.  
  
## <a name="see-also"></a>См. также
- [Оператор Statement](../../../visual-basic/language-reference/statements/operator-statement.md)
- [Процедуры операторов](../../../visual-basic/programming-guide/language-features/procedures/operator-procedures.md)
- [Практическое руководство. Определение оператора](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-an-operator.md)
- [Практическое руководство. Определение оператора преобразования](../../../visual-basic/programming-guide/language-features/procedures/how-to-define-a-conversion-operator.md)
- [Оператор Function](../../../visual-basic/language-reference/statements/function-statement.md)
