---
title: 預覽程式碼變更
ms.date: 12/16/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- vs.codefix.previewchanges
ms.workload:
- multiple
ms.openlocfilehash: 07d722848725753b0b2abf25c8497327cdb53835
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55952160"
---
# <a name="preview-changes-window"></a>[預覽變更] 視窗

在 Visual Studio 中使用各種「快速動作」或「重構」工具時，經常可能需要先預覽要對專案進行的變更，再接受它們。 [預覽變更] 視窗是完成這項作業的位置。  例如，以下 [預覽變更] 視窗會顯示 C# 專案中將在重新命名重構期間變更的內容：

![預覽變更](media/previewchanges.png)

視窗上半部會顯示將變更的特定行，且各有一個核取方塊。 如果您想要選擇性地只將重構套用至特定行，則可以核取或取消核取每個核取方塊。

視窗下半部會顯示專案中將變更的格式化程式碼，並且反白顯示受影響的區域。 選取視窗上半部中的特定行，將會在下半部中反白顯示對應的行。 這可讓您快速跳至適當的行，以及查看周圍的程式碼。

檢閱變更之後，請按一下 [套用] 按鈕認可這些變更，或按一下 [取消] 按鈕不進行變更。

## <a name="see-also"></a>另請參閱

- [在 Visual Studio 中重構](../ide/refactoring-in-visual-studio.md)
- [快速動作](../ide/quick-actions.md)
