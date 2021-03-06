---
title: 在參考管理員中新增參考
ms.date: 04/11/2018
ms.topic: conceptual
f1_keywords:
- VS.ReferenceManager
helpviewer_keywords:
- C# projects, references
- references [Visual Studio], adding
- assemblies [Visual Studio], references
- Visual Basic projects, references
- project references, adding
- referencing components, adding references
- project references, removing
- referencing assemblies
- referencing components, removing references
- references [Visual Studio], removing
- referencing components, assemblies not listed
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1b26c700e90189882f850d4bda1d47fb6f54c025
ms.sourcegitcommit: 3d37c2460584f6c61769be70ef29c1a67397cf14
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/21/2019
ms.locfileid: "58322320"
---
# <a name="how-to-add-or-remove-references-by-using-the-reference-manager"></a>作法：使用參考管理員新增或移除參考

針對由您本身、Microsoft 或其他公司所開發的元件，您可以使用 [參考管理員] 對話方塊新增並管理這些元件的參考。 如果您正在開發通用 Windows app，您的專案會自動參考所有正確的 Windows SDK DLL。 如果您正在開發 .NET 應用程式，您的專案會自動參考 *mscorlib.dll*。 某些 .NET API 是在您手動加入的元件中公開。 您必須手動加入對 COM 元件或自訂元件的參考。

## <a name="reference-manager-dialog-box"></a>[參考管理員] 對話方塊

[參考管理員] 對話方塊在左邊顯示不同的分類，隨專案類型而變：

- **組件**，包含 [Framework] 和 [延伸模組] 子群組。

- **COM** 會列出所有可供參考的 COM 元件。

- **解決方案**，包含 [專案] 子群組。

- **Windows**，包含 [核心] 和 [延伸模組] 子群組。 您可以使用 [物件瀏覽器] 探索 Windows SDK 或延伸模組 SDK 中的參考。

- **瀏覽**，包含 [最近] 子群組。

## <a name="add-a-reference"></a>加入參考

1. 在**方案總管**中，以滑鼠右鍵按一下 [參考] 或 [相依性] 節點，然後選擇 [新增參考]。 您也可以使用滑鼠右鍵按一下專案節點，然後選取 [新增] > [參考]。

   [參考管理員] 隨即開啟，並依群組列出可用的參考。

2. 指定要新增的參考，然後選取 [確定]。

## <a name="assemblies-tab"></a>組件索引標籤

[組件] 索引標籤會列出可供參考的所有 .NET Framework 組件。 [組件] 索引標籤不會列出全域組件快取 (GAC) 中的任何組件，因為 GAC 中的組件是執行階段環境的一部分。 如果您部署或複製的應用程式中包含在 GAC 中註冊之元件的參考，則不論 [複製到本機] 設定為何，該組件都不會隨著應用程式一起部署或複製。 如需詳細資訊，請參閱[管理專案中的參考](../ide/managing-references-in-a-project.md)。

手動新增對任何 EnvDTE 命名空間 (<xref:EnvDTE>、<xref:EnvDTE80>、<xref:EnvDTE90>、<xref:EnvDTE90a> 或 <xref:EnvDTE100>) 的參考時，請在 [屬性] 視窗中，將參考的 [內嵌 Interop 類型] 屬性設定成 **False**。 如果將此屬性設成 **True**，可能會導致組建問題，因為某些 EnvDTE 屬性無法內嵌。

所有傳統型專案都包含 **mscorlib** 的隱含參考。 [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] 專案包含 <xref:Microsoft.VisualBasic> 的隱含參考。 所有專案都包含 **System.Core** 的隱含參考，即使已從參考清單中移除也一樣。

如果專案類型不支援組件，這個索引標籤就不會出現在 [參考管理員] 對話方塊中。

[組件] 索引標籤包括兩個子索引標籤：

