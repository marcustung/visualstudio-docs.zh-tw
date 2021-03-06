---
title: FIELD_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FIELD_INFO
helpviewer_keywords:
- FIELD_INFO structure
ms.assetid: bfafef6d-0c83-43d7-a779-1f0d24b166a1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 83cdacae192ad1286203139432a0eacd632b8511
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694223"
---
# <a name="fieldinfo"></a>FIELD_INFO
此結構描述的本機變數、 參數或其他欄位。

## <a name="syntax"></a>語法

```cpp
typedef struct _tagFieldInfo {
    FIELD_INFO_FIELDS dwFields;
    BSTR              bstrFullName;
    BSTR              bstrName;
    BSTR              bstrType;
    FIELD_MODIFIERS   dwModifiers;
} FIELD_INFO;
```

```csharp
public struct FIELD_INFO {
    public uint   dwFields;
    public string bstrFullName;
    public string bstrName;
    public string bstrType;
    public uint   dwModifiers;
};
```

## <a name="members"></a>成員
dwFields A 中的旗標的組合[FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md)列舉，指定哪些成員會填入。

bstrFullName 欄位的完整名稱。

bstrName 欄位的簡短名稱。

bstrType 欄位的型別。

dwModifiers A 中的旗標的組合[FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)描述欄位的列舉型別。

## <a name="remarks"></a>備註
此結構會傳遞至[GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)填滿其中的方法。

## <a name="requirements"></a>需求
標頭： sh.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [結構和等位](../../../extensibility/debugger/reference/structures-and-unions.md)
- [FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md)
- [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)
