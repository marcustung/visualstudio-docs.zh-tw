---
title: IDebugProviderProgramNode2::UnmarshalDebuggeeInterface | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
helpviewer_keywords:
- IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
ms.assetid: 2e4653c5-10f1-493c-9973-f31d266c5d48
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3007d13ec3eae46511e4775497d0aad5b6325b2b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58943193"
---
# <a name="idebugproviderprogramnode2unmarshaldebuggeeinterface"></a>IDebugProviderProgramNode2::UnmarshalDebuggeeInterface
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

跨處理序界限，會取得指定的介面。  
  
## <a name="syntax"></a>語法  
  
```cpp  
HRESULT UnmarshalDebuggeeInterface(  
   REFIID riid,  
   void** ppvObject  
);  
```  
  
```csharp  
int UnmarshalDebuggeeInterface(  
   ref Guid   riid,  
   out IntPtr ppvObject  
);  
```  
  
#### <a name="parameters"></a>參數  
 `riid`  
 [in]若要取得介面的 GUID。  
  
 `ppvObject`  
 [out]傳回實作所需的介面的物件。 [C + +] 這可以直接為所需的介面型別轉換。 [C#] 使用<xref:System.Runtime.InteropServices.Marshal.GetObjectForIUnknown%2A>方法來取得所需的介面。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 當偵錯引擎中執行時，會使用這個方法[!INCLUDE[vsprvs](../../../includes/vsprvs-md.md)]它自己的處理序空間中執行的處理序空間和正在偵錯程式。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugProviderProgramNode2](../../../extensibility/debugger/reference/idebugproviderprogramnode2.md)
