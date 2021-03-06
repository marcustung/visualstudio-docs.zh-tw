---
title: IDebugClassField::EnumConstructors |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugClassField::EnumConstructors
helpviewer_keywords:
- IDebugClassField::EnumConstructors method
ms.assetid: 66a250b2-75a0-45aa-8d58-40f91cc4bf7b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5ecc2e2fba9dbddc12a58866c7edcde51b148af1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56719095"
---
# <a name="idebugclassfieldenumconstructors"></a>IDebugClassField::EnumConstructors
建立這個類別的建構函式的列舉值。

## <a name="syntax"></a>語法

```cpp
HRESULT EnumConstructors( 
   CONSTRUCTOR_ENUM   cMatch,
   IEnumDebugFields** ppEnum
);
```

```csharp
int EnumConstructors(
   CONSTRUCTOR_ENUM     cMatch,
   out IEnumDebugFields ppEnum
);
```

#### <a name="parameters"></a>參數
 `cMatch`

 [in]值，以從[CONSTRUCTOR_ENUM](../../../extensibility/debugger/reference/constructor-enum.md)列舉，指定列舉型別建構函式的型別。

 `ppEnum`

 [out]傳回[IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)物件，表示建構函式的清單。 如果不有任何建構函式會傳回 null 值。

## <a name="return-value"></a>傳回值
 如果成功，會傳回 S_OK，或如果沒有任何建構函式，則傳回 S_FALSE。 否則會傳回錯誤碼。

## <a name="remarks"></a>備註
 列舉型別的每個項目是[IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)物件，描述建構函式方法。

 通常的建構函式清單不包含編譯器所提供的預設建構函式。

## <a name="see-also"></a>另請參閱
- [IDebugClassField](../../../extensibility/debugger/reference/idebugclassfield.md)
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)
- [IDebugMethodField](../../../extensibility/debugger/reference/idebugmethodfield.md)
- [CONSTRUCTOR_ENUM](../../../extensibility/debugger/reference/constructor-enum.md)