---
title: IDiaLineNumber::get_compilandId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaLineNumber::get_compilandId method
ms.assetid: 2cd6f551-8091-47c7-803f-3f79a766a211
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9874dec57c873164ec1875f31fd15c817781bb7a
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56610904"
---
# <a name="idialinenumbergetcompilandid"></a>IDiaLineNumber::get_compilandId
擷取提供這一行將編譯模組的唯一識別碼。

## <a name="syntax"></a>語法

```C++
HRESULT get_compilandId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]傳回`DWORD`包含提供這一行將編譯模組的唯一識別碼。

## <a name="return-value"></a>傳回值
 如果成功，會傳回 `S_OK`。 傳回`S_FALSE`不支援這個屬性，則為。 否則會傳回錯誤碼。

## <a name="see-also"></a>請參閱
- [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)