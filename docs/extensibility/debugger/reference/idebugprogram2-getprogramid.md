---
title: IDebugProgram2::GetProgramId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::GetProgramId
helpviewer_keywords:
- IDebugProgram2::GetProgramId
ms.assetid: 2c31c0aa-2b71-46c7-849c-356e237d26f8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a3dfec12193efda49a520a40418b93f2d4cef6b1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712888"
---
# <a name="idebugprogram2getprogramid"></a>IDebugProgram2::GetProgramId
取得此程式的 GUID。

## <a name="syntax"></a>語法

```cpp
HRESULT GetProgramId( 
   GUID* pguidProgramId
);
```

```csharp
int GetProgramId( 
   out Guid pguidProgramId
);
```

#### <a name="parameters"></a>參數
 `pguidProgramId`

 [out]傳回`GUID`此計劃。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 偵錯引擎 (DE) 必須傳回原本傳遞至程式識別碼[OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md)或是[附加](../../../extensibility/debugger/reference/idebugengine2-attach.md)方法。 這可讓程式識別在偵錯工具元件。

## <a name="see-also"></a>另請參閱
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [OnAttach](../../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)