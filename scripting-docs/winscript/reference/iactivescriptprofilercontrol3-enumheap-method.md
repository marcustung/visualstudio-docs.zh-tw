---
title: IActiveScriptProfilerControl3::EnumHeap 方法 |Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2799d06d-20dd-4c12-9646-554c0ea3606e
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 6120b8fdd913b4acee2e3ee6774d770aa75b1f5a
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "58147653"
---
# <a name="iactivescriptprofilercontrol3enumheap-method"></a>IActiveScriptProfilerControl3::EnumHeap 方法
傳回的介面 ([IActiveScriptProfilerHeapEnum 介面](../../winscript/reference/iactivescriptprofilerheapenum-interface.md))，可用來逐一查看 GC 堆積物件相關聯的指令碼引擎的內容中。  
  
 您可以呼叫這個方法在任一個偵錯或發行模式。 UI 執行緒閒置時，應該呼叫這個方法。 在呼叫方法之後，應該執行任何作業對指令碼引擎，除了[iactivescriptprofilerheapenum:: Next 方法](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md)直到[iactivescriptprofilerheapenum:: Next 方法](../../winscript/reference/iactivescriptprofilerheapenum-next-method.md)，則傳回 S_FALSE 或[IActiveScriptProfilerHeapEnum 介面](../../winscript/reference/iactivescriptprofilerheapenum-interface.md)釋放介面指標。  
  
## <a name="syntax"></a>語法  
  
```cpp
HRESULT EnumHeap([out] IActiveScriptProfilerHeapEnum** ppEnum);  
```  
  
#### <a name="parameters"></a>參數  
 ppEnum  
 [out]傳回[IActiveScriptProfilerHeapEnum 介面](../../winscript/reference/iactivescriptprofilerheapenum-interface.md)。  
  
## <a name="return-value"></a>傳回值  
 HRESULT。