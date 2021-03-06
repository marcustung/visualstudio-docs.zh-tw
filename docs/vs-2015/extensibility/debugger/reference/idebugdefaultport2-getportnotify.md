---
title: IDebugDefaultPort2::GetPortNotify | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugDefaultPort2::GetPortNotify
helpviewer_keywords:
- IDebugDefaultPort2::GetPortNotify
ms.assetid: 3ae715ee-9886-4694-a52b-59bb3b27467a
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c0f5b1faf000ef982e38736b3cd3ea89a1dc2dc0
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58942988"
---
# <a name="idebugdefaultport2getportnotify"></a>IDebugDefaultPort2::GetPortNotify
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

這個方法會取得[IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md)介面，此連接埠。  
  
## <a name="syntax"></a>語法  
  
```cpp  
HRESULT GetPortNotify(  
   IDebugPortNotify2** ppPortNotify  
);  
```  
  
```csharp  
int GetPortNotify(  
   out IDebugPortNotify2 ppPortNotify  
);  
```  
  
#### <a name="parameters"></a>參數  
 `ppPortNotify`  
 [out][IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md)物件。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 通常`QueryInterface`物件，實作上呼叫方法[IDebugPort2](../../../extensibility/debugger/reference/idebugport2.md)介面，以取得[IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md)介面。 不過，有在程式所需的介面實作的不同物件的情況。 這個方法會隱藏這些情況下，並傳回`IDebugPortNotify2`介面最適當的物件。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugDefaultPort2](../../../extensibility/debugger/reference/idebugdefaultport2.md)   
 [IDebugPortNotify2](../../../extensibility/debugger/reference/idebugportnotify2.md)
