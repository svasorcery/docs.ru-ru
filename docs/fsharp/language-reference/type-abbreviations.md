---
title: "Аббревиатуры типов (F#)"
description: "Дополнительные сведения о аббревиатуры типов F # для предоставления более значимое имя для типа, чтобы сделать код более удобным для чтения."
keywords: "visual f#, f#, функциональное программирование"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 560af74f-935f-415c-af56-604cddb9da6b
ms.openlocfilehash: 235c0240fe89d203b9474dec2b3f91947f453cd8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="type-abbreviations"></a>Сокращенные обозначения типов

Объект *-сокращенная форма типа* — это псевдоним или альтернативное имя для типа.

## <a name="syntax"></a>Синтаксис

```fsharp
type type-abbreviation = type-name
```

## <a name="remarks"></a>Примечания
Сокращенные обозначения типов можно использовать для предоставления типа более значимое имя, чтобы сделать код более удобным для чтения. Их также можно использовать для создания простой в использовании имени типа, в противном случае сложно записать. Кроме того чтобы облегчить изменение базового типа, не изменяя весь код, который использует этот тип можно использовать сокращенные обозначения типов. Ниже приведен пример простой аббревиатуры типа.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2301.fs)]

Сокращенные обозначения типов могут содержать базовые параметры, как показано в следующем коде.

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet2302.fs)]

В приведенном выше коде `Transform` представляет собой сокращенную форму типа, который представляет функцию, которая принимает один аргумент любого типа и возвращает одно значение того же типа.

Сокращенные обозначения типов, не сохраняются в .NET Framework MSIL-код. Таким образом при использовании сборки F # из другого языка .NET Framework, необходимо использовать имя базового типа для сокращенная форма типа.

Сокращенные обозначения типов также может использоваться в единицах измерения. Дополнительные сведения см. в разделе [единицы измерения](units-of-measure.md).


## <a name="see-also"></a>См. также
[Справочник по языку F#](index.md)
