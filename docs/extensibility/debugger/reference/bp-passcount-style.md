---
title: BP_PASSCOUNT_STYLE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_PASSCOUNT_STYLE
helpviewer_keywords:
- BP_PASSCOUNT_STYLE structure
ms.assetid: 0a647047-e2d5-4724-a0b8-68108425ecad
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 809c63fe536166efe0779cd4e4dc0149b219390a
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56686050"
---
# <a name="bppasscountstyle"></a>BP_PASSCOUNT_STYLE
指定會導致引發中斷點的中斷點傳遞計數相關聯的條件。

## <a name="syntax"></a>語法

```cpp
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
BP_PASSCOUNT_NONE 指定任何中斷點傳遞計數樣式。

BP_PASSCOUNT_EQUAL 中斷點傳遞計數樣式設定為等於。 中斷點叫用次數等於傳遞計數時，就會引發中斷點。

BP_PASSCOUNT_EQUAL_OR_GREATER 中斷點傳遞計數樣式設定為等於或大於。 中斷點叫用次數等於或大於傳遞計數時，就會引發中斷點。

指定 BP_PASSCOUNT_MOD 模數傳遞計數。 比方說，如果傳遞計數為型別的`BP_PASSCOUNT_MOD`和傳遞計數值為 4，每次叫用的次數是 4 的倍數，中斷點會引發。

## <a name="remarks"></a>備註
用於`stylePassCount`隸屬[BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)結構，這又是隸屬[BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)並[BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)結構。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)
- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)
- [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)
