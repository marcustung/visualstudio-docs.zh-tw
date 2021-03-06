---
title: IDebugParsedExpression::EvaluateSync | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugParsedExpression::EvaluateSync
helpviewer_keywords:
- IDebugParsedExpression::EvaluateSync method
ms.assetid: 0ea04cfa-de87-4b6c-897e-4572c1a28942
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ea659b847149a6abb2c3a5ba7cc947a59c7ae41c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56709638"
---
# <a name="idebugparsedexpressionevaluatesync"></a>IDebugParsedExpression::EvaluateSync
這個方法會評估剖析的運算式，並選擇性地將轉換成另一個資料類型的結果。

## <a name="syntax"></a>語法

```cpp
HRESULT EvaluateSync( 
   DWORD                 dwEvalFlags,
   DWORD                 dwTimeout,
   IDebugSymbolProvider* pSymbolProvider,
   IDebugAddress*        pAddress,
   IDebugBinder*         pBinder,
   BSTR                  bstrResultType,
   IDebugProperty2**     ppResult
);
```

```csharp
int EvaluateSync(
   uint                 dwEvalFlags,
   uint                 dwTimeout,
   IDebugSymbolProvider pSymbolProvider,
   IDebugAddress        pAddress,
   IDebugBinder         pBinder,
   string               bstrResultType,
   out IDebugProperty2  ppResult
);
```

#### <a name="parameters"></a>參數
 `dwEvalFlags`

 [in]組合[EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md)控制要如何評估運算式的常數。

 `dwTimeout`

 [in]指定的時間上限，以毫秒為單位，從這個方法返回之前等候。 使用`INFINITE`無限期等候。

 `pSymbolProvider`

 [in]符號提供者，以表示[IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)介面。

 `pAddress`

 [in]在方法中，以表示目前的執行位置[IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)介面。

 `pBinder`

 [in]繫結器，以表示[IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)介面。

 `bstrResultType`

 [in]結果的類型應該轉換成。 這個引數可以是 null 值。

 `ppResult`

 [out]傳回[IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)介面，表示評估的結果。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 運算式評估內容由指定`pAddress`這讓您能夠判斷所包含的方法，然後使用語言範圍規則來決定在運算式中的符號的值。

## <a name="see-also"></a>另請參閱
- [IDebugSymbolProvider](../../../extensibility/debugger/reference/idebugsymbolprovider.md)
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugAddress](../../../extensibility/debugger/reference/idebugaddress.md)
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)
- [IDebugParsedExpression](../../../extensibility/debugger/reference/idebugparsedexpression.md)