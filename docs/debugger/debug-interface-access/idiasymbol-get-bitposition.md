---
title: IDiaSymbol::get_bitPosition | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_bitPosition method
ms.assetid: b0059407-8655-497b-81ca-025595989371
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 521a21b2d3534433fe72ea6bd9578c0e668755ac
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56611824"
---
# <a name="idiasymbolgetbitposition"></a>IDiaSymbol::get_bitPosition
擷取位置的位元位置。 使用的時機[LocationType 列舉](../../debugger/debug-interface-access/locationtype.md)是`LocIsBitField`。

## <a name="syntax"></a>語法

```C++
HRESULT get_bitPosition ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]傳回位置的位元位置。

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
- [LocationType 列舉](../../debugger/debug-interface-access/locationtype.md)