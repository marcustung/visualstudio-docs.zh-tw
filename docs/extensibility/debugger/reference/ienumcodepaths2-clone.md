---
title: IEnumCodePaths2::Clone | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumCodePaths2::Clone
helpviewer_keywords:
- IEnumCodePaths2::Clone
ms.assetid: 9d5c6bc6-7e72-4f1b-801c-7192458f3ba8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 54148f7442d714f40b0eab68131113c751cde8e9
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56684373"
---
# <a name="ienumcodepaths2clone"></a>IEnumCodePaths2::Clone
傳回一份目前的列舉，為個別的物件。

## <a name="syntax"></a>語法

```cpp
HRESULT Clone(
   IEnumCodePaths2** ppEnum
);
```

```csharp
int Clone(
   out IEnumCodePaths2 ppEnum
);
```

#### <a name="parameters"></a>參數
 `ppEnum`

 [out]傳回這個列舉型別為個別物件的複本。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 列舉的複本會呼叫這個方法只有在有相同的原始狀態。 不過，複本與原始的狀態是分開的而且可以個別變更。

## <a name="see-also"></a>另請參閱
- [IEnumCodePaths2](../../../extensibility/debugger/reference/ienumcodepaths2.md)