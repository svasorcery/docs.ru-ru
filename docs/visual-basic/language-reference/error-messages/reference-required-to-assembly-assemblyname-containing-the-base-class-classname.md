---
title: Требуется ссылка на сборку &#39; &lt;assemblyname&gt; &#39; содержащую базовый класс &#39; &lt;classname&gt;&#39;
ms.date: 07/20/2015
f1_keywords:
- bc30007
- vbc30007
helpviewer_keywords:
- BC30007
ms.assetid: 5f34cf47-6c6e-4954-bd8e-d6b020b75fb7
ms.openlocfilehash: f2aa8f1f05ce15bd25992b7f1851854952108813
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54506284"
---
# <a name="reference-required-to-assembly-39ltassemblynamegt39-containing-the-base-class-39ltclassnamegt39"></a>Требуется ссылка на сборку &#39; &lt;assemblyname&gt; &#39; содержащую базовый класс &#39; &lt;classname&gt;&#39;
Требуется ссылка на сборку "\<имя_сборки >" содержит базовый класс\<имя_класса > ". Добавьте эту ссылку в проект.  
  
 Класс определяется в библиотеке динамической компоновки (DLL) или в сборке, на которую в проекте нет прямой ссылки. Компилятор Visual Basic требует ссылку, чтобы исключить неоднозначность в случае, если класс определен в нескольких библиотеках DLL или сборках.  
  
 **Идентификатор ошибки:** BC30007  
  
## <a name="to-correct-this-error"></a>Исправление ошибки  
  
-   Включите в ссылки проекта имя библиотеки DLL или сборки, на которую нет ссылки.  
  
## <a name="see-also"></a>См. также

- [Управление ссылками в проекте](/visualstudio/ide/managing-references-in-a-project)
- [Диагностика неработающих ссылок](/visualstudio/ide/troubleshooting-broken-references)
