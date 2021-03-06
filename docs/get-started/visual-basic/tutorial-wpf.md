---
title: 教學課程：使用 Windows Presentation Foundation (WPF) 的 Hello World 應用程式 (Visual Basic)
description: 使用 Windows Presentation Foundation (WPF) UI 架構，透過 Visual Studio 以 Visual Basic 建立一個簡單的 Windows Desktop .NET 應用程式。
ms.custom: seodec18, get-started
ms.date: 03/14/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
ms.topic: conceptual
dev_langs:
- VB
ms.assetid: f84339c7-d617-4f56-bfcd-af2215c347ba
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: b64972f2bf2ef0bb34722f717f7ddf8bf032349d
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2019
ms.locfileid: "58857395"
---
# <a name="tutorial-create-a-simple-application-with-visual-basic"></a>教學課程：使用 Visual Basic 建立簡單的應用程式

藉由完成這個教學課程，讓自己更熟悉許多可在使用 Visual Studio 開發應用程式時運用的工具、對話方塊和設計工具。 當您在學習如何使用整合式開發環境 ([IDE](visual-studio-ide.md)) 時，您會建立簡單的 "Hello, World" 應用程式、設計 UI、新增程式碼，以及進行偵錯。

::: moniker range="vs-2017"

如果您尚未安裝 Visual Studio，請前往 [Visual Studio 下載](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017)頁面免費進行安裝。

::: moniker-end

::: moniker range=">=vs-2019"

如果您尚未安裝 Visual Studio，請前往 [Visual Studio 下載](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)頁面免費進行安裝。

::: moniker-end

## <a name="configure-the-ide"></a>設定 IDE

::: moniker range="vs-2017"

當您第一次開啟 Visual Studio 時，系統會提示您登入。 這在此教學課程中為選擇性步驟。 接下來您可能會看到對話方塊，要求您選擇開發設定和色彩佈景主題。 保留預設值，然後選擇 [啟動 Visual Studio]。

![選擇設定對話方塊](../media/exploreide-settings.png)

Visual Studio 啟動後，您會看到工具視窗、功能表和工具列，以及主視窗空間。 工具視窗會停駐在應用程式視窗的左右端，同時 [ **快速啟動**]、功能表列和標準工具列則位於視窗的上方。 位於應用程式視窗中央的是 [ **起始頁**]。 當您載入方案或專案時，編輯器和設計工具會出現在 [起始頁]  所在的空間中。 在開發應用程式時，您大部分時間都會在此中央區域工作。

![已套用一般設定的 Visual Studio 2017 IDE](../media/exploreide-idewithgeneralsettings.png)

::: moniker-end

::: moniker range=">=vs-2019"

當您啟動 Visual Studio 時，會先開啟 [開始] 視窗。 選取 [不使用程式碼繼續] 以開啟開發環境。 您會看到工具視窗、功能表和工具列，以及主視窗空間。 [工具] 視窗會停駐在應用程式視窗的左側和右側，搜尋方塊、功能表列和標準工具列則位於視窗上方。 當您載入方案或專案時，編輯器和設計工具會出現在應用程式視窗的中央區域。 在開發應用程式時，您大部分時間都會在此中央區域工作。

::: moniker-end

## <a name="create-the-project"></a>建立專案

當您在 Visual Studio 中建立應用程式時，您需要先建立一個專案和一個方案。 在這個範例中，您將建立 Windows Presentation Foundation (WPF) 專案。

::: moniker range="vs-2017"

1. 建立新的專案。 在功能表列上，選取 [檔案] > [新增] > [專案]。

     ![在功能表上依序選擇 [檔案]、[開新檔案] 和 [專案]](../media/exploreide-filenewproject.png)

2. 在 [新增專案] 對話方塊中，選取 [已安裝] > [Visual Basic] > [Windows 桌面] 類別，然後選取 [WPF 應用程式 (.NET Framework)] 範本。 將專案命名為 **HelloWPFApp**，然後選取 [確定]。

     ![Visual Studio [新增專案] 對話方塊中的 WPF 應用程式範本](media/exploreide-newproject-vb.png)

Visual Studio 會建立 HelloWPFApp 專案和方案，而且**方案總管**會顯示各種不同檔案。 **WPF 設計工具**會在分割檢視中顯示 *MainWindow.xaml* 的設計檢視和 XAML 檢視。 您可以滑動分隔器來增加或減少顯示任一檢視。 您可以選擇只查看視覺檢視，或只查看 XAML 檢視。 下列項目會在 **方案總管**中出現：

![已載入 HelloWPFApp 檔案的 [方案總管]](../media/exploreide-hellowpfappfiles.png)

