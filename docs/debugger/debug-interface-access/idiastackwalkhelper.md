---
title: IDiaStackWalkHelper | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2 interface
ms.assetid: d66e5c84-565d-494e-8486-f91db9a34548
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0143945a266b9c76fefa10e1823a7c3ce01f85e7
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56622367"
---
# <a name="idiastackwalkhelper"></a>IDiaStackWalkHelper
可加速查核堆疊使用的程式偵錯資料庫 (.pdb) 檔案。

## <a name="syntax"></a>語法

```

IDiaStackWalkHelper: IUnknown

```

## <a name="methods-in-vtable-order"></a>依照 Vtable 順序的方法
 下表顯示的方法`IDiaStackWalkHelper`:

|方法|說明|
|------------|-----------------|
|[IDiaStackWalkHelper::get_registerValue](../../debugger/debug-interface-access/idiastackwalkhelper-get-registervalue.md)|擷取暫存器的值。|
|[IDiaStackWalkHelper::put_registerValue](../../debugger/debug-interface-access/idiastackwalkhelper-put-registervalue.md)|設定暫存器值。|
|[IDiaStackWalkHelper::readMemory](../../debugger/debug-interface-access/idiastackwalkhelper-readmemory.md)|從記憶體中的可執行檔的映像中讀取資料的區塊。|
|[IDiaStackWalkHelper::searchForReturnAddress](../../debugger/debug-interface-access/idiastackwalkhelper-searchforreturnaddress.md)|搜尋指定的堆疊框架之最接近的函式傳回的位址。|
|[IDiaStackWalkHelper::searchForReturnAddressStart](../../debugger/debug-interface-access/idiastackwalkhelper-searchforreturnaddressstart.md)|搜尋指定的堆疊框架的地址，位於或接近指定的堆疊位址。|
|[IDiaStackWalkHelper::frameForVA](../../debugger/debug-interface-access/idiastackwalkhelper-frameforva.md)|擷取堆疊框架，其中包含指定的虛擬位址。|
|[IDiaStackWalkHelper::symbolForVA](../../debugger/debug-interface-access/idiastackwalkhelper-symbolforva.md)|擷取包含指定的虛擬位址的符號。 **注意：** 符號必須有型別`SymTagFunctionType`(取值[SymTagEnum 列舉](../../debugger/debug-interface-access/symtagenum.md)列舉型別)。|
|[IDiaStackWalkHelper::pdataForVA](../../debugger/debug-interface-access/idiastackwalkhelper-pdataforva.md)|傳回與指定的虛擬位址相關聯的 PDATA 資料區塊。|
|[IDiaStackWalkHelper::imageForVA](../../debugger/debug-interface-access/idiastackwalkhelper-imageforva.md)|擷取可執行檔，開始的虛擬位址的虛擬位址某處可執行檔的記憶體空間中。|

## <a name="remarks"></a>備註
 這個介面會呼叫 DIA 程式碼，以取得要在程式執行期間建構的堆疊框架清單可執行檔的相關資訊。

## <a name="notes-for-callers"></a>呼叫端資訊
 用戶端應用程式會實作這個介面，以支援在程式執行期間查核堆疊。 此介面的執行個體傳遞給[IDiaStackWalker::getEnumFrames](../../debugger/debug-interface-access/idiastackwalker-getenumframes.md)或是[IDiaStackWalker::getEnumFrames2](../../debugger/debug-interface-access/idiastackwalker-getenumframes2.md)方法。

## <a name="requirements"></a>需求
 標頭： Dia2.h

 程式庫： diaguids.lib

 DLL: msdia80.dll

## <a name="see-also"></a>請參閱
- [介面 (偵錯介面存取 SDK)](../../debugger/debug-interface-access/interfaces-debug-interface-access-sdk.md)
- [IDiaFrameData](../../debugger/debug-interface-access/idiaframedata.md)
- [SymTagEnum 列舉](../../debugger/debug-interface-access/symtagenum.md)
- [IDiaStackWalker::getEnumFrames](../../debugger/debug-interface-access/idiastackwalker-getenumframes.md)
- [IDiaStackWalker::getEnumFrames2](../../debugger/debug-interface-access/idiastackwalker-getenumframes2.md)