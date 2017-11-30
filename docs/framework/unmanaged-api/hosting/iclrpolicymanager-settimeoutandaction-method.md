---
title: "Метод ICLRPolicyManager::SetTimeoutAndAction"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRPolicyManager.SetTimeoutAndAction
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRPolicyManager::SetTimeoutAndAction
helpviewer_keywords:
- ICLRPolicyManager::SetTimeoutAndAction method [.NET Framework hosting]
- SetTimeoutAndAction method [.NET Framework hosting]
ms.assetid: 60454f91-d855-4ddf-bb6d-60a02f5eabab
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a15454e1cea29e3c0025797633f22e9e18554347
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="iclrpolicymanagersettimeoutandaction-method"></a><span data-ttu-id="bdfcb-102">Метод ICLRPolicyManager::SetTimeoutAndAction</span><span class="sxs-lookup"><span data-stu-id="bdfcb-102">ICLRPolicyManager::SetTimeoutAndAction Method</span></span>
<span data-ttu-id="bdfcb-103">Задает значение времени ожидания для указанной операции и задает действие политики, которое должен выполнить общеязыковой среды выполнения (CLR), при выполнении этой операции.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-103">Sets a timeout value for the specified operation, and specifies the policy action the common language runtime (CLR) should take when the operation occurs.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bdfcb-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bdfcb-104">Syntax</span></span>  
  
