---
title: IDebugPort2::GetPortRequest | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugPort2::GetPortRequest
helpviewer_keywords:
- IDebugPort2::GetPortRequest
ms.assetid: 14abf847-0675-4fa8-872e-971e00c84224
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e8a103316a292c444a35b8c819968d98cda777b6
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678120"
---
# <a name="idebugport2getportrequest"></a>IDebugPort2::GetPortRequest
取得先前用來建立連接埠 （如果有的話） 的連接埠的描述。

## <a name="syntax"></a>語法

```cpp
HRESULT GetPortRequest( 
   IDebugPortRequest2** ppRequest
);
```

```csharp
int GetPortRequest( 
   out IDebugPortRequest2 ppRequest
);
```

#### <a name="parameters"></a>參數
 `ppRequest`

 [out]傳回[IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)物件，表示用來建立連接埠的要求。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  傳回`E_PORT_NO_REQUEST`如果使用未建立連接埠[IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)連接埠要求。

## <a name="see-also"></a>另請參閱
- [IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)
- [IDebugPortRequest2](../../../extensibility/debugger/reference/idebugportrequest2.md)
- [AddPort](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)