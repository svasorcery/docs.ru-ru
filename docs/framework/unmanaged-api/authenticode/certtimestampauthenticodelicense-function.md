---
title: Функция CertTimestampAuthenticodeLicense
ms.date: 03/30/2017
api_name:
- CertTimestampAuthenticodeLicense
api_location:
- clr.dll
api_type:
- DLLExport
ms.assetid: d468325a-21c5-43ce-8567-84e342b22308
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9987640f988f2239a01d2dfdbcd6b1684579d8bc
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/23/2019
ms.locfileid: "54601512"
---
# <a name="certtimestampauthenticodelicense-function"></a>Функция CertTimestampAuthenticodeLicense
Отметки времени для лицензии Authenticode XrML.  
  
## <a name="syntax"></a>Синтаксис  
  
```  
HRESULT CertTimestampAuthenticodeLicense (  
    [in]  PCRYPT_DATA_BLOB   pSignedLicenseBlob,  
    [in]  LPCWSTR            pwszTimestampURI,  
    [out] PCRYPT_DATA_BLOB   pTimestampSignatureBlob  
);  
```  
  
#### <a name="parameters"></a>Параметры  
 `pSignedLicenseBlob`  
 [в] Подписанная лицензия Authenticode XrML, требующая отметки времени. См. в разделе [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) структуры.  
  
 `pwszTimestampURI`  
 [в] URL-адресу сервера отметок времени.  
  
 `pTimestampSignatureBlob`  
 [из] Указатель на CRYPT_DATA_BLOB для получения подписи с отметкой времени в кодировке base64. Это обязанность вызывающего для освобождения `pTimestampSignatureBlob` -> `pbData` с `HepFree()` после использования. См. в разделе [CRYPTOAPI_BLOB](/windows/desktop/api/dpapi/ns-dpapi-_cryptoapi_blob) структуры.  
  
## <a name="remarks"></a>Примечания  
 Подпись с отметкой времени фактически представляет собой сообщение PKCS #7 SignedData, содержимое которого является двоичной формой SignatureValue из подписи лицензии. По сути, она действует как подпись, подтверждающая лицензию.  
  
## <a name="return-value"></a>Возвращаемое значение  
 `S_OK`, если функция выполняется успешно. В противном случае возвращается код ошибки.  
  
## <a name="see-also"></a>См. также
- [Authenticode](../../../../docs/framework/unmanaged-api/authenticode/index.md)