::: moniker-end

::: moniker range="vs-2019"

1. 開啟 Visual Studio 2019。

2. 在 [建立新專案] 畫面上，搜尋 "WPF"、選擇 [WPF 應用程式 (.NET Framework)]，然後選擇 [下一步]。

   ![Visual Studio [新增專案] 對話方塊中的 WPF 應用程式範本](media/vs-2019/exploreide-newprojectvb-vs2019.png)

3. 在下一個畫面上，為專案指定名稱 **HelloWPFApp**，然後選擇 [建立]。

Visual Studio 會建立 HelloWPFApp 專案和方案，而且**方案總管**會顯示各種不同檔案。 **WPF 設計工具**會在分割檢視中顯示 *MainWindow.xaml* 的設計檢視和 XAML 檢視。 您可以滑動分隔器來增加或減少顯示任一檢視。 您可以選擇只查看視覺檢視，或只查看 XAML 檢視。 下列項目會在 **方案總管**中出現：

![已載入 HelloWPFApp 檔案的 [方案總管]](../media/vs-2019/exploreide-hellowpfappfiles.png)

::: moniker-end

> [!NOTE]
> 如需 XAML (eXtensible Application Markup Language) 的詳細資訊，請參閱 [WPF 的 XAML 概觀](/dotnet/framework/wpf/advanced/xaml-overview-wpf)頁面。

建立專案之後，您可以進行自訂。 使用 [屬性]  視窗 (在 [檢視]  功能表上)，就可以顯示和變更應用程式中的專案項目、控制項及其他項目的選項。

### <a name="change-the-name-of-mainwindowxaml"></a>變更 MainWindow.xaml 的名稱

讓我們給 MainWindow 一個更具體的名稱。

1. 在 [方案總管] 中，選取 *MainWindow.xaml*。 您應該會看到 [屬性] 視窗；如果沒有，請選擇 [檢視] 功能表和 [屬性視窗] 項目。

1. 將 [ **檔案名稱** ] 屬性變更為 `Greetings.xaml`。

     ![包含反白顯示之檔名的 [屬性] 視窗](../media/exploreide-filenameinpropertieswindow.png)

     [方案總管] 現在顯示的檔案名稱是 *Greetings.xaml*，而巢狀程式碼檔案的名稱現在是 *Greetings.xaml.vb*。 這個程式碼檔案套疊在 *.xaml* 檔案節點下，顯示它們彼此密切相關。

## <a name="design-the-user-interface-ui"></a>設計使用者介面 (UI)

我們會將三種類型的控制項新增至這個應用程式：一個 <xref:System.Windows.Controls.TextBlock> 控制項、兩個 <xref:System.Windows.Controls.RadioButton> 控制項和一個 <xref:System.Windows.Controls.Button> 控制項。

### <a name="add-a-textblock-control"></a>新增 TextBlock 控制項

1.  輸入 **Ctrl**+**Q** 啟動搜尋方塊，然後鍵入**工具箱**。 從結果清單中選擇 [檢視] > [工具箱]。

2. 在 [工具箱] 中展開 [通用 WPF 控制項] 節點以查看 TextBlock 控制項。

     ![已反白顯示 [TextBlock] 控制項的 [工具箱]](../media/exploreide-textblocktoolbox.png)

3. 選擇 TextBlock 項目並將它拖曳至設計介面上的視窗，即可將 **TextBlock** 控制項加入設計介面。 將控制項置中靠近視窗頂端。

您的視窗應該會和下圖類似：

![問候表單上的 [TextBlock] 控制項](../media/exploreide-greetingswithtextblockonly.png)

XAML 標記應該看起來與下列範例相似：

```xaml
<TextBlock HorizontalAlignment="Center" TextWrapping="Wrap" VerticalAlignment="Center" RenderTransformOrigin="4.08,2.312" Margin="237,57,221,238"><Run Text="TextBlock"/><InlineUIContainer><TextBlock TextWrapping="Wrap" Text="TextBlock"/>
```

### <a name="customize-the-text-in-the-text-block"></a>自訂文字區塊中的文字

1. 在 XAML 檢視中，找出 TextBlock 的標記並變更 Text 屬性：

   ```xaml
   Text="Select a message option and then choose the Display button."
   ```

2. 視需要再次將 TextBlock 置中，然後按 Ctrl+S 或使用 [檔案] 功能表項目來儲存您的變更。

接下來，您會將兩個 [RadioButton](/dotnet/framework/wpf/controls/radiobutton) 控制項新增至表單。

### <a name="add-radio-buttons"></a>新增選項按鈕

