---
title: BP_ERROR_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_ERROR_TYPE
helpviewer_keywords:
- BP_ERROR_TYPE enumeration
ms.assetid: c483eaab-db29-46de-bfdb-5c2a9a9cfb68
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2964c833abfa25b57678680f8b821f992cb31de8
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56689183"
---
# <a name="bperrortype"></a>BP_ERROR_TYPE
指定中斷點的錯誤類型。

## <a name="syntax"></a>語法

```cpp
enum enum_BP_ERROR_TYPE {
    BPET_NONE            = 0x00000000,
    BPET_TYPE_WARNING    = 0x00000001,
    BPET_TYPE_ERROR      = 0x00000002,
    BPET_SEV_HIGH        = 0x0F000000,
    BPET_SEV_GENERAL     = 0x07000000,
    BPET_SEV_LOW         = 0x01000000,
    BPET_TYPE_MASK       = 0x0000ffff,
    BPET_SEV_MASK        = 0xffff0000,
    BPET_GENERAL_WARNING = BPET_SEV_GENERAL | BPET_TYPE_WARNING,
    BPET_GENERAL_ERROR   = BPET_SEV_GENERAL | BPET_TYPE_ERROR,
    BPET_ALL             = 0xffffffff
};
typedef DWORD BP_ERROR_TYPE;
```

```csharp
public enum enum_BP_ERROR_TYPE {
    BPET_NONE            = 0x00000000,
    BPET_TYPE_WARNING    = 0x00000001,
    BPET_TYPE_ERROR      = 0x00000002,
    BPET_SEV_HIGH        = 0x0F000000,
    BPET_SEV_GENERAL     = 0x07000000,
    BPET_SEV_LOW         = 0x01000000,
    BPET_TYPE_MASK       = 0x0000ffff,
    BPET_SEV_MASK        = 0xffff0000,
    BPET_GENERAL_WARNING = BPET_SEV_GENERAL | BPET_TYPE_WARNING,
    BPET_GENERAL_ERROR   = BPET_SEV_GENERAL | BPET_TYPE_ERROR,
    BPET_ALL             = 0xffffffff
};
```

## <a name="members"></a>成員
BPET_NONE 指定任何中斷點時發生錯誤。

BPET_TYPE_WARNING 指定警告樣式中斷點時發生錯誤。

BPET_TYPE_ERROR 指定錯誤樣式中斷點時發生錯誤。

BPET_SEV_HIGH 指定高嚴重性中斷點時發生錯誤。

BPET_SEV_GENERAL 指定中度嚴重性中斷點時發生錯誤。

BPET_SEV_LOW 指定低嚴重性中斷點時發生錯誤。

BPET_TYPE_MASK 指定遮罩樣式中斷點時發生錯誤。

BPET_SEV_MASK 指定嚴重性遮罩樣式中斷點時發生錯誤。

BPET_GENERAL_WARNING 指定一般警告樣式中斷點時發生錯誤。

BPET_GENERAL_ERROR 指定一般錯誤樣式中斷點時發生錯誤。

BPET_ALL 指定所有中斷點時發生錯誤類型。

## <a name="remarks"></a>備註
這些值可能會合併的位元`OR`，並用於`dwType`隸屬[BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)結構。 做為參數傳遞[EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)方法。

中斷點錯誤型別被組成類型和嚴重性而定。 這表示中斷點錯誤類型永遠不會是型別 (例如`BPET_TYPE_ERROR`，) 或嚴重性 (比方說， `BPET_SEV_GENERAL`) 本身。 `BPET_GENERAL_WARNING` 和`BPET_GENERAL_ERROR`提供一般的警告和錯誤中斷點的預先定義的值。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [BP_ERROR_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-error-resolution-info.md)
- [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)
