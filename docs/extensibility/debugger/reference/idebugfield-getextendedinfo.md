---
title: IDebugField::GetExtendedInfo | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugField::GetExtendedInfo
helpviewer_keywords:
- IDebugField::GetExtendedInfo method
ms.assetid: 46c0dd4d-4fd5-4efd-a908-71e4248e8e8d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0321dfbdc719d8e155bb1ee035032e2862bb90e0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56679043"
---
# <a name="idebugfieldgetextendedinfo"></a>IDebugField::GetExtendedInfo
這個方法取得擴充欄位的相關資訊。

## <a name="syntax"></a>語法

```cpp
HRESULT GetExtendedInfo( 
   REFGUID guidExtendedInfo,
   BYTE**  prgBuffer,
   DWORD*  pdwLen
);
```

```csharp
int GetExtendedInfo(
   ref Guid guidExtendedInfo,
   IntPtr[] prgBuffer,
   ref uint pdwLen
);
```

#### <a name="parameters"></a>參數
 `guidExtendedInfo`

 [in]選取要傳回的資訊。 有效值為：

|值|描述|
|-----------|-----------------|
|`guidConstantValue`|以一連串的位元組值。|
|`guidConstantType`|做為型別簽章類型。|

 `prgBuffer`

 [out]傳回擴充的資訊。

 `pdwLen`

 [in、 out]會傳回大小的擴充的資訊，以位元組為單位。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 目前，這個方法只會傳回型別或常數的值。 呼叫端必須釋放中傳回的緩衝區`prgBuffer`藉由呼叫 COM 的`CoTaskMemFree`函式 （c + +） 或<xref:System.Runtime.InteropServices.Marshal.FreeCoTaskMem%2A>(C#)。

## <a name="see-also"></a>另請參閱
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)