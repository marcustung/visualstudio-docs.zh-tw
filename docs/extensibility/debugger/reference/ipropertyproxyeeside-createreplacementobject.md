---
title: IPropertyProxyEESide::CreateReplacementObject |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IPropertyProxyEESide::CreateReplacementObject
helpviewer_keywords:
- IPropertyProxyEESide::CreateReplacementObject
ms.assetid: 0cfe79b8-c3f1-48b0-a225-e39dee2c92fe
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 03bfeeb30fad4f332a3a747dcf8468c4fb39ef56
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704198"
---
# <a name="ipropertyproxyeesidecreatereplacementobject"></a>IPropertyProxyEESide::CreateReplacementObject
建立特定運算式評估工具 (EE) 的資料物件的複本。

## <a name="syntax"></a>語法

```cpp
HRESULT CreateReplacementObject(
   IEEDataStorage*  dataIn,
   IEEDataStorage** dataOut
);
```

```csharp
int CreateReplacementObject(
   IEEDataStorage     dataIn,
   out IEEDataStorage dataOut
);
```

#### <a name="parameters"></a>參數
 `dataIn`

 [in][IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)含有要複製資料的物件。

 `dataOut`

 [out]傳回新`IEEDataStorage`物件。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 這個方法會獲得[IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)物件，表示為位元組陣列。 此內送的資料物件通常不會實作由 EE。 不過，這個方法所傳回的物件一律藉由 EE，它可讓 EE 實作`IEEDataStorage`上想要使用任何類別的介面。

 請注意資料提供傳入`IEEDataStorage`物件必須是相同的資料，在傳出`IEEDataStorage`物件。

## <a name="see-also"></a>另請參閱
- [IPropertyProxyEESide](../../../extensibility/debugger/reference/ipropertyproxyeeside.md)
- [IEEDataStorage](../../../extensibility/debugger/reference/ieedatastorage.md)