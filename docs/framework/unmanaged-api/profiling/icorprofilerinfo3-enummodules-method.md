---
title: "Метод ICorProfilerInfo3::EnumModules"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo3.EnumModules Method
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo3::EnumModules
helpviewer_keywords:
- ICorProfilerInfo3::EnumModules method [.NET Framework profiling]
- EnumModules method [.NET Framework profiling]
ms.assetid: 1bf00b42-69da-4019-91b3-bf88026e83fb
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: aac765ae29e567965cd90fc9e165d303cc3fa866
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo3enummodules-method"></a><span data-ttu-id="357f1-102">Метод ICorProfilerInfo3::EnumModules</span><span class="sxs-lookup"><span data-stu-id="357f1-102">ICorProfilerInfo3::EnumModules Method</span></span>
<span data-ttu-id="357f1-103">Возвращает перечислитель, предоставляющий методы для последовательного перебора коллекции управляемых модулей, загруженных в приложение.</span><span class="sxs-lookup"><span data-stu-id="357f1-103">Returns an enumerator that provides methods to sequentially iterate through a collection of managed modules that are loaded into the application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="357f1-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="357f1-104">Syntax</span></span>  
  
```  
HRESULT EnumModules([out] ICorProfilerModuleEnum** ppEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="357f1-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="357f1-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="357f1-106">[out] Указатель на [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="357f1-106">[out] A pointer to an [ICorProfilerModuleEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilermoduleenum-interface.md) interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="357f1-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="357f1-107">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="357f1-108">Требования</span><span class="sxs-lookup"><span data-stu-id="357f1-108">Requirements</span></span>  
 <span data-ttu-id="357f1-109">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="357f1-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="357f1-110">**Заголовок:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="357f1-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="357f1-111">**Библиотека:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="357f1-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="357f1-112">**Версии платформы .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="357f1-112">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="357f1-113">См. также</span><span class="sxs-lookup"><span data-stu-id="357f1-113">See Also</span></span>  
 [<span data-ttu-id="357f1-114">ICorProfilerFunctionEnum-интерфейс</span><span class="sxs-lookup"><span data-stu-id="357f1-114">ICorProfilerFunctionEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerfunctionenum-interface.md)  
 [<span data-ttu-id="357f1-115">Интерфейс ICorProfilerInfo3</span><span class="sxs-lookup"><span data-stu-id="357f1-115">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)  
 [<span data-ttu-id="357f1-116">Интерфейсы профилирования</span><span class="sxs-lookup"><span data-stu-id="357f1-116">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="357f1-117">Профилирование</span><span class="sxs-lookup"><span data-stu-id="357f1-117">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)