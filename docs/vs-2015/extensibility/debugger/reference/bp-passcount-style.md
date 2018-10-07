---
title: BP_PASSCOUNT_STYLE |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- BP_PASSCOUNT_STYLE
helpviewer_keywords:
- BP_PASSCOUNT_STYLE structure
ms.assetid: 0a647047-e2d5-4724-a0b8-68108425ecad
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 3c5a505df625b6ac787f1c13a84e11eddb4d8e7a
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47489407"
---
# <a name="bppasscountstyle"></a>BP_PASSCOUNT_STYLE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

本主題的最新的版本可從[BP_PASSCOUNT_STYLE](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/bp-passcount-style)。  
  
指定會導致引發中斷點的中斷點傳遞計數相關聯的條件。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
enum enum_BP_PASSCOUNT_STYLE {   
   BP_PASSCOUNT_NONE             = 0x0000,  
   BP_PASSCOUNT_EQUAL            = 0x0001,  
   BP_PASSCOUNT_EQUAL_OR_GREATER = 0x0002,  
   BP_PASSCOUNT_MOD              = 0x0003  
};  
typedef DWORD BP_PASSCOUNT_STYLE;  
```  
  
```csharp  
public enum enum_BP_PASSCOUNT_STYLE {   
   BP_PASSCOUNT_NONE             = 0x0000,  
   BP_PASSCOUNT_EQUAL            = 0x0001,  
   BP_PASSCOUNT_EQUAL_OR_GREATER = 0x0002,  
   BP_PASSCOUNT_MOD              = 0x0003  
};  
```  
  
## <a name="members"></a>成員  
 BP_PASSCOUNT_NONE  
 不指定任何中斷點傳遞計數樣式。  
  
 BP_PASSCOUNT_EQUAL  
 設定為等於中斷點傳遞計數的樣式。 中斷點叫用次數等於傳遞計數時，就會引發中斷點。  
  
 BP_PASSCOUNT_EQUAL_OR_GREATER  
 將中斷點傳遞計數樣式設定為等於或大於。 中斷點叫用次數等於或大於傳遞計數時，就會引發中斷點。  
  
 BP_PASSCOUNT_MOD  
 指定模數傳遞計數。 比方說，如果傳遞計數為型別的`BP_PASSCOUNT_MOD`和傳遞計數值為 4，每次叫用的次數是 4 的倍數，中斷點會引發。  
  
## <a name="remarks"></a>備註  
 用於`stylePassCount`隸屬[BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)結構，這又是隸屬[BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)並[BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)結構。  
  
## <a name="requirements"></a>需求  
 標頭： msdbg.h  
  
 命名空間： Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>另請參閱  
 [列舉型別](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)   
 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)   
 [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
