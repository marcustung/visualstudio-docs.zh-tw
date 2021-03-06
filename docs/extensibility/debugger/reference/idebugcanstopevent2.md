---
title: IDebugCanStopEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCanStopEvent2
helpviewer_keywords:
- IDebugBreakpointRequest2 interface
ms.assetid: 784bd5b1-4a3f-4455-b313-c4c9a82555a5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 012440e03208fab6bc2cde8814781f7b3a64f79d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56682098"
---
# <a name="idebugcanstopevent2"></a>IDebugCanStopEvent2
此介面用來要求工作階段的偵錯管理員 (SDM) 是否停止在目前的程式碼位置。

## <a name="syntax"></a>語法

```
IDebugCanStopEvent2 : IUknown
```

## <a name="notes-for-implementers"></a>實作者的附註
 偵錯引擎 (DE) 會實作這個介面，以支援 逐步執行原始程式碼。 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)介面必須實作此介面的相同物件上 (使用 SDM [QueryInterface](/cpp/atl/queryinterface)若要存取`IDebugEvent2`介面)。

 這個介面的實作必須與其進行通訊的 SDM 呼叫[CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md)偵錯引擎。 比方說，這可以使用訊息，張貼至偵錯引擎的訊息處理執行緒或實作此介面的物件可以保存的偵錯引擎的參考並使用旗標傳遞至回撥的偵錯引擎`IDebugCanStopEvent2::CanStop`。

## <a name="notes-for-callers"></a>呼叫端資訊
 DE 可以傳送給這個方法會要求繼續執行，以 DE DE 每次會逐步執行程式碼。 此事件會使用傳送[IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)它附加到正在偵錯程式時，在 SDM 所提供的回呼函式。

## <a name="methods-in-vtable-order"></a>依照 Vtable 順序的方法
 下表顯示的方法`IDebugCanStopEvent2`。

|方法|描述|
|------------|-----------------|
|[GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)|取得這個事件的原因。|
|[CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md)|指定正在偵錯程式是否應停止這個事件 （及傳送事件描述停止的原因） 的位置，或就繼續執行。|
|[GetDocumentContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getdocumentcontext.md)|取得描述這個事件的位置的文件內容。|
|[GetCodeContext](../../../extensibility/debugger/reference/idebugcanstopevent2-getcodecontext.md)|取得描述這個事件的位置的程式碼內容。|

## <a name="remarks"></a>備註
 如果使用者逐步執行函式，以 DE 尋找那里無偵錯資訊，或是偵錯資訊存在但是 DE 不知道如果可以顯示該位置的原始程式碼，DE 就會傳送這個介面。

## <a name="requirements"></a>需求
 標頭： msdbg.h

 命名空間：Microsoft.VisualStudio.Debugger.Interop

 組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [IDebugStepCompleteEvent2](../../../extensibility/debugger/reference/idebugstepcompleteevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)