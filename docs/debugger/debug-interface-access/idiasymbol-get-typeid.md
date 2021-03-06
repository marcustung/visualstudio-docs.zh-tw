---
title: IDiaSymbol::get_typeId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_typeId method
ms.assetid: b40be36e-10e1-463c-9c6d-21862679d29f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab6b6194534c6cf3acddbaa94dfc314d8d30514a
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56606000"
---
# <a name="idiasymbolgettypeid"></a>IDiaSymbol::get_typeId
擷取之符號的類型識別碼。

## <a name="syntax"></a>語法

```C++
HRESULT get_typeId ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>參數
 `pRetVal`

[out]傳回符號的類型識別碼。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。

> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。

## <a name="remarks"></a>備註
 識別碼是由 DIA SDK，將標示為唯一的所有符號的唯一值。

## <a name="see-also"></a>請參閱
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)