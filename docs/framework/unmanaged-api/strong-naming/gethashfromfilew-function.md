---
title: "Функция GetHashFromFileW"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetHashFromFileW
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: GetHashFromFileW
helpviewer_keywords: GetHashFromFileW function [.NET Framework strong naming]
ms.assetid: 97c2d7a6-5376-45a1-ba65-146a249147cc
topic_type: apiref
caps.latest.revision: "15"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2c19047f03279b1284ea8b5b8f99785cfaff5146
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2017
---
# <a name="gethashfromfilew-function"></a><span data-ttu-id="69c22-102">Функция GetHashFromFileW</span><span class="sxs-lookup"><span data-stu-id="69c22-102">GetHashFromFileW Function</span></span>
<span data-ttu-id="69c22-103">Создает хэш содержимого файла, заданный строкой в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="69c22-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
 <span data-ttu-id="69c22-104">Эта функция устарела.</span><span class="sxs-lookup"><span data-stu-id="69c22-104">This function has been deprecated.</span></span> <span data-ttu-id="69c22-105">Используйте [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) метод вместо него.</span><span class="sxs-lookup"><span data-stu-id="69c22-105">Use the [ICLRStrongName::GetHashFromFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="69c22-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="69c22-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromFileW (   
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="69c22-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="69c22-107">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="69c22-108">[in] Имя файла для хеширования Юникода.</span><span class="sxs-lookup"><span data-stu-id="69c22-108">[in] The Unicode name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="69c22-109">[in, out] Алгоритм, используемый при создании хеша.</span><span class="sxs-lookup"><span data-stu-id="69c22-109">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="69c22-110">Допустимыми являются алгоритмы, определенные интерфейсом CryptoAPI в Win32.</span><span class="sxs-lookup"><span data-stu-id="69c22-110">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="69c22-111">Если `piHashAlg` имеет значение 0, алгоритм по умолчанию используется CALG_SHA-1.</span><span class="sxs-lookup"><span data-stu-id="69c22-111">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="69c22-112">[out] Массив байтов, содержащий созданный хеш.</span><span class="sxs-lookup"><span data-stu-id="69c22-112">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="69c22-113">[in] Максимальный размер буфера, на который указывает `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="69c22-113">[in] The maximum size of the buffer pointed to by `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="69c22-114">[out] Размер в байтах для `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="69c22-114">[out] The size, in bytes, of `pbHash`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="69c22-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="69c22-115">Remarks</span></span>  
 <span data-ttu-id="69c22-116">Эта функция является таким же, как [GetHashFromFile](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfile-function.md), за исключением того, что спецификация имени файла имеет формат Юникода, а не ANSI.</span><span class="sxs-lookup"><span data-stu-id="69c22-116">This function is the same as [GetHashFromFile](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfile-function.md), except that the file name specification is Unicode instead of ANSI.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="69c22-117">Требования</span><span class="sxs-lookup"><span data-stu-id="69c22-117">Requirements</span></span>  
 <span data-ttu-id="69c22-118">**Платформы:** разделе [требования к системе для](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="69c22-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="69c22-119">**Заголовок:** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="69c22-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="69c22-120">**Библиотека:** включена как ресурс в MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="69c22-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="69c22-121">**Версии платформы .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="69c22-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="69c22-122">См. также</span><span class="sxs-lookup"><span data-stu-id="69c22-122">See Also</span></span>  
 [<span data-ttu-id="69c22-123">Метод GetHashFromFileW</span><span class="sxs-lookup"><span data-stu-id="69c22-123">GetHashFromFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md)  
 [<span data-ttu-id="69c22-124">Метод GetHashFromFile</span><span class="sxs-lookup"><span data-stu-id="69c22-124">GetHashFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md)  
 [<span data-ttu-id="69c22-125">Iclrstrongname-интерфейс</span><span class="sxs-lookup"><span data-stu-id="69c22-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)