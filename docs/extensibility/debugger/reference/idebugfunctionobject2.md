---
title: IDebugFunctionObject2 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugFunctionObject2 interface
ms.assetid: 56b2fdff-146d-4138-a34c-59a9c65a3ddd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 06505798dcff86507cfc52c4209bf038776f7fac
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60100465"
---
# <a name="idebugfunctionobject2"></a>IDebugFunctionObject2
> [!IMPORTANT]
>  在 Visual Studio 2015 中，這種實作運算式評估工具已被取代。 如需實作 CLR 運算式評估工具的資訊，請參閱[CLR 運算式評估工具](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators)並[Managed 運算式評估工具範例](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample)。

 表示函式，並增強[IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)介面。

## <a name="syntax"></a>語法

```
IDebugFunctionObject2 : IUnknown
```

## <a name="notes-for-implementers"></a>實作者的附註
 運算式評估工具 (EE) 會實作這個介面來表示函式。

## <a name="notes-for-callers"></a>呼叫端資訊
 這個介面的方法，延後的**IDebugFunctionObject**如下：

- **IDebugEvaluate**方法會採用旗標。

- **CreateObject**方法會採用旗標和逾時。

- **CreateStringObjectWithLength**方法會採用的長度。

## <a name="methods"></a>方法
 這個介面會實作下列方法：

|方法|描述|
|------------|-----------------|
|[CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject2-createobject.md)|建立會使用指定評估旗標設定和逾時值的建構函式的物件。|
|[CreateStringObjectWithLength](../../../extensibility/debugger/reference/idebugfunctionobject2-createstringobjectwithlength.md)|建立具有指定的長度的字串物件。|
|[Evaluate](../../../extensibility/debugger/reference/idebugfunctionobject2-evaluate.md)|呼叫函式，並傳回產生的值當做物件。|

## <a name="requirements"></a>需求
 標頭：Ee.h

 命名空間：Microsoft.VisualStudio.Debugger.Interop

 組件︰Microsoft.VisualStudio.Debugger.Interop.dll