---
title: IDebugOutputStringEvent2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugOutputStringEvent2
helpviewer_keywords:
- IDebugOutputStringEvent2 interface
ms.assetid: 86596fd1-cecc-4813-8add-dc3d70068f9b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: dfce52f89e75c8e9e697a3fa5ad4184c3d1fa42b
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56721976"
---
# <a name="idebugoutputstringevent2"></a>IDebugOutputStringEvent2
這個介面是由偵錯引擎 (DE) 中，工作階段的偵錯管理員 (SDM) 傳送至輸出字串。

## <a name="syntax"></a>語法

```
IDebugOutputStringEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>實作者的附註
 DE 實作此介面傳送字串至**輸出**在 IDE 的視窗。 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)介面必須實作此介面的相同物件上。 使用 SDM [QueryInterface](/cpp/atl/queryinterface)若要存取`IDebugEvent2`介面。

## <a name="notes-for-callers"></a>呼叫端資訊
 DE 會建立並傳送這個事件来傳送物件的字串**輸出**視窗。 事件會使用傳送[IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)附加至正在進行偵錯程式時，會將 SDM 所提供的回呼函式。

## <a name="methods-in-vtable-order"></a>依照 Vtable 順序的方法
 下表顯示的方法`IDebugOutputStringEvent2`。

|方法|描述|
|------------|-----------------|
|[GetString](../../../extensibility/debugger/reference/idebugoutputstringevent2-getstring.md)|取得可顯示的訊息。|

## <a name="remarks"></a>備註
 比方說，在 unmanaged 程式碼，來輸出字串產生時進行偵錯的程式會傳送字串至 Win32`OutputDebugString`函式。 此字串是 DE 遭到攔截，傳送至為 SDM`IDebugOutputStringEvent2`事件。

 使用[IDebugMessageEvent2](../../../extensibility/debugger/reference/idebugmessageevent2.md)傳送需要使用者回應的訊息。

 使用[IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md)傳送錯誤訊息，不需要回應。

## <a name="requirements"></a>需求
 標頭： msdbg.h

 命名空間：Microsoft.VisualStudio.Debugger.Interop

 組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [IDebugMessageEvent2](../../../extensibility/debugger/reference/idebugmessageevent2.md)
- [IDebugErrorEvent2](../../../extensibility/debugger/reference/idebugerrorevent2.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)