---
title: Метод IMetaDataAssemblyImport::FindManifestResourceByName
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindManifestResourceByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindManifestResourceByName
helpviewer_keywords:
- FindManifestResourceByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindManifestResourceByName method [.NET Framework metadata]
ms.assetid: 7b72fa11-3866-402b-bdea-2b966b77cfe0
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b05c9a75bf870dd3b2316d2df7c50932b26894f3
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54702747"
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a>Метод IMetaDataAssemblyImport::FindManifestResourceByName
Возвращает указатель на ресурс манифеста с указанным именем.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,   
    [out] mdManifestResource     *ptkManifestResource  
);   
```  
  
#### <a name="parameters"></a>Параметры  
 `szName`  
 [in] Имя ресурса.  
  
 `ptkManifestResource`  
 [out] Массив, используемый для хранения `mdManifestResource` маркеров метаданных, каждый из которых представляет ресурса манифеста.  
  
## <a name="remarks"></a>Примечания  
 `FindManifestResourceByName` Метод использует стандартные правила, чтобы позволить среда CLR для разрешения ссылок на.  
  
## <a name="requirements"></a>Требования  
 **Платформа:** См. раздел [Требования к системе](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Заголовок.** Cor.h  
  
 **Библиотека:** Используется как ресурс в MsCorEE.dll  
  
 **Версии платформы .NET Framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>См. также
- [Интерфейс IMetaDataAssemblyImport](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)
- [Обнаружение сборок в среде выполнения](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
