---
title: "Метод IAssemblyName::GetProperty"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyName.GetProperty
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyName::GetProperty
helpviewer_keywords:
- IAssemblyName::GetProperty method [.NET Framework fusion]
- GetProperty method [.NET Framework fusion]
ms.assetid: e59fda62-77d5-4e37-89cb-ce7ae4627975
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6eae7cf2d6dabe9bad4912d6a97249f52464fe65
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="iassemblynamegetproperty-method"></a><span data-ttu-id="3b174-102">Метод IAssemblyName::GetProperty</span><span class="sxs-lookup"><span data-stu-id="3b174-102">IAssemblyName::GetProperty Method</span></span>
<span data-ttu-id="3b174-103">Возвращает указатель на свойство ссылается указанный идентификатор свойства.</span><span class="sxs-lookup"><span data-stu-id="3b174-103">Gets a pointer to the property referenced by the specified property identifier.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3b174-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b174-104">Syntax</span></span>  
  
```  
HRESULT GetProperty (  
    [in]      DWORD    PropertyId,  
    [out]     LPVOID   pvProperty,  
    [in, out] LPDWORD  pcbProperty  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3b174-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b174-105">Parameters</span></span>  
 `PropertyId`  
 <span data-ttu-id="3b174-106">[in] Уникальный идентификатор для запрашиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="3b174-106">[in] The unique identifier for the requested property.</span></span>  
  
 `pvProperty`  
 <span data-ttu-id="3b174-107">[out] Данные возвращаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="3b174-107">[out] The returned property data.</span></span>  
  
 `pcbProperty`  
 <span data-ttu-id="3b174-108">[in, out] Размер в байтах для `pvProperty`.</span><span class="sxs-lookup"><span data-stu-id="3b174-108">[in, out] The size, in bytes, of `pvProperty`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b174-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3b174-109">Requirements</span></span>  
 <span data-ttu-id="3b174-110">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3b174-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b174-111">**Заголовок:** Fusion.h</span><span class="sxs-lookup"><span data-stu-id="3b174-111">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="3b174-112">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b174-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b174-113">См. также</span><span class="sxs-lookup"><span data-stu-id="3b174-113">See Also</span></span>  
 [<span data-ttu-id="3b174-114">IAssemblyName-интерфейс</span><span class="sxs-lookup"><span data-stu-id="3b174-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)