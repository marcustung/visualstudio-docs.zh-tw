---
title: IEnumDebugCodeContexts::Reset | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IEnumDebugCodeContexts.Reset
apilocation:
- jscript.dll
helpviewer_keywords:
- IEnumDebugCodeContexts::Reset
ms.assetid: b7042fac-9f45-46ee-a024-81fed73b0762
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 756ed93f774419f33bc721429ea3e3bb605577df
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "58157577"
---
# <a name="ienumdebugcodecontextsreset"></a>IEnumDebugCodeContexts::Reset
將列舉型別序列重設到開頭。  
  
## <a name="syntax"></a>語法  
  
```cpp
HRESULT Reset();  
```  
  
#### <a name="parameters"></a>參數  
 這個方法會接受任何參數。  
  
## <a name="return-value"></a>傳回值  
 方法會傳回 `HRESULT`。 可能的值包括 (但不限於) 下表中的這些值。  
  
|值|描述|  
|-----------|-----------------|  
|`S_OK`|方法成功。|  
  
## <a name="remarks"></a>備註  
 這個方法會將列舉型別序列重設開頭。  
  
## <a name="see-also"></a>另請參閱  
 [IEnumDebugCodeContexts 介面](../../winscript/reference/ienumdebugcodecontexts-interface.md)