---
title: Метод ICorDebugNativeFrame::GetIP
ms.date: 03/30/2017
api_name:
- ICorDebugNativeFrame.GetIP
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugNativeFrame::GetIP
helpviewer_keywords:
- GetIP method, ICorDebugNativeFrame interface [.NET Framework debugging]
- ICorDebugNativeFrame::GetIP method [.NET Framework debugging]
ms.assetid: 99f693f3-d3b9-4fd8-9d09-b8efd03f7b67
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3a27a50e6fb120e537d28759a79a2b90c6d437e4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54600457"
---
# <a name="icordebugnativeframegetip-method"></a>Метод ICorDebugNativeFrame::GetIP
Получает расположение, к которому в настоящее время задать указатель инструкций смещения в машинном коде.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT GetIP (  
    [out] ULONG32           *pnOffset  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `pnOffset`  
 [out] Указатель на расположение смещения в машинном коде.  
  
## <a name="remarks"></a>Примечания  
 Если кадр стека, представленного «ICorDebugNativeFrame» активен, значением offset является адрес следующую инструкцию для выполнения. Если данный кадр стека не активен, смещение является адресом следующую инструкцию для выполнения при повторной активации кадра стека.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** CorDebug.idl, CorDebug.h  
  
 **Библиотека:** CorGuids.lib  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также

