---
title: 'Idiatable:: Item |Microsoft Docs'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaTable::Item method
ms.assetid: eae11b26-4807-400c-be25-e85bbc0c6b20
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2ad4b51a125af1f08d8766c4c34a2bdd0c54ff64
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47499459"
---
# <a name="idiatableitem"></a>IDiaTable::Item
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

本主題的最新的版本可從[idiatable:: Item](https://docs.microsoft.com/visualstudio/debugger/debug-interface-access/idiatable-item)。  
  
擷取指定的項目資料表中的參考。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT Item (   
   DWORD      index,  
   IUnknown** element  
);  
```  
  
#### <a name="parameters"></a>參數  
 `index`  
 [in]資料表中的項目範圍介於 0 到索引`count`-1，其中`count`會傳回[idiatable:: Get_count](../../debugger/debug-interface-access/idiatable-get-count.md)方法。  
  
 `element`  
 [out]傳回`IUnknown`物件，表示指定的資料表項目。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 資料表代表物件的集合。 根據這些物件的項目參數可以轉換成適當的介面。 例如，如果資料表包含[IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)物件，則項目參數可以轉換成`IDiaSegment`介面。  
  
 它是更常見的方法來呼叫`QueryInterface`方法中的[IDiaTable](../../debugger/debug-interface-access/idiatable.md)適當的列舉程式介面的介面，並使用列舉值的特定方法來存取資料表內容。 請參閱[IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)介面的範例。  
  
## <a name="see-also"></a>另請參閱  
 [IDiaTable](../../debugger/debug-interface-access/idiatable.md)   
 [Idiatable:: Get_count](../../debugger/debug-interface-access/idiatable-get-count.md)   
 [IDiaSegment](../../debugger/debug-interface-access/idiasegment.md)   
 [IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)