1. [Framework] 會列出組成目標 Framework 的所有組件。

    Windows 8.x 市集應用程式的專案預設包含專案建立時，目標 [!INCLUDE[net_win8_profile](../ide/includes/net_win8_profile_md.md)] 中所有組件的參考。 在受控專案中，**方案總管** [參考] 資料夾下的唯讀節點表示整個架構的參考。 因此，[Framework] 索引標籤不會列舉架構中的任何組件，並改為顯示下列訊息：「所有 Framework 組件都已經被參考了。 請使用物件瀏覽器瀏覽 Framework 中的參考」。 對於傳統型專案，[Framework] 索引標籤會列舉目標 Framework 中的組件，而且使用者必須新增應用程式所需的參考。

2. [延伸模組] 會列出外部元件和控制項廠商為了擴充目標 Framework 所開發的全部組件。 根據使用者應用程式的用途，可能會需要這些組件。

   填入 [延伸模組] 的方式是列舉下列位置所註冊的組件：

   32 位元電腦：
   - `HKEY_CURRENT_USER\SOFTWARE\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`

   64 位元電腦：
   - `HKEY_CURRENT_USER\SOFTWARE\Wow6432Node\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\[Target Framework Identifier]\v[Target Framework Version]\AssemblyFoldersEx\[UserComponentName]\@default=[Disk location of assemblies]`

   和舊版的 [目標 Framework 識別碼]

   例如，如果專案在 32 位元電腦上的目標是 .NET Framework 4，則 [延伸模組] 會列舉 *\Microsoft\.NETFramework\v4.0\AssemblyFoldersEx*、*\Microsoft\.NETFramework\v3.5\AssemblyFoldersEx*、*\Microsoft\.NETFramework\v3.0\AssemblyFoldersEx* 及 *\Microsoft\.NETFramework\v2.0\AssemblyFoldersEx* 下註冊的組件。

視專案的 .NET Framework 版本而定，清單中的部分元件可能不會顯示。 在下列狀況下可能會發生這種情形：

- 使用最近版本 .NET Framework 的元件，與目標針對舊版 .NET Framework 的專案並不相容。

    如需如何為專案變更目標 .NET Framework 版本的資訊，請參閱[如何：以一個 .NET Framework 版本為目標](../ide/how-to-target-a-version-of-the-dotnet-framework.md)。

- 使用 [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] 的元件與目標針對 [!INCLUDE[net_v45](../ide/includes/net_v45_md.md)] 的專案不相容。

    當您建立新的應用程式時，有些專案預設會以 [!INCLUDE[net_v45](../ide/includes/net_v45_md.md)] 為目標。

您應該避免將檔案參考加入至同一方案中的其他專案輸出，因為這麼做可能會造成編譯錯誤。 請改用 [加入參考] 對話方塊中的 [專案] 索引標籤，來建立專案對專案間的參考。 這樣一來就能夠更有效的管理在專案中所建立的類別庫，使得小組開發更為容易。 如需詳細資訊，請參閱[針對中斷參考進行疑難排解](../ide/troubleshooting-broken-references.md)。

> [!NOTE]
> 在 Visual Studio 2015 (含) 以後版本中，如果某個專案的 .NET Framework 目標版本為第 4.5 版 (含) 以後版本，而其他專案的目標版本為第 2 版、第 3 版、第 3.5 版或第 4.0 版，則會建立檔案參考而非專案參考。

### <a name="to-display-an-assembly-in-the-add-reference-dialog-box"></a>若要在加入參考對話方塊中顯示組件

- 將組件移動或複製至下列其中一個位置：

   - 目前專案目錄。 (您可以使用 [瀏覽]  索引標籤尋找這些組件)。

   - 同一方案中的其他專案目錄。 (您可以使用 [專案] 索引標籤尋找這些組件)。

    \-或-

