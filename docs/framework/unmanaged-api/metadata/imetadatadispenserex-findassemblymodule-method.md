---
title: Метод IMetaDataDispenserEx::FindAssemblyModule
ms.date: 03/30/2017
api_name:
- IMetaDataDispenserEx.FindAssemblyModule
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataDispenserEx::FindAssemblyModule
helpviewer_keywords:
- FindAssemblyModule method [.NET Framework metadata]
- IMetaDataDispenserEx::FindAssemblyModule method [.NET Framework metadata]
ms.assetid: d1fb65e1-7e19-4513-85b1-44f87c294d3e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 3ae455aeba353cfa66a1253b580e15b280caec8d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54584104"
---
# <a name="imetadatadispenserexfindassemblymodule-method"></a>Метод IMetaDataDispenserEx::FindAssemblyModule
Этот метод не реализован. При вызове, он возвращает E_NOTIMPL.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT FindAssemblyModule(  
    [in]  LPCWSTR  szAppBase,  
    [in]  LPCWSTR  szPrivateBin,  
    [in]  LPCWSTR  szGlobalBin,  
    [in]  LPCWSTR  szAssemblyName,  
    [in]  LPCWSTR  szModuleName,  
    [out] LPCWSTR  szName,  
    [in]  ULONG    cchName,  
    [out] ULONG    *pcName  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `szAppBase`  
 [in] Не используется.  
  
 `szPrivateBin`  
 [in] Не используется.  
  
 `szGlobalBin`  
 [in] Не используется.  
  
 `szAssemblyName`  
 [in] Имя модуля.  
  
 `szModuleName`  
 [in] Сборки, который требуется найти.  
  
 `szName`  
 [out] Простое имя сборки.  
  
 `cchName`  
 [in] Размер в байтах из `szName`.  
  
 `pcName`  
 [out] Число символов, фактически возвращенных в `szName`.  
  
## <a name="requirements"></a>Требования  
 **Платформа:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** Cor.h  
  
 **Библиотека:** Используется как ресурс в MsCorEE.dll  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейс IMetaDataDispenserEx](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenserex-interface.md)
- [Интерфейс IMetaDataDispenser](../../../../docs/framework/unmanaged-api/metadata/imetadatadispenser-interface.md)
