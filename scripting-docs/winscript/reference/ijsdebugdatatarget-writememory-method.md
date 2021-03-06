---
title: 'Ijsdebugdatatarget:: Writememory 方法 |Microsoft Docs'
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.WriteMemory
apilocation:
- jscript9diag.dll
ms.assetid: 0d3c04c3-9ef8-4842-a145-3d29bca75062
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 622de16cc5f755c5d69059a0e0f28d881121861c
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "58153808"
---
# <a name="ijsdebugdatatargetwritememory-method"></a>IJsDebugDataTarget::WriteMemory 方法
讀取目標處理序的記憶體。  
  
## <a name="syntax"></a>語法  
  
```cpp
HRESULT WriteMemory(  
   UINT64 address,  
   const BYTE *pMemory,  
   DWORD size  
);  
```  
  
#### <a name="parameters"></a>參數  
 `address`  
 [in]要寫入的目標處理序記憶體基底位址。  
  
 `pMemory`  
 [in]要寫入指定的處理序的位址空間中的資料。  
  
 `size`  
 [in]要寫入處理序的位元組數目。  
  
## <a name="return-value"></a>傳回值  
  
## <a name="remarks"></a>備註  
 傳送資料之前，系統會確認基底地址和指定大小的記憶體中的所有資料的寫入權限，可存取，且如果您不能存取，則函數會引發 E_JsDEBUG_INVALID_MEMORY_ADDRESS 錯誤。  
  
## <a name="requirements"></a>需求  
 **標頭：** jscript9diag.h  
  
## <a name="see-also"></a>另請參閱  
 [IJsDebugDataTarget 介面](../../winscript/reference/ijsdebugdatatarget-interface.md)