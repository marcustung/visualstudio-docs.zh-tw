---
title: THUNK_ORDINAL | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- Thunk_Ordinal enumeration
ms.assetid: 026f98a9-36b8-41ef-8a72-12d7cbc2d362
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 776ee35e57b62463d47fc6f7fa26133f507f16f9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56613267"
---
# <a name="thunkordinal"></a>THUNK_ORDINAL
將指定的 thunk 類型。

## <a name="syntax"></a>語法

```C++
typedef enum THUNK_ORDINAL {
    THUNK_ORDINAL_NOTYPE,
    THUNK_ORDINAL_ADJUSTOR,
    THUNK_ORDINAL_VCALL,
    THUNK_ORDINAL_PCODE,
    THUNK_ORDINAL_LOAD

    // trampoline thunk ordinals - only for use in Trampoline thunk symbols
    THUNK_ORDINAL_TRAMP_INCREMENTAL,
    THUNK_ORDINAL_TRAMP_BRANCHISLAND,
} THUNK_ORDINAL;
```

## <a name="elements"></a>項目
標準 THUNK_ORDINAL_NOTYPE thunk。

THUNK_ORDINAL_ADJUSTOR A `this` adjustor thunk。

THUNK_ORDINAL_VCALL 虛擬呼叫 thunk。

THUNK_ORDINAL_PCODE p-code thunk。

THUNK_ORDINAL_LOAD 延遲載入 thunk。

（trampoline thunk 用來從一個記憶體空間的呼叫退回到另一個） 的累加 THUNK_ORDINAL_TRAMP_INCREMENTAL trampoline thunk。

THUNK_ORDINAL_TRAMP_BRANCHISLAND 分支點 trampoline thunk。

## <a name="remarks"></a>備註
這個列舉型別中的值會傳回呼叫[idiasymbol:: Get_thunkordinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md)方法。

## <a name="requirements"></a>需求
標頭： cvconst.h

## <a name="see-also"></a>請參閱
- [列舉和結構](../../debugger/debug-interface-access/enumerations-and-structures.md)
- [IDiaSymbol::get_thunkOrdinal](../../debugger/debug-interface-access/idiasymbol-get-thunkordinal.md)
