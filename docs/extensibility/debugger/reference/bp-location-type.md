---
title: BP_LOCATION_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_LOCATION_TYPE
helpviewer_keywords:
- BP_LOCATION_TYPE structure
ms.assetid: 0248430a-3b61-4809-87a9-e9b6bb7d1130
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1695c61a829cf1439ed773e48088430f36f8c653
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56715657"
---
# <a name="bplocationtype"></a>BP_LOCATION_TYPE
指定中斷點要求的中斷點位置類型。

## <a name="syntax"></a>語法

```cpp
enum enum_BP_LOCATION_TYPE {
    BPLT_NONE               = 0x00000000,
    BPLT_FILE_LINE          = 0x00010000,
    BPLT_FUNC_OFFSET        = 0x00020000,
    BPLT_CONTEXT            = 0x00030000,
    BPLT_STRING             = 0x00040000,
    BPLT_ADDRESS            = 0x00050000,
    BPLT_RESOLUTION         = 0x00060000,
    BPLT_CODE_FILE_LINE     = BPT_CODE | BPLT_FILE_LINE,
    BPLT_CODE_FUNC_OFFSET   = BPT_CODE | BPLT_FUNC_OFFSET,
    BPLT_CODE_CONTEXT       = BPT_CODE | BPLT_CONTEXT,
    BPLT_CODE_STRING        = BPT_CODE | BPLT_STRING,
    BPLT_CODE_ADDRESS       = BPT_CODE | BPLT_ADDRESS ,
    BPLT_DATA_STRING        = BPT_DATA | BPLT_STRING,
    BPLT_TYPE_MASK          = 0x0000FFFF,
    BPLT_LOCATION_TYPE_MASK = 0xFFFF0000
};
typedef DWORD BP_LOCATION_TYPE;
```

```csharp
public enum enum_BP_LOCATION_TYPE {
    BPLT_NONE               = 0x00000000,
    BPLT_FILE_LINE          = 0x00010000,
    BPLT_FUNC_OFFSET        = 0x00020000,
    BPLT_CONTEXT            = 0x00030000,
    BPLT_STRING             = 0x00040000,
    BPLT_ADDRESS            = 0x00050000,
    BPLT_RESOLUTION         = 0x00060000,
    BPLT_CODE_FILE_LINE     = BPT_CODE | BPLT_FILE_LINE,
    BPLT_CODE_FUNC_OFFSET   = BPT_CODE | BPLT_FUNC_OFFSET,
    BPLT_CODE_CONTEXT       = BPT_CODE | BPLT_CONTEXT,
    BPLT_CODE_STRING        = BPT_CODE | BPLT_STRING,
    BPLT_CODE_ADDRESS       = BPT_CODE | BPLT_ADDRESS ,
    BPLT_DATA_STRING        = BPT_DATA | BPLT_STRING,
    BPLT_TYPE_MASK          = 0x0000FFFF,
    BPLT_LOCATION_TYPE_MASK = 0xFFFF0000
};
```

## <a name="members"></a>成員
BPLT_NONE 指定任何中斷點的位置。

BPLT_FILE_LINE 指定中斷點的位置類型為的檔案。

BPLT_FUNC_OFFSET 指定中斷點的位置類型當作函式位移。

BPLT_CONTEXT 做為內容指定中斷點的位置類型。

BPLT_STRING 指定中斷點的位置類型為字串。

BPLT_ADDRESS 會指定為位址中斷點的位置類型。

BPLT_RESOLUTION 解析為指定中斷點位置的類型。

BPLT_CODE_FILE_LINE 會指定為來源的程式碼行中斷點的位置類型。

BPLT_CODE_FUNC_OFFSET 指定中斷點的位置類型的程式碼的函式位移。

BPLT_CODE_CONTEXT 指定中斷點的位置類型做為程式碼內容。

BPLT_CODE_STRING 指定中斷點的位置類型做為程式碼的字串。

BPLT_CODE_ADDRESS 指定中斷點的位置類型做為程式碼位址。

BPLT_DATA_STRING 指定中斷點的位置類型做為資料字串。

BPLT_TYPE_MASK 指定位元遮罩，如此中斷點類型可擷取出的值。

BPLT_LOCATION_TYPE_MASK 指定位元遮罩，如此中斷點位置類型可以擷取出的值。

## <a name="remarks"></a>備註
做為參數傳遞[GetLocationType](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getlocationtype.md)方法。

中斷點位置類型是由中斷點類型和位置類型所組成。 這表示中斷點位置類型不只是中斷點類型 (例如`BPT_CODE`) 或位置類型 (例如`BPLT_FILE_LINE`)。 目前支援的所有中斷點位置類型預先定義的常數都會納入此列舉型別 (`BPLT_CODE_FILE_LINE`透過`BPLT_DATA_STRING`)。

`BPT_CODE` 並`BPT_DATA`屬於[BP_TYPE](../../../extensibility/debugger/reference/bp-type.md)列舉型別。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetLocationType](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getlocationtype.md)
- [BP_TYPE](../../../extensibility/debugger/reference/bp-type.md)
