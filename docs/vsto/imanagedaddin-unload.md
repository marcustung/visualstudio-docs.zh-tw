---
title: IManagedAddin::Unload
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Unload method
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 296502aa461688c34152d86ee21aab5f2c83ecb4
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56640489"
---
# <a name="imanagedaddinunload"></a>IManagedAddin::Unload
  卸載 Managed VSTO 增益集之前呼叫。

## <a name="syntax"></a>語法

```csharp
HRESULT Unload();
```

## <a name="return-value"></a>傳回值
 HRESULT 值，表示此方法是否已順利完成。

## <a name="remarks"></a>備註
 Microsoft Office 的目前版本不會呼叫這個方法。 這個方法是保留供日後使用。

## <a name="see-also"></a>另請參閱
- [IManagedAddin 介面](../vsto/imanagedaddin-interface.md)
- [IManagedAddin::Load](../vsto/imanagedaddin-load.md)
