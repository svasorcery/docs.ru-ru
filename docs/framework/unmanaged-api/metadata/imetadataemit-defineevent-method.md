---
title: Метод IMetaDataEmit::DefineEvent
ms.date: 03/30/2017
api_name:
- IMetaDataEmit.DefineEvent
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::DefineEvent
helpviewer_keywords:
- IMetaDataEmit::DefineEvent method [.NET Framework metadata]
- DefineEvent method [.NET Framework metadata]
ms.assetid: cf064bac-9a9f-41c5-9e1d-108ff7af3afe
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: e7d42fe17af5b10d718d0e2b6a7ae33644fa4813
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54730299"
---
# <a name="imetadataemitdefineevent-method"></a>Метод IMetaDataEmit::DefineEvent
Создает определение события с заданной подписью метаданных и получает маркер для определения событий.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT DefineEvent (   
    [in]  mdTypeDef    td,   
    [in]  LPCWSTR      szEvent,   
    [in]  DWORD        dwEventFlags,   
    [in]  mdToken      tkEventType,   
    [in]  mdMethodDef  mdAddOn,   
    [in]  mdMethodDef  mdRemoveOn,   
    [in]  mdMethodDef  mdFire,   
    [in]  mdMethodDef  rmdOtherMethods[],   
    [out] mdEvent      *pmdEvent   
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `td`  
 [in] Токен для целевого класса или интерфейса. Это может быть либо `mdTypeDef` или `mdTypeDefNil` токена.  
  
 `szEvent`  
 [in] Имя события.  
  
 `dwEventFlags`  
 [in] Флаги событий.  
  
 `tkEventType`  
 [in] Токен для класса событий. Это `mdTypeDef`, `mdTypeRef`, или `mdTokenNil` токена.  
  
 `mdAddOn`  
 [in] Метод, используемый для подписки на событие, или значение null.  
  
 `mdRemoveOn`  
 [in] Метод, используемый для отказа от подписки на событие, или значение null.  
  
 `mdFire`  
 [in] Метод, используемый (с помощью производного класса) для вызова события.  
  
 `rmdOtherMethods[]`  
 [in] Массив маркеров для других методов, связанный с событием. Массив прерывается с выдачей `mdMethodDefNil` токена.  
  
 `pmdEvent`  
 [out] Токен метаданных, присвоенная событию.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** Cor.h  
  
 **Библиотека:** Используется как ресурс в MSCorEE.dll  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейс IMetaDataEmit](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)
- [Интерфейс IMetaDataEmit2](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
