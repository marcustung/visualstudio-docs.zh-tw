---
title: C# 專案屬性應用程式頁面
ms.date: 10/30/2018
ms.topic: reference
f1_keywords:
- cs.ProjectPropertiesApplicationWPF
- cs.ProjectPropertiesApplication
helpviewer_keywords:
- Project Designer, Application page
- Application page in Project Designer
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 18527e9b45726dbd76f1e76f5d63976278800f6f
ms.sourcegitcommit: 3201da3499051768ab59f492699a9049cbc5c3c6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2019
ms.locfileid: "58355337"
---
# <a name="application-page-project-designer-c"></a>專案設計工具，應用程式頁 (C#)

使用 [專案設計工具] 的 [應用程式] 頁面來指定專案的應用程式設定和屬性。

若要存取 [應用程式] 頁面，請在方案總管中選擇專案節點 (而不是 [方案] 節點)。 然後選擇功能表列上的 [專案] > [屬性]。 當 [專案設計工具] 出現時，請按一下 [應用程式] 索引標籤。

[!INCLUDE[note_settings_general](../../data-tools/includes/note_settings_general_md.md)]

## <a name="general-application-settings"></a>一般應用程式設定

下列選項可讓您設定應用程式的一般設定。

**組件名稱**

指定將保留組件資訊清單之輸出檔的名稱。 變更此屬性也會變更 [輸出名稱] 屬性。

您也可以從命令列使用 [/out (C# 編譯器選項)](/dotnet/csharp/language-reference/compiler-options/out-compiler-option) 進行這項變更。

若要以程式設計方式存取此屬性，請參閱 <xref:VSLangProj.ProjectProperties.AssemblyName%2A>。

**預設命名空間**

指定新增至專案之檔案的基底命名空間。

如需在程式碼中建立命名空間的詳細資訊，請參閱 [namespace](/dotnet/csharp/language-reference/keywords/namespace)。

若要以程式設計方式存取此屬性，請參閱 <xref:VSLangProj.ProjectProperties.RootNamespace%2A>。

**目標 Framework**

指定應用程式作為目標的 .NET Framework 版本。 此選項可能會有不同的值，而這些值取決於電腦上安裝的 .NET Framework 版本。

根據預設，值會與您建立專案時選取的目標 Framework 相同。

> [!NOTE]
> 第一次開啟該對話方塊時，會自動設定[必要條件對話方塊](../../ide/reference/prerequisites-dialog-box.md)中所列的必要條件套件。 如果您接著變更專案的目標架構，就必須手動選取必要條件以符合新的目標架構。

如需詳細資訊，請參閱[如何：以 .NET Framework 版本為目標](../../ide/how-to-target-a-version-of-the-dotnet-framework.md)和 [Visual Studio 多目標概觀](../../ide/visual-studio-multi-targeting-overview.md)。

**輸出類型**

指定要建置的應用程式類型。 值會因專案類型而有所不同。 例如，針對**主控台應用程式**專案，您可以指定 **Windows 應用程式**、**主控台應用程式**或**類別庫**作為輸出類型。

針對 Web 應用程式專案，您必須指定 [類別庫]。

如需**輸出類型**屬性的詳細資訊，請參閱 [/target (C# 編譯器選項)](/dotnet/csharp/language-reference/compiler-options/target-compiler-option)。

如需如何以程式設計方式存取此屬性的資訊，請參閱 <xref:VSLangProj.ProjectProperties.OutputType%2A>。

**自動產生繫結重新導向**

若應用程式或其元件參考相同組件的多個版本，則繫結重新導向會新增至您的專案。 如果您希望手動定義專案檔中的繫結重新導向，請取消選取 [自動產生繫結重新導向]。

如需重新導向的詳細資訊，請參閱[重新導向組件版本](/dotnet/framework/configure-apps/redirect-assembly-versions)。

**啟始物件**

定義要在應用程式載入時呼叫的進入點。 通常，這會設定成您應用程式中的主要表單，或應該在應用程式啟動時執行的 `Main` 處理序。 因為類別庫沒有進入點，所以這個屬性的唯一選項是 [(未設定)]。

根據預設，此選項在 WPF 應用程式專案中為 [(未設定)]。 另一個選項是 \[projectname].App。 在 WPF 專案中，您必須設定應用程式啟動時載入 UI 資源的啟動 URI。 若要執行此作業，請開啟專案中的 *Application.xaml* 檔案，並將 `StartupUri` 屬性設為專案中的 *.xaml* 檔案 (例如 *Window1.xaml*)。 如需可接受根項目的清單，請參閱 <xref:System.Windows.Application.StartupUri%2A>。 您必須也在專案的類別中定義 `public static void Main()` 方法。 此類別將會以 <專案名稱.類別名稱> 形式出現在 [啟始物件] 清單中。 您接著可以選取類別作為啟始物件。

如需詳細資訊，請參閱 [/main (C# 編譯器選項)](/dotnet/csharp/language-reference/compiler-options/main-compiler-option)。 若要以程式設計方式存取此屬性，請參閱 <xref:VSLangProj.ProjectProperties.StartupObject%2A>。

**組件資訊**

按一下此按鈕會顯示 [組件資訊](../../ide/reference/assembly-information-dialog-box.md) 對話方塊。

## <a name="resources"></a>資源

[資源] 選項可協助您設定應用程式的資源設定。

**圖示和資訊清單**

預設會選取此選項按鈕，並啟用 [圖示] 和 [資訊清單] 選項。 這可讓您選取自己的圖示，或選取不同的資訊清單產生選項。 除非您要提供專案的資源檔，否則請保留選取此選項按鈕。

**圖示**

設定想要用來當作程式圖示的 *.ico* 檔案。 按一下 [瀏覽] 以瀏覽現有圖形，或鍵入您所要檔案的名稱。 如需詳細資訊，請參閱 [/win32icon (C# 編譯器選項)](/dotnet/csharp/language-reference/compiler-options/win32icon-compiler-option)。

若要以程式設計方式存取此屬性，請參閱 <xref:VSLangProj.ProjectProperties.ApplicationIcon%2A>。

**Manifest**

透過使用者帳戶控制 (UAC) 在 Windows Vista 上執行應用程式時，請選取資訊清單產生選項。 此選項可以包含下列值：

- **用預設設定嵌入資訊清單**。 支援 Visual Studio 在 Windows Vista 上操作的一般方式，亦即將 `requestedExecutionLevel` 指定為 `AsInvoker`，以在應用程式可執行檔中嵌入安全性資訊。 這是預設選項。

- **建立無資訊清單應用程式**。 此方法稱為「虛擬化」。 使用此選項，以與舊版應用程式相容。

- **Properties\app.manifest**。 ClickOnce 或免註冊 COM 所部署的應用程式需要此選項。 如果您使用 ClickOnce 部署來發行應用程式，[資訊清單] 會自動設為此選項。

**資源檔**

提供專案的資源檔時，請選取此選項按鈕。 選取此選項會停用 [圖示] 和 [資訊清單] 選項。

輸入路徑名稱，或使用 [瀏覽] 按鈕 (**...**) 將 Win32 資源檔新增至專案。