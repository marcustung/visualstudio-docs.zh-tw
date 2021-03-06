---
title: IDiaFrameData::get_program | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaFrameData::get_program method
ms.assetid: 9201409e-b4b1-4e2e-a9f8-d17678ac538b
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: d87f5c7fda25a901d44b9f511b9a92eb4471f845
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58939735"
---
# <a name="idiaframedatagetprogram"></a>IDiaFrameData::get_program
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

擷取用來計算目前的函式的呼叫之前設定的暫存器的程式字串。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT get_program (   
   BSTR* pRetVal  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pRetVal`  
 [out]傳回程式字串。  
  
## <a name="return-value"></a>傳回值  
 如果成功，會傳回 `S_OK`。 傳回`S_FALSE`不支援這個屬性，則為。 否則會傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 程式字串是一串巨集，以便建立序言解譯。 例如，典型的堆疊框架可能會使用程式字串`"$T0 $ebp = $eip $T0 4 + ^ = $ebp $T0 ^ = $esp $T0 8 + ="`。 格式為反向波蘭文標記法，其中運算子後面接著運算元。 `T0` 表示在堆疊上的暫存變數。 此範例會執行下列步驟：  
  
1. 將暫存器的內容移`ebp`至`T0`。  
  
2. 新增`4`中的值`T0`產生地址、 從該位址，取得值，以及將值儲存在暫存器`eip`。  
  
3. 從儲存在的位址取值`T0`，並將該值儲存在暫存器`ebp`。  
  
4. 新增`8`中的值`T0`，並將該值儲存在暫存器`esp`。  
  
   請注意，程式字串是特定的 CPU，並設定由目前的堆疊框架的函式的呼叫慣例。  
  
## <a name="see-also"></a>另請參閱  
 [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
