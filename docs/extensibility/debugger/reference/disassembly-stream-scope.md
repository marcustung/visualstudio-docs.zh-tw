---
title: DISASSEMBLY_STREAM_SCOPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DISASSEMBLY_STREAM_SCOPE
helpviewer_keywords:
- DISASSEMBLY_STREAM_SCOPE enumeration
ms.assetid: 43e2b364-cbbe-4755-a7e6-a03f3054c965
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 446b0eec7593457ed2cd384eb9a6bca383094e62
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56684490"
---
# <a name="disassemblystreamscope"></a>DISASSEMBLY_STREAM_SCOPE
指定反組譯碼資料流的範圍。

## <a name="syntax"></a>語法

```cpp
enum enum_DISASSEMBLY_STREAM_SCOPE {
    DSS_HUGE     = 0x10000000,
    DSS_FUNCTION = 0x0001,
    DSS_MODULE   = (DSS_HUGE) | 0x0002,
    DSS_ALL      = (DSS_HUGE) | 0x0003
};
typedef DWORD DISASSEMBLY_STREAM_SCOPE;
```

```csharp
public enum enum_DISASSEMBLY_STREAM_SCOPE {
    DSS_HUGE     = 0x10000000,
    DSS_FUNCTION = 0x0001,
    DSS_MODULE   = (DSS_HUGE) | 0x0002,
    DSS_ALL      = (DSS_HUGE) | 0x0003
};
```

## <a name="members"></a>成員
DSS_HUGE 指定反組譯程式碼內容會產生更多的輸出，比用戶端通常會想要擷取的單一呼叫中。

DSS_FUNCTION 指定應該要解譯的程式碼內容所包含的函式。 指定反組譯碼資料流時所傳回代表函式[GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)方法。

所傳回的 DSS_MODULE 時`IDebugDisassemblyStream2::GetScope`方法，可讓您指定的反組譯碼資料流表示的模組。

DSS_ALL 指定反組譯碼的整個位址空間。

## <a name="remarks"></a>備註
作為引數[GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)方法，並由傳回[GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)方法。

這些值可能會合併的位元`OR`。

## <a name="requirements"></a>需求
標頭： msdbg.h

命名空間：Microsoft.VisualStudio.Debugger.Interop

組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetDisassemblyStream](../../../extensibility/debugger/reference/idebugprogram2-getdisassemblystream.md)
- [GetScope](../../../extensibility/debugger/reference/idebugdisassemblystream2-getscope.md)
