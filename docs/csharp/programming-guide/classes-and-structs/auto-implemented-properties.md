---
title: Руководство по программированию на C#. Автоматически реализуемые свойства
ms.custom: seodec18
ms.date: 07/20/2015
helpviewer_keywords:
- auto-implemented properties [C#]
- properties [C#], auto-implemented
ms.assetid: aa55fa97-ccec-431f-b5e9-5ac789fd32b7
ms.openlocfilehash: ef9243498f3f97e560e45c389932ff57e1e4eef7
ms.sourcegitcommit: deb9225a55485a5a6e6c7914deb30ccfceb69d3f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2019
ms.locfileid: "54058520"
---
# <a name="auto-implemented-properties-c-programming-guide"></a>Автоматически реализуемые свойства (Руководство по программированию на C#)
В C# 3.0 и более поздних версиях автоматически реализуемые свойства делают объявление свойств более лаконичным, когда в методах доступа к свойствам не требуется дополнительная логика. Они также позволяют клиентскому коду создавать объекты. При объявлении свойства, как показано в следующем примере, компилятор создает закрытое анонимное резервное поле, которое может быть доступно только через методы доступа `get` и `set` свойства.  
  
## <a name="example"></a>Пример  
 В следующем примере показан простой класс, имеющий несколько автоматически реализуемых свойств.  
  
 [!code-csharp[csProgGuideLINQ#28](../../../csharp/programming-guide/arrays/codesnippet/CSharp/auto-implemented-properties_1.cs)]  
  
 В C# 6 и более поздних версиях можно инициализировать автоматически реализуемые свойства аналогично полям.  
  
```csharp  
public string FirstName { get; set; } = "Jane";  
```  
  
 Класс, который показан в предыдущем примере, является изменяемым. Клиентский код может изменить значения в объектах после их создания. В сложных классах, которые содержат значительные возможности (методы) и данные, часто необходимо иметь открытые свойства. Однако для небольших классов или структур, которые просто инкапсулируют набор значений (данных) и имеют мало функциональных возможностей или совсем их не имеют, вы должны сделать объекты неизменяемыми либо путем объявления метода доступа set как [закрытого](../../../csharp/language-reference/keywords/private.md) (неизменяемого для потребителей), либо путем объявления только метода доступа get (неизменяемого везде, кроме конструктора).  Дополнительные сведения см. в разделе [Как реализации облегченного класса с автоматически реализуемыми свойствами](../../../csharp/programming-guide/classes-and-structs/how-to-implement-a-lightweight-class-with-auto-implemented-properties.md).  
  
## <a name="see-also"></a>См. также раздел

- [Свойства](../../../csharp/programming-guide/classes-and-structs/properties.md)  
- [Модификаторы](../../../csharp/language-reference/keywords/modifiers.md)
