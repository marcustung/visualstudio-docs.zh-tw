---
title: IDebugExpressionEvaluator::Parse | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugExpressionEvaluator::Parse
helpviewer_keywords:
- IDebugExpressionEvaluator::Parse method
ms.assetid: e6e31b3a-63a7-4293-bcda-267eb78dffb6
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 4039534b139eeeaf20f938c6d6c358c602f96227
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58943827"
---
# <a name="idebugexpressionevaluatorparse"></a>IDebugExpressionEvaluator::Parse
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

這個方法會將剖析的運算式中的運算式字串。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT Parse(   
   LPCOLESTR                upstrExpression,  
   PARSEFLAGS               dwFlags,  
   UINT                     nRadix,  
   BSTR*                    pbstrError,  
   UINT*                    pichError,  
   IDebugParsedExpression** ppParsedExpression  
);  
```  
  
```csharp  
int Parse(  
   string                     upstrExpression,   
   enum_PARSEFLAGS            dwFlags,   
   uint                       nRadix,   
   out string                 pbstrError,   
   out uint                   pichError,   
   out IDebugParsedExpression ppParsedExpression  
);  
```  
  
#### <a name="parameters"></a>參數  
 `upstrExpression`  
 [in]要剖析的運算式字串。  
  
 `dwFlags`  
 [in]集合[PARSEFLAGS](../../../extensibility/debugger/reference/parseflags.md)常數，以判斷要如何剖析運算式。  
  
 `nRadix`  
 [in]用來解譯任何數字資訊的基數。  
  
 `pbstrError`  
 [out]以人類看得懂的文字，會傳回錯誤。  
  
 `pichError`  
 [out]傳回字元位置開始的錯誤中的運算式字串。  
  
 `ppParsedExpression`  
 [out]在剖析的運算式會傳回[IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)物件。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 這個方法會產生剖析的運算式，不是實際的值。 剖析的運算式已準備好進行評估，也就是轉換成值。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugExpressionEvaluator](../../../extensibility/debugger/reference/idebugexpressionevaluator.md)   
 [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)   
 [PARSEFLAGS](../../../extensibility/debugger/reference/parseflags.md)
