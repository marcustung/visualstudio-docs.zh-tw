---
title: 'Idiasymbol:: Get_thisadjust |Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_thisAdjust method
ms.assetid: 56b9a147-e8c0-4d4b-a42a-398214dd5f86
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d63047375ce1e224a8e4ba70d4e1de8bf276c703
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56643024"
---
# <a name="idiasymbolgetthisadjust"></a>IDiaSymbol::get_thisAdjust
擷取邏輯`this`adjustor 方法。

## <a name="syntax"></a>語法

```C++
HRESULT get_thisAdjust ( 
   LONG* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]傳回邏輯`this`adjustor 方法。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。

> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。

## <a name="remarks"></a>備註
 在某些多重繼承的情況下，方法本身必須計算真正`this`加上位移值`this`。

## <a name="see-also"></a>請參閱
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)