---
title: 'Idiasymbol:: Get_function |Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_function method
ms.assetid: 48b3a318-3211-410f-8570-c02ee210f0a5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bde3de3d4098edb85a14dda8cd573327549a9deb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613397"
---
# <a name="idiasymbolgetfunction"></a>IDiaSymbol::get_function
擷取指定公用符號是否參考的函式的旗標。

## <a name="syntax"></a>語法

```C++
HRESULT get_function ( 
   BOOL* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]會傳回`TRUE`符號參考的函式; 否則會傳回`FALSE`。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。

> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。

## <a name="requirements"></a>需求

|需求|說明|
|-----------------|-----------------|
|標頭：|dia2.h|
|版本:|DIA SDK v7.0|

## <a name="see-also"></a>請參閱
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)