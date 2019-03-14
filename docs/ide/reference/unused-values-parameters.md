---
title: 未使用的值和參數
ms.date: 02/15/2019
ms.topic: reference
author: kendrahavens
ms.author: kendrahavens
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 1ea80887fff6dcb1afba80feb782b23d1e790579
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2019
ms.locfileid: "57325023"
---
# <a name="unused-expression-values-and-parameters"></a>未使用的運算式值和參數

此重構適用於：

- C#
- Visual Basic

**功能：** 淡化未使用的參數，並為未使用的運算式值產生警告。

**時機：** 您擁有從未使用的參數或運算式值。

**原因：** 有時候很難分辨值或參數是否已不再使用。 藉由淡出這些值或發出警告，您就能清楚了解哪些程式碼可以刪除。

## <a name="unused-expression-values-and-parameters-diagnostic"></a>未使用的運算式值和參數診斷

1. 具有任何未使用的運算式值或參數。
2. 未使用的參數會淡出顯示。未使用的運算式值會收到警告。

  ![未使用的參數](media/unused-parameter.png)
  ![未使用的值](media/unused-value.png)

## <a name="see-also"></a>另請參閱

- [重構](../refactoring-in-visual-studio.md)
- [.NET 開發人員的秘訣](../../ide/visual-studio-2017-for-dotnet-developers.md)