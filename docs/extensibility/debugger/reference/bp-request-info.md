---
title: BP_REQUEST_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_REQUEST_INFO
helpviewer_keywords:
- BP_REQUEST_INFO structure
ms.assetid: 42a31412-5b6b-47fe-a762-0c2bc769e1cc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 54af482e8896ce1905700312e59bd156c40b556d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56697815"
---
# <a name="bprequestinfo"></a>BP_REQUEST_INFO
包含中斷點的實作所需的資訊。

## <a name="syntax"></a>語法

```cpp
typedef struct _BP_REQUEST_INFO {
    BPREQI_FIELDS   dwFields;
    GUID            guidLanguage;
    BP_LOCATION     bpLocation;
    IDebugProgram2* pProgram;
    BSTR            bstrProgramName;
    IDebugThread2*  pThread;
    BSTR            bstrThreadName;
    BP_CONDITION    bpCondition;
    BP_PASSCOUNT    bpPassCount;
    BP_FLAGS        dwFlags;
} BP_REQUEST_INFO;
```

```csharp
public struct BP_REQUEST_INFO {
    public uint           dwFields;
    public Guid           guidLanguage;
    public BP_LOCATION    bpLocation;
    public IDebugProgram2 pProgram;
    public string         bstrProgramName;
    public IDebugThread2  pThread;
    public string         bstrThreadName;
    public BP_CONDITION   bpCondition;
    public BP_PASSCOUNT   bpPassCount;
    public uint           dwFlags;
};
```

## <a name="members"></a>成員
`dwFields` 從旗標的組合[BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)列舉，指定哪些欄位都已填寫。

`guidLanguage` 語言 GUID。

`bpLocation` [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)結構，指定之中斷點位置的類型。

`pProgram` [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)物件，表示中斷點發生的應用程式。

`bstrProgramName` 中斷點會發生在應用程式的名稱。

`pThread` [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)物件，表示中斷點發生的執行緒。

`bstrThreadName` 中斷點會發生執行緒的名稱。

`bpCondition` [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)結構，描述在其下會引發中斷點的條件。

`bpPassCount` [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)結構，其中包含中斷點的傳遞計數資訊。

`dwFlags` 從旗標的組合[BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md)指定要求之中斷點的旗標的列舉型別。

## <a name="remarks"></a>備註
此結構由[GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md)方法。

如果您需要取得偵錯引擎廠商的 GUID，中斷點條件約束或追蹤點，請參閱[BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)結構。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [結構和等位](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetRequestInfo](../../../extensibility/debugger/reference/idebugbreakpointrequest2-getrequestinfo.md)
- [BPREQI_FIELDS](../../../extensibility/debugger/reference/bpreqi-fields.md)
- [BP_LOCATION](../../../extensibility/debugger/reference/bp-location.md)
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)
- [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)
- [BP_FLAGS](../../../extensibility/debugger/reference/bp-flags.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
