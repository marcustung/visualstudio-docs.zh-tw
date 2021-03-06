---
title: BPREQI_FIELDS90 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- BPREQI_FIELDS90 enumeration
ms.assetid: bf6f7efc-39f2-46a2-906d-c3647bf89995
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: be07e034b4059ae7ade40a5a248c01bc4a8237b8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695930"
---
# <a name="bpreqifields90"></a>BPREQI_FIELDS90
列舉有效的值，指定要擷取有關中斷點要求的資訊。 這個列舉型別會擴充[BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)列舉型別。

## <a name="syntax"></a>語法

```cpp
enum enum_BPREQI_FIELDS90
{
    // VS 8.0 values
    BPREQI90_BPLOCATION                = 0x0001,
    BPREQI90_LANGUAGE                  = 0x0002,
    BPREQI90_PROGRAM                   = 0x0004,
    BPREQI90_PROGRAMNAME               = 0x0008,
    BPREQI90_THREAD                    = 0x0010,
    BPREQI90_THREADNAME                = 0x0020,
    BPREQI90_PASSCOUNT                 = 0x0040,
    BPREQI90_CONDITION                 = 0x0080,
    BPREQI90_FLAGS                     = 0x0100,
    BPREQI90_ALLOLDFIELDS              = 0x01ff,
    BPREQI90_VENDOR                    = 0x0200,
    BPREQI90_CONSTRAINT                = 0x0400,
    BPREQI90_TRACEPOINT                = 0x0800,

    // Values added in VS 9.0
    BPREQI90_MACROTRACEPOINT           = 0x1000,

    BPREQI90_ALLFIELDS                 = 0xffff
};
typedef DWORD BPREQI_FIELDS90;
```

```csharp
public enum enum_BPREQI_FIELDS90
{
    // VS 8.0 values
    BPREQI90_BPLOCATION                = 0x0001,
    BPREQI90_LANGUAGE                  = 0x0002,
    BPREQI90_PROGRAM                   = 0x0004,
    BPREQI90_PROGRAMNAME               = 0x0008,
    BPREQI90_THREAD                    = 0x0010,
    BPREQI90_THREADNAME                = 0x0020,
    BPREQI90_PASSCOUNT                 = 0x0040,
    BPREQI90_CONDITION                 = 0x0080,
    BPREQI90_FLAGS                     = 0x0100,
    BPREQI90_ALLOLDFIELDS              = 0x01ff,
    BPREQI90_VENDOR                    = 0x0200,
    BPREQI90_CONSTRAINT                = 0x0400,
    BPREQI90_TRACEPOINT                = 0x0800,

    // Values added in VS 9.0
    BPREQI90_MACROTRACEPOINT           = 0x1000,

    BPREQI90_ALLFIELDS                 = 0xffff
};
```

#### <a name="parameters"></a>參數
BPREQI90_BPLOCATION 初始化，或使用`bpLocation`（中斷點位置） 欄位[BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)或是[BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)結構。

BPREQI90_LANGUAGE 初始化，或使用`guidLanguage`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_PROGRAM 初始化，或使用`pProgram`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_PROGRAMNAME 初始化，或使用`bstrProgramName`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_THREAD 初始化，或使用`pThread`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_THREADNAME 初始化，或使用`bstrThreadName`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_PASSCOUNT 初始化，或使用`bpPassCount`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_CONDITION 初始化，或使用`bpCondition`（中斷點條件） 欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_FLAGS 初始化，或使用`dwFlags`欄位`BP_REQUEST_INFO`或`BP_REQUEST_INFO2`結構。

BPREQI90_ALLOLDFIELDS 初始化或所有欄位的使用的`BP_REQUEST_INFO`結構。

BPREQI90_VENDOR 初始化，或使用`guidVendor`欄位`BP_REQUEST_INFO2`結構。

BPREQI90_CONSTRAINT 初始化，或使用`bstrConstraint`欄位`BP_REQUEST_INFO2`結構。

BPREQI90_TRACEPOINT 初始化，或使用`bstrTracepoint`欄位`BP_REQUEST_INFO2`結構。

BPREQI90_MACROTRACEPOINT 初始化，或使用`bstrMacroTracepoint`欄位`BP_REQUEST_INFO2`結構。 BPREQI_ALLFIELDS 不包含此欄位。

BPREQI90_ALLFIELDS 指定所有欄位`BP_REQUEST_INFO2`結構。

## <a name="requirements"></a>需求
標頭：Msdbg90.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
