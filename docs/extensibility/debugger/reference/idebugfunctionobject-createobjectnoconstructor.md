---
title: IDebugFunctionObject::CreateObjectNoConstructor |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor
helpviewer_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor method
ms.assetid: 4e2bd6d5-f4bd-4c10-a998-3db451c9a0c8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6a5ecd42b0ddf0138e98e2159fae1236ca02b473
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56707389"
---
# <a name="idebugfunctionobjectcreateobjectnoconstructor"></a>IDebugFunctionObject::CreateObjectNoConstructor
使用沒有建構函式建立物件。

## <a name="syntax"></a>語法

```cpp
HRESULT CreateObjectNoConstructor( 
   IDebugField*   pClassObject,
   IDebugObject** ppObject
);
```

```csharp
int CreateObjectNoConstructor(
   IDebugField      pClassField,
   out IDebugObject ppObject
);
```

#### <a name="parameters"></a>參數
 `pClassObject`

 [in][IDebugField](../../../extensibility/debugger/reference/idebugfield.md)物件，表示要建立之物件的型別。

 `ppObject`

 [out]傳回[IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)代表新建立的物件。

## <a name="return-value"></a>傳回值
 如果成功，會傳回 S_OK;否則，傳回錯誤碼。

## <a name="remarks"></a>備註
 呼叫這個方法來建立物件，表示結構或複雜型別 （也就不需要建構函式） 的函式的參數所表示的執行個體[IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)介面。

 如果物件參數需要建構函式，呼叫[CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)方法。

## <a name="see-also"></a>另請參閱
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)
- [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)