1. 在 [工具箱] 中，尋找 **RadioButton** 控制項。

     ![已選取 [RadioButton] 控制項的 [工具箱] 視窗](../media/exploreide-radiobuttontoolbox.png)

2. 選擇 **RadioButton** 項目並將它拖曳至設計介面的視窗，即可將兩個 RadioButton 控制項新增至設計介面。 移動按鈕 (選取它們並使用方向鍵)，讓按鈕並排顯示於 TextBlock 控制項下。

     您的視窗應該會像這樣：

     ![具有 TextBlock 控制項和兩個選項按鈕的問候表單](../media/exploreide-greetingswithradiobuttons.png)

3. 在左側 RadioButton 控制項的 [ **屬性** ] 視窗中，將 [ **名稱** ] 屬性 (在 [ **屬性** ] 視窗頂端的屬性) 變更為 `HelloButton`。

     ![RadioButton 的 [屬性] 視窗](../media/exploreide-buttonproperties.png)

4. 在右邊 RadioButton 控制項的 [屬性] 視窗中，將 [名稱] 屬性變更為 `GoodbyeButton`，然後儲存您的變更。

您現在可以為每個 RadioButton 控制項加入顯示的文字。 下列步驟會更新 RadioButton 控制項的 [ **內容** ] 屬性。

### <a name="add-display-text-for-each-radio-button"></a>為每個選項按鈕新增顯示的文字

1. 在設計介面上，以滑鼠右鍵按一下 HelloButton 開啟 HelloButton 捷徑功能表，選擇 [編輯文字]，然後輸入 `Hello`。

2. 以滑鼠右鍵按一下 GoodbyeButton 開啟 GoodbyeButton 捷徑功能表，選擇 [編輯文字]，然後輸入 `Goodbye`。

### <a name="set-a-radio-button-to-be-checked-by-default"></a>設定預設勾選的選項按鈕

在此步驟中，我們會設定預設勾選 HelloButton，這樣就一律會選取兩個選項按鈕的其中一個。

在 XAML 檢視中，找出 HelloButton 的標記並新增 **IsChecked** 屬性：

```xaml
IsChecked="True"
```

最後一個要新增的 UI 項目是 [Button](/dotnet/framework/wpf/controls/button) 控制項。

### <a name="add-the-button-control"></a>新增按鈕控制項

1. 在 [工具箱] 中尋找 **Button** 控制項，然後將它拖曳至設計檢視中的表單，將它新增至設計介面的 RadioButton 控制項底下。

2. 在 XAML 檢視中，將 Button 控制項的 [內容] 值從 `Content="Button"` 變更為 `Content="Display"`，然後儲存變更。

     這個標記應類似於下列範例：`<Button Content="Display" HorizontalAlignment="Left" VerticalAlignment="Top" Width="75" Margin="215,204,0,0"/>`

     您的視窗應該會和下圖類似。

     ![具有控制項標籤的問候表單](../media/exploreide-greetingswithcontrollabels.png)

### <a name="add-code-to-the-display-button"></a>將程式碼新增至顯示按鈕

此應用程式執行時，會在使用者選擇選項按鈕並選擇 [顯示] 按鈕之後顯示訊息方塊。 一個訊息方塊會顯示 Hello，而另外一個會顯示 Goodbye。 若要建立這個行為，您必須將程式碼新增至 *Greetings.xaml.vb* 或 *Greetings.xaml.cs* 中的 `Button_Click` 事件。

1. 在設計介面上，按兩下 [ **顯示** ] 按鈕。

     *Greetings.xaml.vb* 隨即開啟，並將游標置於 `Button_Click` 事件中。

    ```vb
    Private Sub Button_Click_1(sender As Object, e As RoutedEventArgs)

    End Sub
    ```

2. 輸入下列程式碼：

    ```vb
    If HelloButton.IsChecked = True Then
        MessageBox.Show("Hello.")
    ElseIf GoodbyeButton.IsChecked = True Then
        MessageBox.Show("Goodbye.")
    End If
    ```

3. 儲存應用程式。

## <a name="debug-and-test-the-application"></a>偵錯和測試應用程式

接下來，您會偵錯應用程式以尋找錯誤，並測試兩個訊息方塊是否都正確出現。 下列指示會告訴您如何建置和啟動偵錯工具，不過您稍後也可閱讀 [建置 WPF 應用程式 (WPF)](/dotnet/framework/wpf/app-development/building-a-wpf-application-wpf) 和[對 WPF 進行偵錯](../../debugger/debugging-wpf.md)以取得詳細資訊。

### <a name="find-and-fix-errors"></a>尋找和修正錯誤

在這個步驟中，您會發現我們先前變更 *MainWindow.xaml* 檔案名稱所產生的錯誤。

