---
title: 'Idiasymbol:: Get_machinetype |Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_machineType method
ms.assetid: 30870b10-6f32-45c6-a0d7-020dea707710
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a409f914edd7832f5bf8429ebd740746e65047ac
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58940253"
---
# <a name="idiasymbolgetmachinetype"></a>IDiaSymbol::get_machineType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

擷取目標 CPU 的類型。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT get_machineType (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>參數  
 `pRetVal`  
 [out]傳回值，以從[CV_CPU_TYPE_e 列舉](../../debugger/debug-interface-access/cv-cpu-type-e.md)指定的目標 CPU 類型的列舉型別。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回`S_FALSE`或錯誤碼。  
  
> [!NOTE]
>  傳回值為`S_FALSE`表示此屬性不適用於符號。  
  
## <a name="see-also"></a>另請參閱  
 [CV_CPU_TYPE_e Enumeration](../../debugger/debug-interface-access/cv-cpu-type-e.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
