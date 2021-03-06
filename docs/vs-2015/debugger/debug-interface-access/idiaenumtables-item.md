---
title: IDiaEnumTables::Item | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumTables::Item method
ms.assetid: d65ab262-10c6-48ce-95a3-b5e4cb2c85af
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 9eec94a5a02eda8fe9b1b3bf8f76f5050ab1e020
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58938793"
---
# <a name="idiaenumtablesitem"></a>IDiaEnumTables::Item
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

擷取透過索引或名稱的資料表。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
HRESULT Item (   
   VARIANT     index,  
   IDiaTable** table  
);  
```  
  
#### <a name="parameters"></a>參數  
 `index`  
 [in]索引或名稱[IDiaTable](../../debugger/debug-interface-access/idiatable.md)要擷取。 如果使用整數變數，則它必須是範圍介於 0 到`count`-1，其中`count`會傳回[idiaenumtables:: Get_count](../../debugger/debug-interface-access/idiaenumtables-get-count.md)方法。  
  
 `table`  
 [out]傳回[IDiaTable](../../debugger/debug-interface-access/idiatable.md)物件，表示所需的資料表。  
  
## <a name="return-value"></a>傳回值  
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。  
  
## <a name="remarks"></a>備註  
 如果指定的字串變數，則字串會命名特定的資料表。 中所定義，名稱應該是其中一個資料表名稱[常數 (偵錯介面存取 SDK)](../../debugger/debug-interface-access/constants-debug-interface-access-sdk.md)。  
  
## <a name="example"></a>範例  
  
```cpp#  
VARIANT var;  
var.vt = VT_BSTR;  
var.bstrVal = SysAllocString(DiaTable_Symbols );  
IDiaTable* pTable;  
pEnumTables->Item( var, &pTable );  
```  
  
## <a name="see-also"></a>另請參閱  
 [IDiaEnumTables](../../debugger/debug-interface-access/idiaenumtables.md)   
 [IDiaTable](../../debugger/debug-interface-access/idiatable.md)   
 [IDiaEnumTables::get_Count](../../debugger/debug-interface-access/idiaenumtables-get-count.md)   
 [常數 (偵錯介面存取 SDK)](../../debugger/debug-interface-access/constants-debug-interface-access-sdk.md)