#### <a name="start-debugging-and-find-the-error"></a>開始偵錯並找出錯誤

1. 按 **F5** 或依序選取 [偵錯] 和 [開始偵錯]，來啟動偵錯工具。

   [中斷模式] 視窗隨即出現，而 [輸出] 視窗會指出發生了 IOException：找不到資源 'mainwindow.xaml'。

   ![IOException 訊息的螢幕擷取畫面](../media/exploreide-ioexception.png)

2. 選擇 [偵錯] > [停止偵錯] 停止偵錯工具。

我們已在這個教學課程開始時，將 *MainWindow.xaml* 重新命名為 *Greetings.xaml*，但程式碼仍會參考 *MainWindow.xaml* 作為應用程式的啟動 URI，因此專案無法啟動。

#### <a name="specify-greetingsxaml-as-the-startup-uri"></a>指定 Greetings.xaml 作為啟動 URI

1. 在 [方案總管]中，開啟 *Application.xaml* 檔。

2. 將 `StartupUri="MainWindow.xaml"` 變更為 `StartupUri="Greetings.xaml"`，然後儲存變更。

再次啟動偵錯工具 (按 **F5**)。 您應該會看到應用程式的 **Greetings** 視窗。 立即關閉應用程式視窗停止偵錯。

### <a name="debug-with-breakpoints"></a>使用中斷點進行偵錯

新增一些中斷點，即可在偵錯時測試程式碼。 您可以選擇 [偵錯] > [切換中斷點]，或是在您要中斷的程式碼行旁邊，按一下編輯器的左邊界，或按 **F9** 來新增中斷點。

#### <a name="add-breakpoints"></a>新增中斷點

1. 開啟 *Greetings.xaml.vb*，然後選取下列程式碼： `MessageBox.Show("Hello.")`

2. 按 **F9**，或從功能表中依序選取 [偵錯] 和 [切換中斷點]，來新增中斷點。

   在編輯器視窗最左緣、程式碼行的旁邊會出現一個紅色圓圈。

3. 請選取下列程式碼行： `MessageBox.Show("Goodbye.")`。

4. 按 **F9** 鍵新增中斷點，然後按 **F5** 開始偵錯。

5. 在 [ **Greetings** ] 視窗中，選擇 [ **Hello** ] 選項按鈕，然後選擇 [ **顯示** ] 按鈕。

   程式碼行 `MessageBox.Show("Hello.")` 會以黃色反白顯示。 在 IDE 底部，[自動變數]、[區域變數] 和 [監看式] 視窗會一起停駐在左邊，而 [呼叫堆疊]、[中斷點]、[例外狀況設定]、[命令]、[即時運算] 和 [輸出] 視窗會一起停駐在右邊。

   ![偵錯工具中的中斷點螢幕擷取畫面](media/exploreide-debugbreakpoint.png)

6. 在功能表列上，選擇 [偵錯] > [跳離函式]。

     應用程式會繼續執行，而且會顯示含有文字 "Hello" 的訊息方塊。

7. 選擇訊息方塊上的 [ **確定** ] 按鈕將它關閉。

8. 在 [ **Greetings** ] 視窗中，選擇 [ **Goodbye** ] 選項按鈕，然後選擇 [ **顯示** ] 按鈕。

     程式碼行 `MessageBox.Show("Goodbye.")` 會以黃色反白顯示。

9. 選擇 **F5** 鍵繼續偵錯。 當訊息方塊出現時，選擇訊息方塊中的 [ **確定** ] 按鈕關閉它。

10. 關閉應用程式視窗停止偵錯。

11. 在功能表列上，選擇 [偵錯] > [停用所有中斷點]。

### <a name="build-a-release-version-of-the-application"></a>建置應用程式的發行版本

既然已經驗證應用程式的運作一切正常，您就可以準備其發行組建。

1. 在主功能表上，選取 [組建] > [清除方案]，刪除在上一個組建期間建立的中繼檔和輸出檔。 這並非必要動作，但它可清除偵錯建置輸出。

2. 使用工具列上的下拉式控制項 (它目前的名稱是 "Debug")，將 HelloWPFApp 的建置組態從 [偵錯] 變更為 [發行]。

3. 選擇 [建置] > [建置方案] 來建置方案。

恭喜您完成此教學課程！ 您可在方案和專案目錄 (*...\HelloWPFApp\HelloWPFApp\bin\Release*) 下找到您建置的 *.exe*。

## <a name="see-also"></a>另請參閱

- [Visual Studio 2017 的新功能](../../ide/whats-new-visual-studio.md)
- [生產力祕訣](../../ide/productivity-tips-for-visual-studio.md)