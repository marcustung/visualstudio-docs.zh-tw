---
title: IDebugCodeContext2::GetLanguageInfo | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugCodeContext2::GetLanguageInfo
helpviewer_keywords:
- IDebugCodeContext2::GetLanguageInfo
ms.assetid: 03002ef1-9fe6-44b6-b23b-ef7b86b2b21b
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 0df2a08dd7906b9c4c0935d90150037a3bc0275a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58942138"
---
# <a name="idebugcodecontext2getlanguageinfo"></a>IDebugCodeContext2::GetLanguageInfo
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

取得此程式碼內容的語言資訊。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT GetLanguageInfo(   
   BSTR* pbstrLanguage,  
   GUID* pguidLanguage  
);  
```  
  
```csharp  
int GetLanguageInfo(   
   ref string pbstrLanguage,  
   ref Guid pguidLanguage  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pbstrLanguage`  
 [in、 out]傳回字串，包含名稱的語言，例如"C + +"。  
  
 `pguidLanguage`  
 [in、 out]例如，傳回之語言的程式碼內容，GUID `guidCPPLang`。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 至少其中一個參數必須傳回非 null 值。  
  
## <a name="see-also"></a>另請參閱  
 [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
