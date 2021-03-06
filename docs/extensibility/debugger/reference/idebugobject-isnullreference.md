---
title: IDebugObject::IsNullReference |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::IsNullReference
helpviewer_keywords:
- IDebugObject::IsNullReference method
ms.assetid: 6dbfcdb0-954f-4486-8fac-7ea8d003e3a9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 25de5fdde9e0d834b98f09d2f5c9e2444f8a9d0e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706895"
---
# <a name="idebugobjectisnullreference"></a>IDebugObject::IsNullReference
測試這個物件是否為 null 參考。

## <a name="syntax"></a>語法

```cpp
HRESULT IsNullReference( 
   BOOL* pfIsNull
);
```

```csharp
int IsNullReference(
   out int pfIsNull
);
```

#### <a name="parameters"></a>參數
 `pfIsNull`

 [out]會傳回非零 (`TRUE`) 如果此物件為 null 的參考; 否則會傳回零 (`FALSE`)。

## <a name="return-value"></a>傳回值
 如果成功，會傳回 S_OK;否則，傳回錯誤碼。

## <a name="remarks"></a>備註
 Null 的參考表示空的物件或尚未指派給物件。

## <a name="see-also"></a>另請參閱
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)