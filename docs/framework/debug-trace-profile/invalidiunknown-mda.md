---
title: Помощник по отладке управляемого кода invalidIUnknown
ms.date: 03/30/2017
helpviewer_keywords:
- MDAs (managed debugging assistants), invalid IUnknown pointer
- InvalidIUnknown MDA
- invalid IUnknown pointers
- IUnknown pointers
- managed debugging assistants (MDAs), invalid IUnknown pointer
ms.assetid: c7924771-a16b-40fe-b337-ce51dcdf6a12
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5fead50c42c0d686492459829f7629654c20a0f3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54582673"
---
# <a name="invalidiunknown-mda"></a>Помощник по отладке управляемого кода invalidIUnknown
Помощник по отладке управляемого кода (MDA) `invalidIUnknown` активируется, когда недопустимый указатель `IUnknown` передается в управляемый код из машинного кода. `IUnknown` не удалось возвратить успех при запросе для интерфейса `IUnknown`.  
  
## <a name="symptoms"></a>Признаки  
 Непредвиденная ошибка при маршалинге указателя интерфейса СОМ во время маршалинга аргумента.  
  
## <a name="cause"></a>Причина  
 Неверная реализация `QueryInterface` в интерфейсе COM, переданном в среду CLR.  
  
## <a name="resolution"></a>Решение  
 Исправьте реализацию `QueryInterface`.  
  
## <a name="effect-on-the-runtime"></a>Влияние на среду выполнения  
 Этот помощник отладки управляемого кода не оказывает никакого влияния на среду CLR.  
  
## <a name="output"></a>Вывод  
 Описание ошибки  
  
## <a name="configuration"></a>Конфигурация  
  
```xml  
<mdaConfig>  
  <assistants>  
    <invalidIUnknown />  
  </assistants>  
</mdaConfig>  
```  
  
## <a name="see-also"></a>См. также
- <xref:System.Runtime.InteropServices.MarshalAsAttribute>
- [Диагностика ошибок посредством помощников по отладке управляемого кода](../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)
- [Маршалинг взаимодействия](../../../docs/framework/interop/interop-marshaling.md)
