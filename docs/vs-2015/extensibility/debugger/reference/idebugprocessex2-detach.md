---
title: IDebugProcessEx2::Detach | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProcessEx2::Detach
helpviewer_keywords:
- IDebugProcessEx2::Detach method
ms.assetid: 66d54c2c-9302-47c8-9975-f30ed988ab29
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b79f1f80f9b6849c37fc9b6c4c8669f1397f0227
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58945669"
---
# <a name="idebugprocessex2detach"></a>IDebugProcessEx2::Detach
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

這個方法會通知程序工作階段不會再偵錯程序。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT Detach(   
   IDebugSession2* pSession  
);  
```  
  
```csharp  
int Detach(  
   IDebugSession2 pSession  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pSession`  
 [in]值，這個值可唯一識別要卸離此程序的工作階段。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 介面傳入`pSession`是被視為只 cookie，唯一識別工作階段的偵錯管理員原來的值附加至此處理序; 提供的介面上的方法沒有任何功能。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugProcessEx2](../../../extensibility/debugger/reference/idebugprocessex2.md)
