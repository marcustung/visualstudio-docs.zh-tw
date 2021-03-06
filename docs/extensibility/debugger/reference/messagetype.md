---
title: MESSAGETYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MESSAGETYPE
helpviewer_keywords:
- MESSAGETYPE enumeration
ms.assetid: 800cc77d-3c27-4763-a9df-552a9384bd49
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 16d2b9ae9c446d4c8082a8c35c9e4d1810233b95
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687506"
---
# <a name="messagetype"></a>MESSAGETYPE
指定訊息類型和原因。

## <a name="syntax"></a>語法

```cpp
enum enum_MESSAGETYPE { 
   MT_OUTPUTSTRING      = 0x0000001,
   MT_MESSAGEBOX        = 0x00000002,
   MT_TYPE_MASK         = 0x000000FF,
   MT_REASON_EXCEPTION  = 0x00000100,
   MT_REASON_TRACEPOINT = 0x00000200,
   MT_REASON_MASK       = 0x0000FF00
};
typedef DWORD MESSAGETYPE;
```

```csharp
public enum enum_MESSAGETYPE { 
   MT_OUTPUTSTRING      = 0x0000001,
   MT_MESSAGEBOX        = 0x00000002,
   MT_TYPE_MASK         = 0x000000FF,
   MT_REASON_EXCEPTION  = 0x00000100,
   MT_REASON_TRACEPOINT = 0x00000200,
   MT_REASON_MASK       = 0x0000FF00
};
```

## <a name="members"></a>成員
 MT_OUTPUTSTRING 表示訊息應傳送至輸出視窗。 這是從互斥`MT_MESSAGEBOX`。

 MT_MESSAGEBOX 指示訊息應該顯示在訊息方塊。 這是從互斥`MT_OUTPUTSTRING`。

 若要找出訊息的目的地 MT_TYPE_MASK 的遮罩值。

 MT_REASON_EXCEPTION 指出訊息方塊顯示在發生例外狀況。 這是從互斥`MT_REASON_TRACEPOINT`。

 MT_REASON_TRACEPOINT 指出訊息方塊顯示因為叫用追蹤點。 這是互斥`MT_REASON_EXCEPTION`。

 若要找出所顯示的訊息的原因 MT_REASON_MASK 的遮罩值。

## <a name="remarks"></a>備註
 會傳回這些值從[GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md)並[GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md)方法。

 其中一個原因值可以結合使用位元的輸出目的地值的其中一個`OR`。

## <a name="requirements"></a>需求
 標頭： msdbg.h

 命名空間：Microsoft.VisualStudio.Debugger.Interop

 組件︰Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>另請參閱
- [列舉](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetMessage](../../../extensibility/debugger/reference/idebugmessageevent2-getmessage.md)
- [GetErrorMessage](../../../extensibility/debugger/reference/idebugerrorevent2-geterrormessage.md)