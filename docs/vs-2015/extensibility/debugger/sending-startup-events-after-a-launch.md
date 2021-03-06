---
title: 在啟動後傳送啟動事件 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], startup events
ms.assetid: 306ea0b4-6d9e-4871-8d8d-a4032d422940
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: eeb378b09ffc3e12de8996d7feabbd20a4b40068
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58943053"
---
# <a name="sending-startup-events-after-a-launch"></a>在啟動後傳送啟動事件
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

在偵錯引擎 (DE) 附加至程式中，它會將一系列的啟動事件送回偵錯工作階段中。  
  
 啟動事件，傳送回到偵錯工作階段包含下列各項：  
  
- 引擎建立的事件。  
  
- 程式建立的事件。  
  
- 執行緒建立和模組載入事件。  
  
- 載入完成事件，傳送程式碼時載入並準備好執行之前執行任何程式碼  
  
  > [!NOTE]
  >  當此事件繼續時，會初始化全域變數，並啟動程序執行。  
  
- 可能的其他執行緒建立和模組載入事件。  
  
- 項目點事件，以指示程式這類已達到它的主要進入點**Main**或`WinMain`。 如果 DE 將附加至已在執行程式，不是一般傳送這個事件。  
  
  以程式設計的方式，裝置會先傳送工作階段的偵錯管理員 (SDM) [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md)介面，代表引擎建立事件，後面跟著[IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md)表示程式建立事件。  
  
  這通常後面跟著一或多個[IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md)執行緒建立事件並[IDebugModuleLoadEvent2](../../extensibility/debugger/reference/idebugmoduleloadevent2.md)模組載入事件。  
  
  當程式碼載入並準備好執行但 DE 執行任何程式碼之前，傳送 SDM [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md)載入完整的事件。 最後，如果尚未執行程式，裝置會傳送[IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md)項目點事件，訊號處理程式已達到其主要進入點，並準備好進行偵錯。  
  
## <a name="see-also"></a>另請參閱  
 [控制執行](../../extensibility/debugger/control-of-execution.md)   
 [偵錯工作](../../extensibility/debugger/debugging-tasks.md)
