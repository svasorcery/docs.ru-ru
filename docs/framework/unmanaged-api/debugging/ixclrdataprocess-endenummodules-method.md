---
title: Метод IXCLRDataProcess::EndEnumModules
ms.date: 01/16/2019
api.name:
- IXCLRDataProcess::EndEnumModules Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataProcess::EndEnumModules Method
helpviewer.keywords:
- IXCLRDataProcess::EndEnumModules Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 50ad55674360d7b880af3ddf701cf17005f30ce7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54722742"
---
# <a name="ixclrdataprocessendenummodules-method"></a>Метод IXCLRDataProcess::EndEnumModules

Освобождает ресурсы, используемые внутренней итераторы, используемые при перечислении модуля.

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>Синтаксис
```
HRESULT EndEnumModules(
    [in] CLRDATA_ENUM handle
);
```

### <a name="parameters"></a>Параметры
`handle` [out] Дескриптор для перечисления модули.

## <a name="remarks"></a>Примечания

Указанный метод является частью `IXCLRDataProcess` интерфейса и соответствует 26 слот в таблице виртуального метода.

## <a name="requirements"></a>Требования

**Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).   
**Заголовок.** Нет   
**Библиотека:** Нет   
**Версии платформы .NET Framework:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]   

## <a name="see-also"></a>См. также

- [Отладка](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [Интерфейс IXCLRDataProcess](../../../../docs/framework/unmanaged-api/debugging/ixclrdataprocess-interface.md)
