---
title: IDiaSymbol::get_libraryName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_libraryName method
ms.assetid: d04ddd9a-812d-46e4-bd39-28bdf3edfb70
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f832bc0472cc6b04d803dc1e5871eda62bbe451d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56605636"
---
# <a name="idiasymbolgetlibraryname"></a>IDiaSymbol::get_libraryName
擷取要從中載入物件的文件庫或物件檔案的檔案名稱。

## <a name="syntax"></a>語法

```C++
HRESULT get_libraryName ( 
   BSTR* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]傳回從中載入物件的文件庫或物件檔案的檔案名稱。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。

> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。

## <a name="see-also"></a>請參閱
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)