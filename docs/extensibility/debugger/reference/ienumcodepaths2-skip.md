---
title: IEnumCodePaths2::Skip | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumCodePaths2::Skip
helpviewer_keywords:
- IEnumCodePaths2::Skip
ms.assetid: 356472d8-68b2-4b7e-b5f0-1f16d4ee80af
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 61d176a13e71ce2dfbe00744e6c45b8d97762291
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56713278"
---
# <a name="ienumcodepaths2skip"></a>IEnumCodePaths2::Skip
略過指定的元素數目。

## <a name="syntax"></a>語法

```cpp
HRESULT Skip(
   ULONG celt
);
```

```csharp
int Skip(
   uint celt
);
```

#### <a name="parameters"></a>參數
 `celt`

 [in]略過的項目數目。

## <a name="return-value"></a>傳回值
 如果成功，會傳回 `S_OK`。 會傳回`S_FALSE`如果`celt`大於其餘項目數目，否則會傳回錯誤碼。

## <a name="remarks"></a>備註
 如果`celt`指定的值大於其餘的項目，列舉型別設定為結束和`S_FALSE`會傳回。

## <a name="see-also"></a>另請參閱
- [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md)