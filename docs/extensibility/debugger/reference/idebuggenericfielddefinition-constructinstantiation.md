---
title: IDebugGenericFieldDefinition::ConstructInstantiation | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- ConstructInstantiation
- IDebugGenericFieldDefinition::ConstructInstantiation
ms.assetid: ef8ae261-a98b-4dc2-93b3-7c5191818ba2
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 8c2fc6b9b7683180c3a9c3f2aa967ba171a48097
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56690678"
---
# <a name="idebuggenericfielddefinitionconstructinstantiation"></a>IDebugGenericFieldDefinition::ConstructInstantiation
建構指定型別引數陣列的欄位執行個體。

## <a name="syntax"></a>語法

```cpp
HRESULT ConstructInstantiation(
   ULONG32       cArgs,
   IDebugField** ppArgs,
   IDebugField** ppConstructedField
);
```

```csharp
int ConstructInstantiation(
   uint            cArgs,
   IDebugField[]   ppArgs,
   out IDebugField ppConstructedField
);
```

#### <a name="parameters"></a>參數
 `cArgs`

 [in]中的引數`ppArgs`陣列。

 `ppArgs`

 [in]包含型別引數的陣列。 型別引數必須是封閉式的型別 （非泛型或完整具現化泛型）。

 `ppConstructedField`

 [out]傳回[IDebugField](../../../extensibility/debugger/reference/idebugfield.md)介面，表示新的欄位。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 不會檢查條件約束。

## <a name="see-also"></a>另請參閱
- [IDebugGenericFieldDefinition](../../../extensibility/debugger/reference/idebuggenericfielddefinition.md)