```  
HRESULT SetTimeoutAndAction (  
    [in] EClrOperation operation,  
    [in] DWORD dwMilliseconds,  
    [in] EPolicyAction action  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bdfcb-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bdfcb-105">Parameters</span></span>  
 `operation`  
 <span data-ttu-id="bdfcb-106">[in] Один из [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) значения, указывает, что операция, для которого требуется задать время ожидания и политики `action`.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-106">[in] One of the [EClrOperation](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md) values, indicating the operation for which to set the timeout and policy `action`.</span></span> <span data-ttu-id="bdfcb-107">Поддерживаются следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bdfcb-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="bdfcb-108">OPR_AppDomainUnload</span><span class="sxs-lookup"><span data-stu-id="bdfcb-108">OPR_AppDomainUnload</span></span>  
  
-   <span data-ttu-id="bdfcb-109">OPR_ProcessExit</span><span class="sxs-lookup"><span data-stu-id="bdfcb-109">OPR_ProcessExit</span></span>  
  
-   <span data-ttu-id="bdfcb-110">OPR_ThreadRudeAbortInCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="bdfcb-110">OPR_ThreadRudeAbortInCriticalRegion</span></span>  
  
-   <span data-ttu-id="bdfcb-111">OPR_ThreadRudeAbortInNonCriticalRegion</span><span class="sxs-lookup"><span data-stu-id="bdfcb-111">OPR_ThreadRudeAbortInNonCriticalRegion</span></span>  
  
 `dwMilliseconds`  
 <span data-ttu-id="bdfcb-112">[in] Новое значение времени ожидания в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-112">[in] The new timeout value, in milliseconds.</span></span> <span data-ttu-id="bdfcb-113">Значение БЕСКОНЕЧНЫЙ причины `operation` никогда не до времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-113">A value of INFINITE causes `operation` never to time out.</span></span>  
  
 `action`  
 <span data-ttu-id="bdfcb-114">[in] Один из [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) значения, указывающие действие политики, когда должна выполнять среда CLR `operation` происходит.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-114">[in] One of the [EPolicyAction](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md) values, indicating the policy action that the CLR should take when `operation` occurs.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bdfcb-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bdfcb-115">Return Value</span></span>  
  
|<span data-ttu-id="bdfcb-116">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bdfcb-116">HRESULT</span></span>|<span data-ttu-id="bdfcb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="bdfcb-117">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bdfcb-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="bdfcb-118">S_OK</span></span>|<span data-ttu-id="bdfcb-119">`SetTimeoutAndAction`успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-119">`SetTimeoutAndAction` returned successfully.</span></span>|  
|<span data-ttu-id="bdfcb-120">ЗНАЧЕНИЕ HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bdfcb-120">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bdfcb-121">Среда CLR не загружена в процесс или находится в состоянии, в котором не может выполнять управляемый код или успешно обработать вызов.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-121">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bdfcb-122">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bdfcb-122">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bdfcb-123">Истекло время ожидания вызова.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-123">The call timed out.</span></span>|  
|<span data-ttu-id="bdfcb-124">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bdfcb-124">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bdfcb-125">Вызывающий объект не является владельцем блокировки.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-125">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bdfcb-126">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bdfcb-126">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bdfcb-127">Событие было отменено заблокированный поток или ожидал волокон.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-127">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bdfcb-128">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bdfcb-128">E_FAIL</span></span>|<span data-ttu-id="bdfcb-129">Неизвестная Неустранимая ошибка.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-129">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bdfcb-130">После метод вернет значение E_FAIL, среда CLR больше не может использоваться в процессе.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-130">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bdfcb-131">Последующие вызовы размещение методы возвращают значение HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-131">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="bdfcb-132">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bdfcb-132">E_INVALIDARG</span></span>|<span data-ttu-id="bdfcb-133">Невозможно задать время ожидания для указанного `operation`, или было задано недопустимое значение для `action`.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-133">A timeout cannot be set for the specified `operation`, or an invalid value was supplied for `action`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bdfcb-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="bdfcb-134">Remarks</span></span>  
 <span data-ttu-id="bdfcb-135">`SetTimeoutAndAction`Инкапсулирует возможности [ICLRPolicyManager::SetTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md) и [ICLRPolicyManager::SetActionOnTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md) методов и может быть вызван вместо последовательные вызовы этих двух методов.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-135">`SetTimeoutAndAction` encapsulates the capabilities of the [ICLRPolicyManager::SetTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeout-method.md) and [ICLRPolicyManager::SetActionOnTimeout](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md) methods, and can be called in place of sequential calls to these two methods.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="bdfcb-136">Не все значения действий политики может быть указан как поведение времени ожидания для операций среды CLR.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-136">Not all policy action values can be specified as the timeout behavior for CLR operations.</span></span> <span data-ttu-id="bdfcb-137">См. в разделах Примечание разделов для этих двух методов для допустимых значений.</span><span class="sxs-lookup"><span data-stu-id="bdfcb-137">See the Remarks sections of the topics for these two methods for valid values.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bdfcb-138">Требования</span><span class="sxs-lookup"><span data-stu-id="bdfcb-138">Requirements</span></span>  
 <span data-ttu-id="bdfcb-139">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bdfcb-139">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bdfcb-140">**Заголовок:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="bdfcb-140">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bdfcb-141">**Библиотека:** включена как ресурс в MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bdfcb-141">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bdfcb-142">**Версии платформы .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bdfcb-142">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bdfcb-143">См. также</span><span class="sxs-lookup"><span data-stu-id="bdfcb-143">See Also</span></span>  
 [<span data-ttu-id="bdfcb-144">EClrOperation-перечисление</span><span class="sxs-lookup"><span data-stu-id="bdfcb-144">EClrOperation Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclroperation-enumeration.md)  
 [<span data-ttu-id="bdfcb-145">EPolicyAction-перечисление</span><span class="sxs-lookup"><span data-stu-id="bdfcb-145">EPolicyAction Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/epolicyaction-enumeration.md)  
 [<span data-ttu-id="bdfcb-146">Интерфейс ICLRPolicyManager</span><span class="sxs-lookup"><span data-stu-id="bdfcb-146">ICLRPolicyManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md)  
 [<span data-ttu-id="bdfcb-147">SetActionOnTimeout-метод</span><span class="sxs-lookup"><span data-stu-id="bdfcb-147">SetActionOnTimeout Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-setactionontimeout-method.md)  
 [<span data-ttu-id="bdfcb-148">ICLRPolicyManager::SetTimeoutAndAction</span><span class="sxs-lookup"><span data-stu-id="bdfcb-148">ICLRPolicyManager::SetTimeoutAndAction</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-settimeoutandaction-method.md)