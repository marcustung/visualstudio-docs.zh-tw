---
title: IDebugPortPicker::DisplayPortPicker |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- DisplayPortPicker
- IDebugPortPicker::DisplayPortPicker
ms.assetid: 08511ef5-be64-4069-b169-a569cc94bc64
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3dd9317a73800a3886a5a807e9e28b0c24b2301c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58939908"
---
# <a name="idebugportpickerdisplayportpicker"></a>IDebugPortPicker::DisplayPortPicker
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

顯示指定的對話方塊中，可讓使用者選取一個連接埠。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT DisplayPortPicker(  
   HWND hwndParentDialog,  
   BSTR* pbstrPortId  
);  
```  
  
```csharp  
public int DisplayPortPicker(  
   int hwndParentDialog,  
   out string pbstrPortId  
);  
```  
  
#### <a name="parameters"></a>參數  
 `hwndParentDialog`  
 [in]父對話方塊中的控制代碼。  
  
 `pbstrPortId`  
 [out]連接埠識別碼字串。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。 傳回值`S_FALSE`(或傳回值`S_OK`具有`BSTR`設定為`NULL`) 指出使用者已按下**取消**。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugPortPicker](../../../extensibility/debugger/reference/idebugportpicker.md)
