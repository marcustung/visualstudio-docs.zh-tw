---
title: 更新 Visual Studio 2017
titleSuffix: ''
description: 了解如何將 Visual Studio 逐步更新至最新版本。
ms.date: 03/30/2019
ms.custom: seodec18
ms.topic: conceptual
ms.prod: visual-studio-windows
ms.technology: vs-installation
helpviewer_keywords:
- update [Visual Studio]
- change [Visual Studio]
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a64256f44e9de5bbfd9e65dd6410b9911aaf5075
ms.sourcegitcommit: 36f5ffd6ae3215fe31837f4366158bf0d871f7a9
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2019
ms.locfileid: "59232680"
---
# <a name="update-visual-studio-to-the-most-recent-release"></a>將 Visual Studio 更新至最新版本

::: moniker range="vs-2017"

我們建議您更新到[最新版本](/visualstudio/releasenotes/vs2017-relnotes/)的 Visual Studio 2017，使您可以持續取得最新的功能、修正及功能改進。

如果您希望試用下一個版本，請考慮一併下載 [Visual Studio 2019](//visualstudio/releases/2019/release-notes/) 的候選版。

> [!IMPORTANT]
> 您必須以具有安裝、更新或修改 Visual Studio 之系統管理權限的帳戶登入。 如需詳細資訊，請參閱[使用者權限和 Visual Studio](../ide/user-permissions-and-visual-studio.md)。
>
> [!NOTE]
> 本主題適用於 Windows 上的 Visual Studio。 針對 Visual Studio for Mac，請參閱[更新 Visual Studio for Mac](/visualstudio/mac/update)。

## <a name="update-visual-studio-2017-version-156-or-later"></a>更新 Visual Studio 2017 15.6 版或更新版本

我們已簡化安裝及更新的體驗，讓使用者可以更輕鬆地從 IDE 內直接使用它們。 以下是從 Visual Studio 15.6 版及更新版本進行升級的方法。

### <a name="using-the-notifications-hub"></a>使用 [通知] 中樞

有更新可用時，Visual Studio 會顯示相對應的通知旗標。

1. 儲存您的工作。

1. 選擇通知旗標以開啟 [通知] 中樞，然後選擇您要安裝的更新。

   ![使用 [通知] 中樞更新 Visual Studio 2017](media/vs-install-notifications-hub-15dot6.png "Visual Studio 2017 中的 [通知] 中樞")

      > [!TIP]
      > Visual Studio 2017 的版本更新是累積性的，因此請一律選擇安裝版本號碼為最新的更新。

1. 當 [更新] 對話方塊開啟時，選擇 [立即更新]。

    ![使用 [通知] 中樞的 [更新] 對話方塊來更新 Visual Studio 2017](media/vs-update-now-from-notifications-hub.png "Visual Studio 中 [通知] 中樞的 [更新] 對話方塊")

     若系統開啟 [使用者存取控制] 對話方塊，請選擇 [是]。 接著，系統可能會短暫開啟 [請稍後] 對話方塊，然後 Visual Studio 安裝程式便會開啟以開始更新。

     ![15.6 版中的新 Visual Studio 安裝程式體驗](media/visual-studio-15dot6-installer.png "15.6 版中的新 Visual Studio 安裝程式體驗")

     更新將會繼續。 當它完成後，Visual Studio 會重新啟動。

     > [!NOTE]
     > 當您以系統管理員模式執行 Visual Studio 時，就必須在更新之後手動重新啟動 Visual Studio。

### <a name="using-the-ide"></a>使用 IDE

您可以從 Visual Studio 中的功能表列檢查更新並安裝該更新。

1. 儲存您的工作。

1. 選擇 [說明] > [檢查更新]。

     ![Visual Studio 15.6 版中的新 [說明] 功能表](media/vs-help-menu-check-for-updates.png "Visual Studio 15.6 版中的新 [說明] 功能表")

1. 當 [更新] 對話方塊開啟時，選擇 [立即更新]。

   更新會以如上一節所述的方式執行，然後 Visual Studio 會在完成後重新啟動。

   > [!NOTE]
   > 當您以系統管理員模式執行 Visual Studio 時，就必須在更新之後手動重新啟動 Visual Studio。

### <a name="using-the-visual-studio-installer"></a>使用 Visual Studio 安裝程式

和較舊版本的 Visual Studio 相同，您可以使用 Visual Studio 安裝程式來安裝更新。

1. 儲存您的工作。

1. 開啟安裝程式。 Visual Studio 安裝程式可能會需要更新才能繼續執行。

   > [!NOTE]
   > 若要在執行 Windows 10 的電腦上尋找安裝程式，您可在字母 **V** 底下找到 **Visual Studio 安裝程式**，或是在字母 **M** 底下找到 **Microsoft Visual Studio 安裝程式**。

1. 在安裝程式的 [產品] 頁面上，尋找您已安裝的 Visual Studio 版本。

1. 如果有更新可供使用，您會看到 [更新] 按鈕。 (安裝程式可能需要幾秒鐘的時間來判斷是否有更新可供使用)。

   選擇 [更新] 按鈕，以安裝更新。

     ![使用 Visual Studio 安裝程式更新 Visual Studio 2017](media/update-visual-studio.png "使用 Visual Studio 安裝程式更新 Visual Studio 2017")

## <a name="update-visual-studio-2017-version-155-or-earlier"></a>更新 Visual Studio 2017 15.5 版或較早版本

如果您是使用較早的版本，以下是從 Visual Studio 2017 15.0 版至 15.5 版套用更新的方式。

### <a name="update-by-using-the-notifications-hub"></a>使用通知中樞更新

1. 有更新可用時，Visual Studio 會顯示相對應的通知旗標。

   ![使用通知中樞更新 Visual Studio 2017](media/notification-flag.png "Visual Studio 中的更新通知旗標")

   選擇通知旗標，以開啟 [通知] 中樞。

   ![使用通知中樞更新 Visual Studio 2017](media/notifications-hub.png "Visual Studio 中的通知中樞")

      > [!TIP]
      > Visual Studio 2017 的版本更新是累積性的，因此請一律選擇安裝版本號碼為最新的更新。

1. 選擇 ["Visual Studio Update" is available] (有 "Visual Studio 更新" 可供使用)，以開啟 [延伸模組和更新] 對話方塊。

   ![使用通知中樞更新 Visual Studio 2017](media/notifications-hub-select.png "Visual Studio 中的通知中樞")

1. 在 [延伸模組和更新] 對話方塊中，選擇 [更新] 按鈕。

   ![使用通知中樞更新 Visual Studio 2017](media/notifications-extensions-and-updates.png "Visual Studio 中的 [擴充功能和更新] 對話方塊")

#### <a name="more-about-visual-studio-notifications"></a>進一步了解 Visual Studio 通知

Visual Studio 會通知您何時有 Visual Studio 本身或任何元件的更新可用，也會通知您 Visual Studio 環境中何時發生特定事件。

* 通知旗標為黃色時，表示有可供您安裝的 Visual Studio 產品更新。
* 通知旗標為紅色時，表示您的授權發生問題。
* 通知旗標為黑色時，表示有需要檢閱的選擇性或資訊訊息。

選擇通知旗標以開啟 [通知] 中樞，然後選擇您想要處理的通知。 或者，選擇忽略或關閉通知。

 ![在 [通知] 中樞內檢視選擇性或資訊訊息](media/notification-flag-optional.png "Visual Studio 中的選擇性或資訊訊息通知旗標")

如果您選擇忽略通知，則 Visual Studio 會停止顯示該通知。 如果您想要重設已忽略通知的清單，請選擇 [通知] 中樞中的 [設定] 按鈕。

   ![選擇 [通知] 中樞內的 [設定] 按鈕來檢視通知選項](media/vs-notifications-hub-settings-button.png "選擇 [通知] 中樞內的 [設定] 按鈕來檢視通知選項")

### <a name="update-by-using-the-visual-studio-installer"></a>使用 Visual Studio 安裝程式更新

1. 開啟安裝程式。 您可能需要更新安裝程式才能繼續。 如果是這種情況，系統會提示您執行這項操作。

   > [!NOTE]
   > 若要在執行 Windows 10 的電腦上尋找安裝程式，您可在字母 **V** 底下找到 **Visual Studio 安裝程式**，或是在字母 **M** 底下找到 **Microsoft Visual Studio 安裝程式**。

1. 在安裝程式的 [產品] 頁面上，尋找您已安裝的 Visual Studio 版本。

1. 如果有更新可供使用，您會看到 [更新] 按鈕。 (安裝程式可能需要幾秒鐘的時間來判斷是否有更新可供使用)。

   選擇 [更新] 按鈕，以安裝更新。

     ![使用 Visual Studio 安裝程式更新 Visual Studio 2017](media/update-visual-studio.png "使用 Visual Studio 安裝程式更新 Visual Studio")

::: moniker-end

::: moniker range="vs-2019"

我們建議您更新到[最新版本](/visualstudio/releases/2019/release-notes/)的 Visual Studio 2019，使您可以持續取得最新的功能、修正及功能改進。

> [!IMPORTANT]
> 您必須以具有安裝、更新或修改 Visual Studio 之系統管理權限的帳戶登入。 如需詳細資訊，請參閱[使用者權限和 Visual Studio](../ide/user-permissions-and-visual-studio.md)。
>
> [!NOTE]
> 本主題適用於 Windows 上的 Visual Studio。 針對 Visual Studio for Mac，請參閱[更新 Visual Studio for Mac](/visualstudio/mac/update)。

以下是更新 Visual&nbsp;Studio&nbsp;2019&nbsp;Preview 或 Visual&nbsp;Studio&nbsp;2019&nbsp;RC 的方式。

## <a name="use-the-visual-studio-installer"></a>使用 Visual Studio 安裝程式

1. 開啟安裝程式。

     ![開啟 Visual Studio 安裝程式](media/vs2019-visual-studio-installer.png "開啟 Visual Studio 安裝程式")

   您可能需要更新安裝程式才能繼續。 若是如此，請遵循提示。

1. 請在安裝程式中尋找您安裝的 Visual Studio 版本。

   舉例來說，如果您之前安裝了 Visual&nbsp;Studio Community&nbsp;2019&nbsp;RC 且其有更新，安裝程式中就會出現**有可用的更新**訊息。

     ![請選取您要更新的 Visual Studio 2019 版本](media/vs2019-update-visual-studio-community-rc.png "請選取您要更新的 Visual Studio 2019 版本")

1. 選擇 [更新] 安裝更新。

    ![請選取 [更新] 按鈕來安裝更新](media/vs2019-choose-update-visual-studio-community-rc.png "請選取 [更新] 按鈕來安裝更新")

1. 更新完成後，請選擇 [啟動] 來啟動 Visual Studio。

    ![請選取 [啟動] 按鈕來啟動 Visual Studio](media/vs2019-choose-launch-visual-studio-community-rc.png "請選取 [啟動] 按鈕來啟動 Visual Studio")

## <a name="use-the-ide"></a>使用 IDE

您可以從功能表列或 Visual Studio 2019 中的搜尋方塊檢查更新並安裝該更新。

### <a name="open-visual-studio"></a>開啟 Visual Studio

1. 從 Windows [開始] 功能表選擇 [Visual Studio 2019]。

    ![開啟 Visual Studio 2019 RC](media/vs2019-visual-studio-rc.png "從 Windows 開啟 Visual Studio 2019")

1. 在 [開始使用] 下，選擇任一選項開啟 IDE。

    ![開啟 Visual Studio 安裝程式](media/vs2019-choose-option-from-get-started.png "開啟 Visual Studio 安裝程式")

    Visual Studio 隨即開啟。 在 IDE 中，會顯示 **Visual Studio 2019 更新**訊息。

    ![IDE 中的「Visual Studio 2019 更新」訊息](media/vs2019-update-visual-studio-ide-message.png "IDE 中的「Visual Studio 2019 更新」訊息")

1. 在 **Visual Studio 2019 更新**訊息中，選擇 [檢視詳細資料]。

   ![選擇 Visual Studio 2019 IDE 更新訊息中的 [檢視詳細資料] 按鈕](media/vs2019-update-visual-studio-ide-view-details.png "選擇 Visual Studio 2019 更新訊息中的 [檢視詳細資料] 按鈕")

1. 在 [已下載更新，可以開始安裝] 對話方塊方塊中，選擇 [更新]。

     ![在 [已下載更新，可以開始安裝] 對話方塊中選擇 [更新] 按鈕](media/vs2019-update-visual-studio-community-rc-from-ide.png "在 [已下載更新，可以開始安裝] 對話方塊中選擇 [更新] 按鈕")

   Visual Studio 隨即更新，然後關閉再重新開啟。

### <a name="in-visual-studio"></a>在 Visual Studio 中

1. 從功能表列選擇 [說明]，然後選擇 [查看是否有更新]。

     ![從 [說明] 功能表選擇 [查看是否有更新]](media/vs-2019/vs-ide-check-updates-help-menu.png "從 [說明] 功能表選擇 [查看是否有更新]")

    > [!NOTE]
    > 您也可以使用 IDE 中的搜尋方塊來檢查更新。 按下 **Ctrl**+**Q**，鍵入「查看是否有更新」，然後選擇符合的搜尋結果。

1. 在 [已下載更新，可以開始安裝] 對話方塊方塊中，選擇 [更新]。

     ![在 [已下載更新，可以開始安裝] 對話方塊中選擇 [更新] 按鈕](media/vs2019-update-visual-studio-community-rc-from-ide.png "在 [已下載更新，可以開始安裝] 對話方塊中選擇 [更新] 按鈕")

   Visual Studio 隨即更新，然後關閉再重新開啟。

## <a name="use-the-notifications-hub"></a>使用 [通知] 中樞

1. 在 Visual Studio 中，儲存您的工作。

1. 從 Visual Studio IDE 的右下角選擇通知圖示，以開啟 [通知] 中樞。

   ![Visual Studio IDE 中的通知圖示](media/vs-2019/notification-bar.png "Visual Studio IDE 中的通知圖示")

1. 在 [通知] 中樞中，選擇您要安裝的更新，然後選擇 [檢視詳細資料]。

     ![Visual Studio 2019 中的 [通知] 中樞](media/vs-2019/notification-hub-update.png "Visual Studio 2019 中的 [通知] 中樞")

      > [!TIP]
      > Visual Studio 2019 的版本更新是累積性的，因此請選擇安裝版本號碼為最新的更新。

1. 在 [已下載更新，可以開始安裝] 對話方塊方塊中，選擇 [更新]。

   Visual Studio 隨即更新，然後關閉再重新開啟。

::: moniker-end

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>另請參閱

* [更新 Visual Studio 的網路型安裝](update-a-network-installation-of-visual-studio.md)
* [更新 Visual Studio for Mac](/visualstudio/mac/update)
* [修改 Visual Studio 2017](modify-visual-studio.md)
* [解除安裝 Visual Studio](uninstall-visual-studio.md)
