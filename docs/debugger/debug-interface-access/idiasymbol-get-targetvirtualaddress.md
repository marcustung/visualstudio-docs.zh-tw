---
title: IDiaSymbol::get_targetVirtualAddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_targetVirtualAddress method
ms.assetid: a0a5ce72-95f8-443e-bb4b-8c21194faad0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ade3d2d968a7b152c982f34fc03144f21059e007
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56635263"
---
# <a name="idiasymbolgettargetvirtualaddress"></a>IDiaSymbol::get_targetVirtualAddress
擷取 thunk 目標的虛擬位址 (VA)。

## <a name="syntax"></a>語法

```C++
HRESULT get_targetVirtualAddress ( 
   ULONGLONG* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]傳回 thunk 目標的 VA。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。

> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。

## <a name="remarks"></a>備註
 這個屬性就有效才做為符號[SymTagEnum 列舉](../../debugger/debug-interface-access/symtagenum.md)的值`SymTagThunk`。

 「 Thunk 」 是一種轉換的 32 位元記憶體位址空間 （也就是一般的位址空間） 和 （又稱為分段的位址空間） 的 16 位元位址空間的程式碼。

## <a name="see-also"></a>請參閱
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [SymTagEnum 列舉](../../debugger/debug-interface-access/symtagenum.md)