---
title: IDebugExceptionEvent2::PassToDebuggee |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugExceptionEvent2::PassToDebuggee
helpviewer_keywords:
- IDebugExceptionEvent2::PassToDebuggee
ms.assetid: a20d0f0b-2ca0-4437-bd22-9213c81d2738
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: ecc7eb3830522cdee0022f4193482daab3780230
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58942473"
---
# <a name="idebugexceptionevent2passtodebuggee"></a>IDebugExceptionEvent2::PassToDebuggee
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

指定例外狀況應該傳遞給正在偵錯程式時繼續執行，或如果例外狀況應予捨棄。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT PassToDebuggee(  
   BOOL fPass  
);  
```  
  
```csharp  
int PassToDebuggee(  
   int fPass  
);  
```  
  
#### <a name="parameters"></a>參數  
 `fPass`  
 [in]非零值 (`TRUE`) 如果例外狀況應該傳遞給正在偵錯程式時繼續執行，則為零 (`FALSE`) 如果例外狀況應予捨棄。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 呼叫這個方法並不會實際會執行所偵錯的程式中的任何程式碼。 呼叫只是設定為下一個程式碼執行狀態。 例如，呼叫[CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)方法可能會傳回`S_OK`具有[EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md)。`dwState` 欄位設定為`EXCEPTION_STOP_SECOND_CHANCE`。  
  
 IDE 可能會收到[IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)事件，並呼叫[繼續](../../../extensibility/debugger/reference/idebugprogram2-continue.md)方法。 偵錯引擎 (DE) 應有的預設行為，可處理則`PassToDebuggee`不會呼叫方法。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)   
 [CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)   
 [Continue](../../../extensibility/debugger/reference/idebugprogram2-continue.md)
