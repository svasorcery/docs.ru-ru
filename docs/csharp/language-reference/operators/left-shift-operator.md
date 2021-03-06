---
title: Справочник по C#. Оператор &lt;&lt;
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- <<_CSharpKeyword
helpviewer_keywords:
- left shift operator (<<) [C#]
- << operator [C#]
ms.assetid: a654eb56-1ff7-4bf3-9064-b631be0cdccc
ms.openlocfilehash: 79a48d88e2c83b5ad78804367ee3c07f78622c08
ms.sourcegitcommit: 5c36aaa8299a2437c155700c810585aff19edbec
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2019
ms.locfileid: "54333529"
---
# <a name="ltlt-operator-c-reference"></a>Справочник по C#. Оператор &lt;&lt;

Оператор сдвига влево (`<<`) сдвигает первый операнд влево на число битов, задаваемое вторым операндом. Второй операнд должен иметь тип [int](../keywords/int.md) или тип, для которого существует предварительно определенное неявное числовое преобразование в `int`.

## <a name="remarks"></a>Примечания

Если первый операнд имеет тип [int](../keywords/int.md) или [uint](../keywords/uint.md) (32-разрядное число), величина сдвига определяется пятью младшими разрядами второго операнда. Фактическая величина сдвига составляет от 0 до 31 бита.

Если первый операнд имеет тип [long](../keywords/long.md) или [ulong](../keywords/ulong.md) (64-разрядное число), величина сдвига определяется шестью младшими разрядами второго операнда. Фактическая величина сдвига составляет от 0 до 63 битов.

Любые старшие разряды, не попадающие в диапазон значений типа первого операнда после сдвига, отбрасываются, а пустые младшие разряды заполняются нулями. Операции сдвига никогда не вызывают переполнение.

Определяемые пользователем типы могут перегружать оператор `<<` (см. [operator](../keywords/operator.md)). В этом случае первый операнд должен иметь определяемый пользователем тип, а второй операнд — тип `int`. При перегрузке бинарного оператора соответствующий оператор присвоения (если таковой имеется) также неявно перегружается.

## <a name="example"></a>Пример

[!code-csharp[csRefOperators#14](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefOperators/CS/csrefOperators.cs#14)]

## <a name="comments"></a>Комментарии

Обратите внимание, что `i<<1` и `i<<33` дают один и тот же результат, поскольку 1 и 33 имеют одинаковые младшие пять разрядов.

## <a name="see-also"></a>См. также

- [Справочник по C#](../index.md)
- [Руководство по программированию на C#](../../programming-guide/index.md)
- [Операторы в C#](index.md)
