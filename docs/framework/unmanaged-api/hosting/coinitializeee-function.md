---
title: "Функция CoInitializeEE"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CoInitializeEE
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: CoInitializeEE
helpviewer_keywords: CoInitializeEE function [.NET Framework hosting]
ms.assetid: 7e42a928-5068-4ba6-b8c3-806551a01fa8
topic_type: apiref
caps.latest.revision: "15"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 429d055ec0853d04f794b063a76a395d98aceb4f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2017
---
# <a name="coinitializeee-function"></a><span data-ttu-id="34b96-102">Функция CoInitializeEE</span><span class="sxs-lookup"><span data-stu-id="34b96-102">CoInitializeEE Function</span></span>
<span data-ttu-id="34b96-103">Обеспечивает загрузку исполняющий механизм среды выполнения в процесс.</span><span class="sxs-lookup"><span data-stu-id="34b96-103">Ensures that the common language runtime execution engine is loaded into a process.</span></span> <span data-ttu-id="34b96-104">Эта функция устарела в [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="34b96-104">This function is deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="34b96-105">Используйте [ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) метод вместо него.</span><span class="sxs-lookup"><span data-stu-id="34b96-105">Use the [ICLRRuntimeHost::Start](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="34b96-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34b96-106">Syntax</span></span>  
  
```  
HRESULT CoInitializeEE (  
   [in] DWORD fFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="34b96-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34b96-107">Parameters</span></span>  
 `fFlags`  
 <span data-ttu-id="34b96-108">[in] Один из [COINITIEE](../../../../docs/framework/unmanaged-api/metadata/coinitiee-enumeration.md) константы перечисления.</span><span class="sxs-lookup"><span data-stu-id="34b96-108">[in] One of the [COINITIEE](../../../../docs/framework/unmanaged-api/metadata/coinitiee-enumeration.md) enumeration constants.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="34b96-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="34b96-109">Return Value</span></span>  
 <span data-ttu-id="34b96-110">Этот метод возвращает стандартные коды ошибок COM, определенные в файле Winerror.h и значения в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="34b96-110">This method returns standard COM error codes as defined in Winerror.h, and the values in the following table.</span></span>  
  
|<span data-ttu-id="34b96-111">Код возврата</span><span class="sxs-lookup"><span data-stu-id="34b96-111">Return code</span></span>|<span data-ttu-id="34b96-112">Описание</span><span class="sxs-lookup"><span data-stu-id="34b96-112">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="34b96-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="34b96-113">S_OK</span></span>|<span data-ttu-id="34b96-114">Подсистема выполнения была успешно загружена.</span><span class="sxs-lookup"><span data-stu-id="34b96-114">The execution engine was loaded successfully.</span></span>|  
|<span data-ttu-id="34b96-115">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="34b96-115">S_FALSE</span></span>|<span data-ttu-id="34b96-116">Подсистема выполнения уже загружен.</span><span class="sxs-lookup"><span data-stu-id="34b96-116">The execution engine is already loaded.</span></span>|  
|<span data-ttu-id="34b96-117">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="34b96-117">E_FAIL</span></span>|<span data-ttu-id="34b96-118">Не удалось загрузить подсистему выполнения.</span><span class="sxs-lookup"><span data-stu-id="34b96-118">The execution engine could not be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="34b96-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="34b96-119">Remarks</span></span>  
 <span data-ttu-id="34b96-120">Этот метод загружает ядро выполнения, если он не был загружен ранее.</span><span class="sxs-lookup"><span data-stu-id="34b96-120">This method loads the execution engine if it has not been previously loaded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="34b96-121">Требования</span><span class="sxs-lookup"><span data-stu-id="34b96-121">Requirements</span></span>  
 <span data-ttu-id="34b96-122">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="34b96-122">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="34b96-123">**Заголовок:** Cor.h</span><span class="sxs-lookup"><span data-stu-id="34b96-123">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="34b96-124">**Библиотека:** включена как ресурс в MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="34b96-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="34b96-125">**Версии платформы .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="34b96-125">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34b96-126">См. также</span><span class="sxs-lookup"><span data-stu-id="34b96-126">See Also</span></span>  
 [<span data-ttu-id="34b96-127">Глобальные статические функции метаданных</span><span class="sxs-lookup"><span data-stu-id="34b96-127">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)