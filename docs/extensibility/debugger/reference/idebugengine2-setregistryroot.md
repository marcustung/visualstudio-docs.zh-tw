---
title: IDebugEngine2::SetRegistryRoot |Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugEngine2::SetRegistryRoot
helpviewer_keywords:
- IDebugEngine2::SetRegistryRoot
ms.assetid: d0d81202-8a4a-4bc3-b297-30a047c5ec60
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2761a8509958c60746f7e5312fa5f5e13631acc7
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56698803"
---
# <a name="idebugengine2setregistryroot"></a>IDebugEngine2::SetRegistryRoot
設定偵錯引擎 (DE) 的登錄根目錄。

## <a name="syntax"></a>語法

```cpp
HRESULT SetRegistryRoot( 
   LPCOLESTR pszRegistryRoot
);
```

```csharp
int SetRegistryRoot( 
   string pszRegistryRoot
);
```

#### <a name="parameters"></a>參數
 `pszRegistryRoot`

 [in]若要使用的登錄根目錄。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="remarks"></a>備註
 這個方法可讓[!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)]來指定替代的登錄根目錄 DE 應該用來取得登錄設定; 例如，"HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\VisualStudio\8.0Exp 」。

## <a name="see-also"></a>另請參閱
- [IDebugEngine2](../../../extensibility/debugger/reference/idebugengine2.md)