---
title: CANSTOP_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CANSTOP_REASON
helpviewer_keywords:
- CANSTOP_REASON enumeration
ms.assetid: 6da944eb-36cd-4a8c-8d71-544c775cfcc1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bbc4143c61a0223fe3940b4167748727d1ebd560
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56711614"
---
# <a name="canstopreason"></a>CANSTOP_REASON
用來判斷是否程式可能會停止在達到執行中的特定點之後執行。

## <a name="syntax"></a>語法

```cpp
enum enum_CANSTOP_REASON {
    CANSTOP_ENTRYPOINT = 0x0000,
    CANSTOP_STEPIN     = 0x0001
};
typedef DWORD CANSTOP_REASON;
```

```csharp
public enum enum_CANSTOP_REASON {
    CANSTOP_ENTRYPOINT = 0x0000,
    CANSTOP_STEPIN     = 0x0001
};
```

## <a name="members"></a>成員
CANSTOP_ENTRYPOINT 指定特定程式的進入點。

CANSTOP_STEPIN 指定逐步執行函式。

## <a name="remarks"></a>備註
作為引數[GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)方法，以確認與工作階段進行偵錯管理員 (SDM)，如果可以停止或逐步執行函式或方法之後到達該程式的進入點。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)
