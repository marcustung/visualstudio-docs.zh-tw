---
title: IEnumDebugCustomAttributes |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumCustomAttributes
helpviewer_keywords:
- IEnumDebugCustomAttributes interface
ms.assetid: 11aa768d-1852-44d6-9de3-17f9bafaded2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: cb0df87f4147fab0dbb356b9699393c5a8e81399
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56695683"
---
# <a name="ienumdebugcustomattributes"></a>IEnumDebugCustomAttributes
列舉自訂屬性。

## <a name="syntax"></a>語法

```
IEnumCustomAttributes : IUnknown
```

## <a name="notes-for-implementers"></a>實作者的附註
 符號提供者會實作這個介面來支援自訂屬性 (透過[IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)介面)。

## <a name="notes-for-callers"></a>呼叫端資訊
- [EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md)傳回此介面。

## <a name="methods-in-vtable-order"></a>依照 Vtable 順序的方法
 下表顯示的方法`IEnumDebugCustomAttributes`。

|方法|描述|
|------------|-----------------|
|[下一步](../../../extensibility/debugger/reference/ienumdebugcustomattributes-next.md)|擷取列舉型別序列中的自訂屬性指定的數目。|
|[Skip](../../../extensibility/debugger/reference/ienumdebugcustomattributes-skip.md)|略過指定的數目的列舉型別序列中的自訂屬性。|
|[Reset](../../../extensibility/debugger/reference/ienumdebugcustomattributes-reset.md)|將列舉型別序列重設到開頭。|
|[Clone](../../../extensibility/debugger/reference/ienumdebugcustomattributes-clone.md)|建立列舉值，包含目前的列舉值相同的列舉型別狀態。|
|[GetCount](../../../extensibility/debugger/reference/ienumdebugcustomattributes-getcount.md)|取得列舉值中的自訂屬性的數目。|

## <a name="requirements"></a>需求
 標頭： sh.h

 命名空間：Microsoft.VisualStudio.Debugger.Interop

 組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [符號提供者介面](../../../extensibility/debugger/reference/symbol-provider-interfaces.md)
- [EnumCustomAttributes](../../../extensibility/debugger/reference/idebugcustomattributequery2-enumcustomattributes.md)
- [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)