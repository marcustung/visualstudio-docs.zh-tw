---
title: IDebugThread2::GetLogicalThread | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::GetLogicalThread
helpviewer_keywords:
- IDebugThread2::GetLogicalThread
ms.assetid: bce6230e-41d4-49b7-a050-2dde5efb6805
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 99e8dbd78ef262479fbc8405b77fa0cf53f8087a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56723288"
---
# <a name="idebugthread2getlogicalthread"></a>IDebugThread2::GetLogicalThread
偵錯引擎不會實作這個方法。

## <a name="syntax"></a>語法

```cpp
HRESULT GetLogicalThread( 
   IDebugStackFrame2*     pStackFrame,
   IDebugLogicalThread2** ppLogicalThread
);
```

```csharp
int GetLogicalThread( 
   IDebugStackFrame2        pStackFrame,
   out IDebugLogicalThread2 ppLogicalThread
);
```

#### <a name="parameters"></a>參數
 `pStackFrame`

 [in][IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md)物件，代表堆疊框架。

 `ppLogicalThread`

 [out]傳回`IDebugLogicalThread2`介面，表示相關聯的邏輯執行緒。 偵錯引擎實作應該將此設定為 null 值。

## <a name="return-value"></a>傳回值
 偵錯引擎實作永遠會傳回`E_NOTIMPL`。

## <a name="see-also"></a>另請參閱
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)