- 設定用以指定組件顯示位置的登錄機碼：

   針對 32 位元的作業系統，請加入下列登錄機碼之一。

   - `[HKEY_CURRENT_USER\SOFTWARE\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   - `[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   針對 64 位元的作業系統，請在 32 位元登錄區中，加入下列登錄機碼之一。

   - `[HKEY_CURRENT_USER\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   - `[HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\<VersionMinimum>\AssemblyFoldersEx\MyAssemblies]@="<AssemblyLocation>"`

   \<最低版本\> 是適用的最低 .NET Framework 版本。 如果 \<最低版本\> 是 3.0 版，則 *AssemblyFoldersEx* 中指定的資料夾適用於以 .NET Framework 3.0 (含) 以後版本為目標的專案。

   \<組件位置\> 代表您想要在 [新增參考] 對話方塊中顯示的組件目錄，例如 *C:\MyAssemblies*。

   在 `HKEY_LOCAL_MACHINE` 節點下建立登錄機碼，可讓所有使用者都能在 [新增參考] 對話方塊中看到指定位置的組件。 在 `HKEY_CURRENT_USER` 節點下建立登錄機碼，只會影響目前使用者的設定。

   再次開啟 [加入參考] 對話方塊。 組件應該會出現在 [.NET] 索引標籤上。如果沒有顯示，請確認組件位於指定的 <組件位置> 目錄中，然後重新啟動 Visual Studio 並再試一次。

## <a name="projects-tab"></a>[專案] 索引標籤

[專案] 索引標籤會在 [方案] 子索引標籤內列出目前解決方案的所有相容專案。

專案可以參考以不同 .NET Framework 版本為目標的其他專案。 例如，您可以建立以 [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] 為目標，但是參考針對 .NET Framework 2 所建置之組件的專案。 不過，.NET Framework 2 專案無法參考 [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] 專案。 如需詳細資訊，請參閱[多目標概觀](../ide/visual-studio-multi-targeting-overview.md)。

目標為 [!INCLUDE[net_v40_short](../code-quality/includes/net_v40_short_md.md)] 的專案與目標為 [!INCLUDE[net_client_v40_long](../deployment/includes/net_client_v40_long_md.md)] 的專案不相容。

如果專案的目標為 .NET Framework 4，而另一個專案的目標為舊版，則會建立檔案參考而不是專案參考。

目標為 [!INCLUDE[net_win8_profile](../ide/includes/net_win8_profile_md.md)] 的專案無法將專案參考新增至目標為 .NET Framework 的專案，反之亦然。

## <a name="universal-windows-tab"></a>[通用 Windows] 索引標籤

[通用 Windows] 索引標籤會列出 Windows 作業系統執行所在平台特定的所有 SDK。
此索引標籤有兩個子群組：[核心] 和 [延伸模組]。

### <a name="core-subgroup"></a>[核心] 子群組

根據預設，通用 Windows 應用程式專案具有通用 Windows SDK 的參考。 因此，[參考管理員] 中的 [核心] 子群組不會列舉 Windows SDK 中的任何組件。

### <a name="extensions-subgroup"></a>[延伸模組] 子群組

[延伸模組] 會列出擴充目標 Windows 平台的使用者 SDK。

SDK 是檔案集合，Visual Studio 會將這個集合視為單一元件。 在 [延伸模組] 索引標籤中，適用於叫用 [參考管理員] 對話方塊所在專案的 SDK 會以單一項目形式列出。 新增至專案時，Visual Studio 會使用所有 SDK 內容，因此使用者不需要採取任何進一步動作就可以在 IntelliSense、工具箱、設計工具、物件瀏覽器、組建、部署、偵錯和封裝中利用 SDK 內容。

如需如何在 [延伸模組] 索引標籤中顯示 SDK 的資訊，請參閱[建立軟體開發套件](../extensibility/creating-a-software-development-kit.md)。

> [!NOTE]
> 如果專案參考的 SDK 取決於另一個 SDK，則除非您手動新增第二個 SDK 的參考，否則 Visual Studio 不會使用第二個 SDK。 當使用者在 [延伸模組] 索引標籤中選擇 SDK 時，[參考管理員] 對話方塊會在 [詳細資料] 窗格中列出所有相依性，幫助您識別 SDK 相依性。

如果專案類型不支援延伸模組，此索引標籤就不會出現在 [參考管理員] 對話方塊中。

## <a name="com-tab"></a>COM 索引標籤

[COM] 索引標籤會列出所有可供參考的 COM 元件。 如果您要將參考加入包含內部資訊清單的已註冊 COM DLL，請先移除註冊 DLL。 否則 Visual Studio 會將組件參考新增為 ActiveX 控制項，而不是原生 DLL。

如果專案類型不支援 COM，這個索引標籤就不會出現在 [參考管理員] 對話方塊中。

## <a name="browse-button"></a>瀏覽按鈕

您可以使用 [瀏覽] 按鈕，瀏覽檔案系統中的元件。

專案可以參考以不同 .NET Framework 版本為目標的元件。 例如，您可以建立目標為 .NET Framework 4.7，但參考目標為 .NET Framework 4 之元件的應用程式。 如需詳細資訊，請參閱[多目標概觀](../ide/visual-studio-multi-targeting-overview.md)。

您應該避免將檔案參考加入至同一方案中的其他專案輸出，因為這種做法可能會造成編譯錯誤。 請改用 [參考管理員] 對話方塊中的 [方案] 索引標籤來建立專案對專案間的參考。 這樣一來就能夠更有效的管理在專案中所建立的類別庫，使得小組開發更為容易。 如需詳細資訊，請參閱[針對中斷參考進行疑難排解](../ide/troubleshooting-broken-references.md)。

您無法瀏覽至 SDK，並將它新增至您的專案。 您只能瀏覽至檔案 (例如，組件或 *.winmd*)，並將它新增至專案。

對 WinMD 執行檔案參考時，預期的配置是將 \<檔案名稱>.winmd、\<檔案名稱>.dll 和 \<檔案名稱>.pri 檔案全部放置在一起。 如果您在下列情境中參考 WinMD，會將不完整的檔案集合複製到專案輸出目錄中，因此造成建置和執行階段失敗發生。

- **原生元件**：原生專案會為每一個不相鄰的命名空間集合建立一個 WinMD，並且建立一個包含實作的 DLL。 WinMD 會有不同的名稱。 參考這個原生元件檔時，MSBuild 不會將採用不同名稱的 WinMD 辨識為同一個元件。 因此，只會複製同名的 \<檔案名稱>.dll 和 \<檔案名稱>.winmd，並會發生執行階段錯誤。 若要解決這個問題，請建立延伸模組 SDK。 如需詳細資訊，請參閱[建立軟體開發套件](../extensibility/creating-a-software-development-kit.md)。

- **使用控制項**：XAML 控制項至少包含 \<檔案名稱>.winmd、\<檔案名稱>.dll、\<檔案名稱>.pri\<XamlName>.xaml、 和 \<ImageName>.jpg。 專案建置後，系統不會將已與檔案參考建立關聯的資源檔複製到專案輸出目錄中，只會複製 \<檔案名稱>.winmd、\<檔案名稱>.dll 和 \<檔案名稱>.pri。 此時會記錄建置錯誤，通知使用者遺漏 \<XAML 名稱>.xaml 和 \<影像名稱>.jpg 資源。 若要成功，使用者必須手動將這些資源檔複製到專案輸出目錄中供建置和偵錯/執行階段使用。 若要解決這個問題，請遵循[建立軟體開發套件](../extensibility/creating-a-software-development-kit.md)中的步驟建立延伸模組 SDK，或編輯專案檔以新增下列屬性：

    ```xml
    <PropertyGroup>
       <GenerateLibraryOutput>True</GenerateLibraryOutput>
    </PropertyGroup>
    ```

    > [!NOTE]
    > 如果您加入屬性，建置執行速度可能會變慢。

## <a name="recent"></a>最近

[組件]、[COM]、[Windows] 和 [瀏覽] 各支援一個 [最近] 索引標籤，其中會列舉最近新增至專案中的元件清單。

## <a name="search"></a>搜尋

[參考管理員] 對話方塊中的搜尋列會在成為焦點的索引標籤上運作。 例如，如果使用者在 [方案] 索引標籤成為焦點時於搜尋列中鍵入 "System"，則除非方案擁有包含 "System" 的專案名稱，否則搜尋不會傳回任何結果。

## <a name="see-also"></a>另請參閱

- [管理專案中的參考](../ide/managing-references-in-a-project.md)