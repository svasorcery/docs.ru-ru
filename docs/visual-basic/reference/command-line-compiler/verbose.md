---
title: -verbose
ms.date: 03/13/2018
helpviewer_keywords:
- verbose compiler option [Visual Basic]
- -verbose compiler option [Visual Basic]
- /verbose compiler option [Visual Basic]
ms.assetid: d1aec0c1-0261-421d-9adc-5b13756100be
ms.openlocfilehash: 7a5dd305d1cc40e57d0f07f383151dc1a965bdda
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54513923"
---
# <a name="-verbose"></a>-verbose
Указывает компилятору создавать подробные сообщения о состоянии и ошибки.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
-verbose[+ | -]  
```  
  
## <a name="arguments"></a>Аргументы  
 `+` &#124; `-`  
 Необязательный параметр. Указание `-verbose` же эффект достигается указанием `-verbose+`, который указывает компилятору выдавать подробные сообщения. Значение по умолчанию для этого параметра — `-verbose-`.  
  
## <a name="remarks"></a>Примечания  
 `-verbose` Отображает сведения о общее количество ошибок, выдаваемых компилятором, сообщает, какие сборки загружаются в модуле и отображает, какие файлы компилируемые.  
  
> [!NOTE]
>  `-verbose` Не доступна из среды разработки Visual Studio; она доступна только при компиляции из командной строки.  
  
## <a name="example"></a>Пример  
 Следующий код компилирует `In.vb` и предписывает компилятору отобразить подробные сведения о состоянии.  
  
```console  
vbc -verbose in.vb  
```  
  
## <a name="see-also"></a>См. также
- [Компилятор Visual Basic с интерфейсом командной строки](../../../visual-basic/reference/command-line-compiler/index.md)
- [Примеры командных строк компиляции](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
