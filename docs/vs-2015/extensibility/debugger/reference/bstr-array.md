---
title: BSTR_ARRAY | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- BSTR_ARRAY
helpviewer_keywords:
- BSTR_ARRAY structure
ms.assetid: 48da37f7-a237-48a9-9ff9-389c1a00862c
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 912537eb632768b3bcb6543dab098126ce02424f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58945954"
---
# <a name="bstrarray"></a>BSTR_ARRAY
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

結構描述的字串陣列。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
typedef struct tagBSTR_ARRAY {  
   DWORD dwCount;  
   BSTR* Members;  
} BSTR_ARRAY;  
```  
  
```csharp  
struct BSTR_ARRAY {  
   DWORD    dwCount;  
   string[] Members;  
}  
```  
  
## <a name="terms"></a>詞彙  
 dwCount  
 中的字串數目`Members`陣列。  
  
 成員  
 字串陣列。  
  
## <a name="remarks"></a>備註  
 此結構會傳回從[EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md)方法。  
  
 [只有 c + +]每個個別的字串必須使用釋放`SysFreeString`，而`Members`陣列必須釋放與`CoTaskMemFree`。  
  
## <a name="requirements"></a>需求  
 標頭： msdbg.h  
  
 命名空間：Microsoft.VisualStudio.Debugger.Interop  
  
 組件︰Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>另請參閱  
 [結構和等位](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [EnumPersistedPorts](../../../extensibility/debugger/reference/idebugportsupplier3-enumpersistedports.md)
