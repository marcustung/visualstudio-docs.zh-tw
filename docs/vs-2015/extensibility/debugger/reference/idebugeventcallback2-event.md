---
title: IDebugEventCallback2::Event | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugEventCallback2::Event
helpviewer_keywords:
- IDebugEventCallback2::Event
ms.assetid: e5a3345b-d460-4e40-8f5b-3111c56a2ed9
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 37462b5f274ca6e6c2a4a2feb4083ea94ea2f066
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58942336"
---
# <a name="idebugeventcallback2event"></a>IDebugEventCallback2::Event
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

傳送通知的偵錯事件。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT Event(   
   IDebugEngine2*  pEngine,  
   IDebugProcess2* pProcess,  
   IDebugProgram2* pProgram,  
   IDebugThread2*  pThread,  
   IDebugEvent2*   pEvent,  
   REFIID          riidEvent,  
   DWORD           dwAttrib  
);  
```  
  
```csharp  
int Event(   
   IDebugEngine2  pEngine,  
   IDebugProcess2 pProcess,  
   IDebugProgram2 pProgram,  
   IDebugThread2  pThread,  
   IDebugEvent2   pEvent,  
   ref Guid       riidEvent,  
   uint           dwAttrib  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pEngine`  
 [in][IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)物件，表示正在傳送這個事件的偵錯引擎 (DE)。 規定，才能填入此參數。  
  
 `pProcess`  
 [in][IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)物件，表示發生事件的程序。 此參數會填入工作階段的偵錯管理員 (SDM)。 DE 一律會傳遞此參數的 null 值。  
  
 `pProgram`  
 [in][IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)物件，表示的程式發生此事件。 對於大多數事件，此參數不是 null 的值。  
  
 `pThread`  
 [in][IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)物件，表示發生此事件的執行緒。 停止事件，此參數不能堆疊框架取自此參數為 null 值。  
  
 `pEvent`  
 [in][IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)物件，代表偵錯事件。  
  
 `riidEvent`  
 [in]GUID，識別哪些事件介面，以取得從`pEvent`參數。  
  
 `dwAttrib`  
 [in]從旗標的組合[EVENTATTRIBUTES](../../../extensibility/debugger/reference/eventattributes.md)列舉型別。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 呼叫這個方法時`dwAttrib`參數必須符合從傳回的值[GetAttributes](../../../extensibility/debugger/reference/idebugevent2-getattributes.md)方法，如事件物件上呼叫傳入`pEvent`參數。  
  
 所有偵錯事件是以非同步方式張貼，不論事件本身是否為非同步。 當 DE 呼叫這個方法時，傳回的值不會指出是否處理事件，僅是否收到事件。 事實上，在大部分情況下，事件尚未處理此方法傳回時。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)   
 [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)   
 [IDebugProcess2](../../../extensibility/debugger/reference/idebugprocess2.md)   
 [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)   
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)   
 [EVENTATTRIBUTES](../../../extensibility/debugger/reference/eventattributes.md)
