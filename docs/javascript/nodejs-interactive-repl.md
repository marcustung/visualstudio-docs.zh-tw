---
title: 使用 Node.js REPL
description: Visual Studio 提供與 Node.js 執行階段互動的支援
ms.date: 12/04/2018
ms.topic: conceptual
ms.devlang: javascript
author: mikejo5000
ms.author: mikejo
manager: jillfra
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: faed930c60869010f740cf0a1e118a40299ce782
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/25/2019
ms.locfileid: "54940670"
---
# <a name="work-with-the-nodejs-interactive-window"></a>使用 Node.js 互動式視窗

適用於 Visual Studio 的 Node.js 工具包含用於已安裝 Node.js 執行階段的互動式視窗。 此視窗可讓您輸入 JavaScript 程式碼並立即查看結果並執行 npm 命令，以與目前的專案互動。 互動式視窗也稱為 REPL (**R**ead/**E**valuate/**P**rint **L**oop)。

## <a name="open-the-interactive-window"></a>開啟互動式視窗

若要開啟互動式視窗，請以滑鼠右鍵按一下 [方案總管] 中的 Node.js 專案節點，然後選取 [開啟 Node.js 互動式視窗]。

![專案操作功能表中的 Node.js 互動式視窗](../javascript/media/interactivewindow-open-from-project.png)

開啟 Node.js 互動式視窗的預設快速鍵是 **[CTRL] + K、N**。或者，您也可以從工具列選擇 [檢視] > [Windows] > [Node.js 互動式視窗] 來開啟視窗。

## <a name="use-the-repl"></a>使用 REPL

開啟後，即可以輸入命令。

![Node.js 互動式視窗](../javascript/media/interactivewindow.png)

互動式視窗具有數個內建命令，以點前置詞開頭以便與您宣告的任何 JavaScript 函式區別。 支援下列命令：

**.cls、.clear** 清除編輯視窗的內容，但不變更歷程記錄和執行內容。

**.help** 顯示指定命令的說明，如未指定，則顯示所有可用的命令和索引鍵繫結。

**.info** 顯示目前使用的 Node.js 可執行檔相關資訊。

**.npm** 執行 npm 命令。 如果方案包含多個專案，請使用 `.npm [projectname] <npm arguments>` 指定目標專案。

**.reset** 將執行環境重設為初始狀態，但保留歷程記錄。

**.save** 將目前的 REPL 工作階段儲存至檔案。