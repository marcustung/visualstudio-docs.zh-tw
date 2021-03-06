---
title: Visual Studio Tools for Unity 使用者入門 | Microsoft Docs
ms.custom: ''
ms.date: 07/03/2018
ms.technology: vs-unity-tools
ms.topic: conceptual
ms.assetid: 66b5b4eb-13b5-4071-98d2-87fafa4598a8
author: conceptdev
ms.author: crdun
manager: crdun
ms.workload:
- unity
ms.openlocfilehash: c22b9c25f95ea26f2cdaf5c2035fb7a373123241
ms.sourcegitcommit: 935e341a02dba1c2aa3b6e89469388aa6e626f7f
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/20/2018
ms.locfileid: "53684778"
---
# <a name="get-started-with-visual-studio-tools-for-unity"></a>Visual Studio Tools for Unity 使用者入門

## <a name="install-visual-studio"></a>安裝 Visual Studio

### <a name="unity-bundled-installation"></a>Unity 配套安裝

從 Unity 2018.1 開始，Visual Studio 是 Unity 的預設 C# 指令碼編輯器，而且包含在 Unity 下載助理，以及 Unity 中樞安裝工具中。

- 從 [store.unity.com](https://store.unity.com/) 下載 Unity。

在安裝期間，請確定已核取要與 Unity 一起安裝之元件清單中的 Visual Studio：

#### <a name="unity-hub"></a>Unity 中樞

![unity 中樞安裝](media/vstu_unity-hub.png)

#### <a name="unity-download-assistant"></a>Unity 下載小幫手

![unity 下載小幫手安裝](media/vstu_download-assistant.png)

#### <a name="check-for-updates-to-visual-studio"></a>檢查 Visual Studio 的更新

Unity 安裝所隨附的 Visual Studio 版本可能不是最新的。 建議您檢查更新，以確保您可以存取最新工具和功能。

- [更新 Visual Studio](../install/update-visual-studio.md)

### <a name="manual-installation"></a>手動安裝

若已安裝 Visual Studio 2017 或想要手動安裝，請執行 Visual Studio 安裝程式。

1. [下載 Visual Studio 安裝程式](../install/install-visual-studio.md)或開啟它 (若已安裝)。

1. 針對您想要的 Visual Studio 版本按一下 (若已安裝) 或 [安裝] (針對新安裝)。

1. 在 [工作負載] 索引標籤上，捲動到 [行動與遊戲] 區段，然後選取 [使用 Unity 進行遊戲開發] 工作負載。

    ![Unity 工作負載](media/vstu_unity-workload.png)

1. 按一下安裝程式視窗右下角的 [修改] (若已安裝) 或 [安裝] (針對新安裝)。

## <a name="configure-unity-for-use-with-visual-studio"></a>設定 Unity 以搭配 Visual Studio 使用

從 Unity 2018.1 開始，Visual Studio 應該是 Unity 中的預設外部指令碼編輯器。 您可以確認這一點，或將外部指令碼編輯器變更為特定版本 Visual Studio：

1. 從 [編輯] 功能表，選取 [喜好設定]。

   ![選取 [喜好設定]](media/vstu_unity-preferences.png)

2. 在 [喜好設定] 對話方塊中，選取 [外部工具] 索引標籤。

3. 從 [External Script Editor] \(外部指令碼編輯器\) 下拉式清單中選擇您想要的 Visual Studio 版本 (若已列出)，否則請選取 [瀏覽]。

   ![選取 [Visual Studio]](media/vstu_unity-external-tools.png)

4. 若已選取 [瀏覽]，請瀏覽到您 Visual Studio 安裝目錄中的 **Common7/IDE** 目錄，然後選取 [devenv.exe]。 接著，按一下 [開啟]。

   ![選取 [開啟]](media/vstu_browse-for-application.png)

5. 在 [External Script Editor] \(外部指令碼編輯器\) 清單中選取 Visual Studio 之後，請確認已選取 [Editor Attaching] \(編輯器附加\) 核取方塊。

6. 關閉 [喜好設定] 對話方塊以完成設定程序。

## <a name="support-for-older-versions"></a>針對舊版的支援

 從 Visual Studio Marketplace 下載並安裝 Visual Studio Tools for Unity。 您必須安裝適用於您 Visual Studio 版本的封裝。

- 針對 Visual Studio 2015 Community、Visual Studio 2015 Professional 或 Visual Studio 2015 Enterprise：

   [下載 Visual Studio 2015 Tools for Unity](https://marketplace.visualstudio.com/items?itemName=SebastienLebreton.VisualStudio2015ToolsforUnity)

> [!NOTE]
> Visual Studio Tools for Unity 需要 Unity 5.2 與更新的版本，以及支援延伸模組的 Visual Studio 版本，例如 Visual Studio Community、Professional、Premium 或 Enterprise。 若要確認 Unity 安裝中已啟用 Visual Studio Tools for Unity，請從 [說明] 功能表中選取 [About Unity] \(關於 Unity\)，並在對話方塊左下角尋找「已啟用 Microsoft Visual Studio Tools for Unity」文字。
> ![ Unity](media/vstu_about-unity.png)

## <a name="next-steps"></a>後續步驟

 如需了解如何在 Visual Studio 中使用及偵錯 Unity 專案，請參閱 [Visual Studio Tools for Unity](../cross-platform/using-visual-studio-tools-for-unity.md)。
