---
title: Метод ICorProfilerInfo2::GetArrayObjectInfo
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetArrayObjectInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetArrayObjectInfo
helpviewer_keywords:
- ICorProfilerInfo2::GetArrayObjectInfo method [.NET Framework profiling]
- GetArrayObjectInfo method [.NET Framework profiling]
ms.assetid: bda75017-739f-4ce5-9000-f3b526e8473c
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: d0444b6a5fd1bb286df573b1bba7d35b0d2d14a7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54498847"
---
# <a name="icorprofilerinfo2getarrayobjectinfo-method"></a>Метод ICorProfilerInfo2::GetArrayObjectInfo
Получает подробные сведения об объекте массива.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT GetArrayObjectInfo(  
    [in] ObjectID objectId,  
    [in] ULONG32 cDimensions,  
    [out, size_is(cDimensions), length_is(cDimensions)] ULONG32 pDimensionSizes[],  
    [out, size_is(cDimensions), length_is(cDimensions)] int pDimensionLowerBounds[],  
    [out] BYTE **ppData);  
```  
  
#### <a name="parameters"></a>Параметры  
 `objectId`  
 [in] Идентификатор объекта допустимым массивом.  
  
 `cDimensions`  
 [in] Ранг (число измерений) массива.  
  
 `pDimensionSizes`  
 [out] Массив, содержащий целые числа, каждый из которых представляет размер измерения массива.  
  
 `pDimensionLowerBounds`  
 [out] Массив, содержащий целые числа, каждый из которых представляет нижняя граница измерения массива.  
  
 `ppData`  
 [out] Указатель на адрес необработанного буфера для массива, который располагается в соответствии с соглашением C++.  
  
## <a name="remarks"></a>Примечания  
 `pDimensionSizes` И `pDimensionLowerBounds` являются параллельными массивами, поэтому характеристики одной сущности, элементы, расположенный в один и тот же индекс в каждом массиве.  
  
## <a name="requirements"></a>Требования  
 **Платформы:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** CorProf.idl, CorProf.h  
  
 **Библиотека:** CorGuids.lib  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейс ICorProfilerInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
- [Интерфейс ICorProfilerInfo2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)
