---
title: Пошаговое руководство. Создание пользовательского типа блока потока данных
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Task Parallel Library, dataflows
- TPL dataflow library, creating custom dataflow blocks
- dataflow blocks, creating custom in TPL
ms.assetid: a6147146-0a6a-4d9b-ab0f-237b3c1ac691
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 380bcb6d2a2846d09267eeb3a0d637469ce9fba5
ms.sourcegitcommit: a36cfc9dbbfc04bd88971f96e8a3f8e283c15d42
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "54221093"
---
# <a name="walkthrough-creating-a-custom-dataflow-block-type"></a>Пошаговое руководство. Создание пользовательского типа блока потока данных
Хотя библиотека потоков данных предоставляет несколько типов блоков потоков данных, которые позволяют использовать различные функции, можно также создавать пользовательские типы блоков. В этом документе описано, как создать тип блока потока данных, который реализует пользовательское поведение.  
  
## <a name="prerequisites"></a>Предварительные требования  
 Ознакомьтесь с руководством по [потокам данных](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md), прежде чем читать этот документ.  

[!INCLUDE [tpl-install-instructions](../../../includes/tpl-install-instructions.md)]
  
## <a name="defining-the-sliding-window-dataflow-block"></a>Определение блока потока данных скользящего окна  
 Рассмотрим приложение потока данных, которое требует, чтобы входные значения были буферизованы и затем выводились по принципу скользящего окна. Например, для входных значений {0, 1, 2, 3, 4, 5} и размера окна 3, блок потока данных скользящего окна создает массивы вывода {0, 1, 2}, {1, 2, 3}, {2, 3, 4} и {3, 4, 5}. В следующих разделах описываются два способа создания типа блока потока данных, который реализует это пользовательское поведение. В первом способе используется метод <xref:System.Threading.Tasks.Dataflow.DataflowBlock.Encapsulate%2A> для объединения возможностей объекта <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601> и объекта <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601> в одном блоке распространения. Второй способ определяет класс, производный от <xref:System.Threading.Tasks.Dataflow.IPropagatorBlock%602>, и объединяет существующие функциональные возможности для обеспечения пользовательского поведения.  
  
## <a name="using-the-encapsulate-method-to-define-the-sliding-window-dataflow-block"></a>Использование метода инкапсуляции для определения блока потока данных скользящего окна  
 В следующем примере используется метод <xref:System.Threading.Tasks.Dataflow.DataflowBlock.Encapsulate%2A> для создания блока распространения из источника и целевого объекта. Блок распространения позволяет блокам источника и целевого объекта действовать в качестве отправителя и получателя данных.  
  
 Этот способ полезен, когда требуется пользовательская функциональность потока данных, но нет необходимости в типе, который предоставляет дополнительные методы, свойства или поля.  
  
 [!code-csharp[TPLDataflow_SlidingWindowBlock#1](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_slidingwindowblock/cs/slidingwindowblock.cs#1)]
 [!code-vb[TPLDataflow_SlidingWindowBlock#1](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_slidingwindowblock/vb/slidingwindowblock.vb#1)]  
  
## <a name="deriving-from-ipropagatorblock-to-define-the-sliding-window-dataflow-block"></a>Наследование от IPropagatorBlock для определения блока потока данных скользящего окна  
 В следующем примере демонстрируется класс `SlidingWindowBlock`. Этот класс является производным от <xref:System.Threading.Tasks.Dataflow.IPropagatorBlock%602>, поэтому способен действовать и как источник, и как целевой объект данных. Как и в предыдущем примере, класс `SlidingWindowBlock` создается на основе существующих типов блоков потока данных. Однако класс `SlidingWindowBlock` также реализует методы, необходимые для интерфейсов <xref:System.Threading.Tasks.Dataflow.ISourceBlock%601>, <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601> и <xref:System.Threading.Tasks.Dataflow.IDataflowBlock>. Все эти методы переадресуют работу членам предопределенных типов блоков потока данных. Например, метод `Post` передает работу данным-члену `m_target`, также являющемуся объектом <xref:System.Threading.Tasks.Dataflow.ITargetBlock%601>.  
  
 Этот способ полезен, когда требуется пользовательская функциональность потока данных и тип, который предоставляет дополнительные методы, свойства или поля. Например, класс `SlidingWindowBlock` также является производным от <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601>, чтобы он мог предоставлять методы <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601.TryReceive%2A> и <xref:System.Threading.Tasks.Dataflow.IReceivableSourceBlock%601.TryReceiveAll%2A>. Класс `SlidingWindowBlock` также демонстрирует расширяемость, предоставляя свойство `WindowSize`, которое возвращает количество элементов в скользящем окне.  
  
 [!code-csharp[TPLDataflow_SlidingWindowBlock#2](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_slidingwindowblock/cs/slidingwindowblock.cs#2)]
 [!code-vb[TPLDataflow_SlidingWindowBlock#2](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_slidingwindowblock/vb/slidingwindowblock.vb#2)]  
  
## <a name="the-complete-example"></a>Полный пример  
 В следующем примере приведен полный код для этого руководства. Здесь также показано, как использовать оба блока скользящего окна в методе, который записывает в блок, считывает из него и выводит результаты на консоль.  
  
 [!code-csharp[TPLDataflow_SlidingWindowBlock#100](../../../samples/snippets/csharp/VS_Snippets_Misc/tpldataflow_slidingwindowblock/cs/slidingwindowblock.cs#100)]
 [!code-vb[TPLDataflow_SlidingWindowBlock#100](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpldataflow_slidingwindowblock/vb/slidingwindowblock.vb#100)]  
  
## <a name="compiling-the-code"></a>Компиляция кода  
 Скопируйте код примера и вставьте его в проект Visual Studio или в файл с именем `SlidingWindowBlock.cs` (`SlidingWindowBlock.vb` для Visual Basic), затем выполните в окне командной строки разработчика для Visual Studio следующую команду.  
  
 Visual C#  
  
 **csc.exe /r:System.Threading.Tasks.Dataflow.dll SlidingWindowBlock.cs**  
  
 Visual Basic  
  
 **vbc.exe /r:System.Threading.Tasks.Dataflow.dll SlidingWindowBlock.vb**  

## <a name="see-also"></a>См. также

- [Поток данных](../../../docs/standard/parallel-programming/dataflow-task-parallel-library.md)
