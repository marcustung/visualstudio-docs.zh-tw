---
title: IDebugStopCompleteEvent2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- IDebugStopCompleteEvent2 interface
ms.assetid: ff3e89f4-61bb-489d-901c-447260100218
caps.latest.revision: 7
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: a9c2a6a6e69bf47751706710801dd78c832ccd2c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58930210"
---
# <a name="idebugstopcompleteevent2"></a>IDebugStopCompleteEvent2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

偵錯引擎 (DE) 在程式停止時，可以傳送這個選擇性事件工作階段的偵錯管理員 (SDM)。  
  
## <a name="syntax"></a>語法  
  
```  
IDebugStopCompleteEvent2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>實作者的附註  
 這是新介面[!INCLUDE[vsprvslong](../../../includes/vsprvslong-md.md)]。 先前的版本不支援非同步停止。  
  
 [停止](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md)SDM 多處理序或多重程式案例中會呼叫。 當某個程式停止將事件傳送到 SDM 時，SDM 會要求太停止其他程式。  
  
 它用來以非同步方式通知程式已停止在 SDM。 這是很有用的解譯器偵錯引擎，有時沒有程式碼執行偵錯的程式內，因此[停止](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md)未以同步方式完成。 如果偵錯引擎想要運用此非同步通知時，它必須傳回`S_ASYNC_STOP`從[停止](../../../extensibility/debugger/reference/idebugengineprogram2-stop.md)。  
  
## <a name="requirements"></a>需求  
 標頭： msdbg.h  
  
 命名空間：Microsoft.VisualStudio.Debugger.Interop  
  
 組件︰Microsoft.VisualStudio.Debugger.Interop.dll
