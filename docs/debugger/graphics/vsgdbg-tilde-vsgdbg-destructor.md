---
title: 'VsgDbg:: ~ VsgDbg （解構函式） |Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 7a3b97fb-d344-4df7-b195-9347d1edfcf7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 64d2ce58a0a543a6bccfca4d96ff57915d45ce49
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56686557"
---
# <a name="vsgdbgvsgdbg-destructor"></a>VsgDbg::~VsgDbg (解構函式)
終結的執行個體`VsgDbg`類別。 如果目前正在錄製的圖形資訊，圖形記錄檔已完成並關閉，並主動擷取圖形資訊時所使用的資源，會釋放。

## <a name="syntax"></a>語法

```C++
~VsgDbg();
```

## <a name="see-also"></a>請參閱
- [VsgDbg::VsgDbg (建構函式)](vsgdbg-vsgdbg-constructor.md)