---
title: IDiaPropertyStorage::ReadPropertyNames |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaPropertyStorage::ReadPropertyNames
ms.assetid: f8bcab77-afca-4a8f-8710-697842f8a518
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7492e0eee0523fd102ecd057d075f2672bf3b25b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695839"
---
# <a name="idiapropertystoragereadpropertynames"></a>IDiaPropertyStorage::ReadPropertyNames
擷取對應的字串名稱指定屬性識別碼。

## <a name="syntax"></a>語法

```C++
HRESULT ReadPropertyNames (
   ULONG         cpropid,
   PROPID const* rgpropid,
   BSTR*         rglpwstrName
);
```

#### <a name="parameters"></a>參數
 `cpropid`

[in]中的屬性識別碼的數目`rgpropid`。

 `rgpropid`

[in]要取得名稱的屬性識別碼的陣列 (`PROPID`定義為 WTypes.h 中`ULONG`)。

 `rglpwstrName`

[in、 out]指定的屬性識別碼的屬性名稱的陣列。 陣列必須預先配置來保存屬性名稱的要求的數目，而且必須能夠容納至少`cpropid``BSTR`字串。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則會傳回錯誤碼。

## <a name="remarks"></a>備註
 傳回的屬性名稱，必須釋放 (藉由呼叫`SysFreeString`函式) 在不再需要時。

## <a name="see-also"></a>請參閱
- [IDiaPropertyStorage](../../debugger/debug-interface-access/idiapropertystorage.md)