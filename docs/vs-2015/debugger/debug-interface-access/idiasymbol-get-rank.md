---
title: 'Idiasymbol:: Get_rank |Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_rank method
ms.assetid: 14cc9c4b-a5ec-414a-b01f-4a142c17b7cc
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 5574f0c2a5e6b5d1b75a85e74faceb18e99216e8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58940122"
---
# <a name="idiasymbolgetrank"></a>IDiaSymbol::get_rank
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

擷取 FORTRAN 多維陣列的陣序 （維度數目）。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT get_rank (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pRetVal`  
 [out]FORTRAN 多維陣列中傳回維度的數目。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。  
  
> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。  
  
## <a name="remarks"></a>備註  
 陣序規範是指的陣列會宣告為陣列中的維度數目`myarray[1,2,3]`。 此範例中有 3 和 3 個維度的順位。 陣序規範不適用於 c + + 會使用每個維度的陣列的陣列的概念 (亦即`myarray[1][2][3]`)。  
  
## <a name="see-also"></a>另請參閱  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
