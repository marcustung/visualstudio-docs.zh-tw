---
title: DEBUGREF_INFO_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DEBUGREF_INFO_FLAGS
helpviewer_keywords:
- DEBUGREF_INFO_FLAGS enumeration
ms.assetid: 1b043327-302a-4f6d-b51d-f94f9d7c7f9d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 50efecb332be0a1cd9d9ff2c92dc97d5096eb44e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56686287"
---
# <a name="debugrefinfoflags"></a>DEBUGREF_INFO_FLAGS
指定要擷取偵錯參考物件的相關資訊。

## <a name="syntax"></a>語法

```cpp
enum enum_DEBUGREF_INFO_FLAGS {
    DEBUGREF_INFO_NAME             = 0x00000001,
    DEBUGREF_INFO_TYPE             = 0x00000002,
    DEBUGREF_INFO_VALUE            = 0x00000004,
    DEBUGREF_INFO_ATTRIB           = 0x00000008,
    DEBUGREF_INFO_REFTYPE          = 0x00000010,
    DEBUGREF_INFO_REF              = 0x00000020,
    DEBUGREF_INFO_VALUE_AUTOEXPAND = 0x00010000,
    DEBUGREF_INFO_NONE             = 0x00000000,
    DEBUGREF_INFO_ALL              = 0xffffffff
};
typedef DWORD DEBUGREF_INFO_FLAGS;
```

```csharp
public enum enum_DEBUGREF_INFO_FLAGS {
    DEBUGREF_INFO_NAME             = 0x00000001,
    DEBUGREF_INFO_TYPE             = 0x00000002,
    DEBUGREF_INFO_VALUE            = 0x00000004,
    DEBUGREF_INFO_ATTRIB           = 0x00000008,
    DEBUGREF_INFO_REFTYPE          = 0x00000010,
    DEBUGREF_INFO_REF              = 0x00000020,
    DEBUGREF_INFO_VALUE_AUTOEXPAND = 0x00010000,
    DEBUGREF_INFO_NONE             = 0x00000000,
    DEBUGREF_INFO_ALL              = 0xffffffff
};
```

## <a name="members"></a>成員
DEBUGREF_INFO_NAME 初始化/使用`bstrName`欄位在結構中。

DEBUGREF_INFO_TYPE 初始化/使用`bstrType`欄位在結構中。

DEBUGREF_INFO_VALUE 初始化/使用`bstrValue`欄位在結構中。

DEBUGREF_INFO_ATTRIB 初始化/使用`dwAttrib`欄位在結構中。

DEBUGREF_INFO_REFTYPE 初始化/使用`dwRefType`欄位在結構中。

DEBUGREF_INFO_REF 初始化/使用`pReference`欄位在結構中。

DEBUGREF_INFO_VALUE_AUTOEXPAND [值] 欄位應該包含自動展開值，如果有的話，這種類型的物件。

DEBUGREF_INFO_NONE 表示未設定任何旗標。

DEBUGREF_INFO_ALL 表示旗標的遮罩。

## <a name="remarks"></a>備註
這些旗標會傳遞給[EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)並[GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)方法以指出哪些欄位[DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md)結構會進行初始化。

用於`dwFields`隸屬`DEBUG_REFERENCE_INFO`表示哪些欄位是使用和有效時，會傳回這個結構的結構。

這些值可能會合併的位元`OR`。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [DEBUG_REFERENCE_INFO](../../../extensibility/debugger/reference/debug-reference-info.md)
- [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)
- [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)
