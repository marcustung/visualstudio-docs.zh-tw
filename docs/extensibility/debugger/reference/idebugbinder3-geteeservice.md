---
title: IDebugBinder3::GetEEService | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder3::GetEEService
helpviewer_keywords:
- IDebugBinder3::GetEEService method
ms.assetid: eb07aa40-8cd9-4a52-a4c7-4affd2307a01
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3d709124a392ffb6b6cbbb5a29576a985fe6d0f2
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56700129"
---
# <a name="idebugbinder3geteeservice"></a>IDebugBinder3::GetEEService
這個方法會傳回要求的服務。

## <a name="syntax"></a>語法

```cpp
HRESULT GetEEService(
   [in] GUID        vendor,
   [in] GUID        language,
   [in] GUID        iid,
   [out] IUnknown** ppService
);
```

```csharp
Int GetEEService(
   Guid       vendor,
   Guid       language,
   Guid       iid,
   out object ppService
);
```

#### <a name="parameters"></a>參數
 `vendor`

 [in]`GUID` （null 的值是可接受的） 之供應商。

 `language`

 [in]`GUID`的 （null 的值是可接受） 的語言。

 `iid`

 [in]`IID`要取得的服務。

 `ppService`

 [out]要求的服務介面。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 傳遞`IID`for [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)介面 (`IID_IEEVisualizerServiceProvider`) 類型視覺化檢視服務是否可用。 如果運算式評估工具可以取得的話[IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)介面，以支援類型視覺化檢視。 請參閱[視覺化及檢視資料](../../../extensibility/debugger/visualizing-and-viewing-data.md)如需詳細資訊。

## <a name="see-also"></a>另請參閱
- [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)
- [IEEVisualizerServiceProvider](../../../extensibility/debugger/reference/ieevisualizerserviceprovider.md)
- [IEEVisualizerService](../../../extensibility/debugger/reference/ieevisualizerservice.md)
- [視覺化及檢視資料](../../../extensibility/debugger/visualizing-and-viewing-data.md)