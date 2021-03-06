---
title: Предложение Skip While (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.QuerySkipWhile
helpviewer_keywords:
- Skip While statement [Visual Basic]
- Skip While clause [Visual Basic]
- queries [Visual Basic], Skip While
ms.assetid: 5dee8350-7520-4f1a-b00d-590cacd572d6
ms.openlocfilehash: 7da5f50a9d0fa867244a569e03685cc637bf3ce6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54692523"
---
# <a name="skip-while-clause-visual-basic"></a>Предложение Skip While (Visual Basic)
Пропускает элементы в коллекции, если заданное условие имеет значение `true`, и возвращает остальные элементы.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
Skip While expression  
```  
  
## <a name="parts"></a>Части  
  
|Термин|Определение|  
|---|---|  
|`expression`|Обязательный. Выражение, которое представляет условие для проверки элементов. Выражение должно возвращать `Boolean` значение или функциональный эквивалент, например `Integer` для оценки в качестве `Boolean`.|  
  
## <a name="remarks"></a>Примечания  
 `Skip While` Предложение пропускает элементы в начале результатов запроса до предоставленного `expression` возвращает `false`. После `expression` возвращает `false`, запрос возвращает все оставшиеся элементы. `expression` Игнорируется для оставшихся результатов.  
  
 `Skip While` Предложение отличается от `Where` предложение, в который `Where` предложение может использоваться для исключения всех элементов из запроса, который не удовлетворяют определенному условию. `Skip While` Предложение исключает элементы только до момента первого, условие не выполняется. `Skip While` Предложение наиболее полезно при работе с упорядоченным результатом запроса.  
  
 Можно пропустить определенное количество результатов в начале результата запроса с помощью `Skip` предложение.  
  
## <a name="example"></a>Пример  
 В следующем примере кода используется `Skip While` предложение для обхода результатов, пока не будет найдено первого заказчика из США.  
  
 [!code-vb[VbSimpleQuerySamples#3](../../../visual-basic/language-reference/queries/codesnippet/VisualBasic/skip-while-clause_1.vb)]  
  
## <a name="see-also"></a>См. также
- [Introduction to LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md) (Знакомство с LINQ в Visual Basic)
- [Запросы](../../../visual-basic/language-reference/queries/index.md)
- [Предложение Select](../../../visual-basic/language-reference/queries/select-clause.md)
- [Предложение From](../../../visual-basic/language-reference/queries/from-clause.md)
- [Предложение Skip](../../../visual-basic/language-reference/queries/skip-clause.md)
- [Предложение Take While](../../../visual-basic/language-reference/queries/take-while-clause.md)
- [Предложения Where](../../../visual-basic/language-reference/queries/where-clause.md)
