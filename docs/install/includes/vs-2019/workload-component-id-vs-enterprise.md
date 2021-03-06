---
title: Visual Studio Enterprise 2019 工作負載和元件識別碼
titleSuffix: ''
description: 使用工作負載和元件識別碼透過命令列安裝 Visual Studio，或是在 VSIX 資訊清單中指定為相依性
keywords: ''
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.date: 04/02/2019
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.topic: include
ms.openlocfilehash: 5c004b1db829f50b2fed435ad0202308ef3726c8
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2019
ms.locfileid: "58872928"
---
## <a name="visual-studio-core-editor-included-with-visual-studio-enterprise-2019"></a>Visual Studio 核心編輯器 (隨附於 Visual Studio Enterprise 2019)

**識別碼：** Microsoft.VisualStudio.Workload.CoreEditor

**描述：** Visual Studio 核心殼層體驗，包括語法感知程式碼編輯、原始程式碼控制及工作項目管理。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.VisualStudio.Component.CoreEditor | Visual Studio 核心編輯器 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.StartPageExperiment.Cpp | C++ 使用者的 Visual Studio 起始畫面 | 16.0.28315.86 | Optional

## <a name="azure-development"></a>Azure 開發

**識別碼：** Microsoft.VisualStudio.Workload.Azure

**描述：** Azure SDK、工具及專案，可用於開發雲端應用程式、建立資源及建置包含 Docker 支援的容器。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | 必要
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure WebJobs 工具 | 16.0.28714.129 | 必要
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | 必要
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET Core 2.1 開發工具 | 16.0.28516.191 | 必要
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure 製作工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Azure.ClientLibs | Azure Libraries for .NET | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure 計算模擬器 | 16.0.28720.110 | 必要
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure 儲存體模擬器 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.FSharp | F# 語言支援 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.FSharp.WebTemplates | Web 專案的 F# 語言支援 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.ComponentGroup.Azure.Prerequisites | Azure 開發必要條件 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure WebJobs 工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 必要
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake 與串流分析工具 | 16.0.28720.110 | 建議
Microsoft.Net.Component.4.5.1.TargetingPack | .NET Framework 4.5.1 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.6.TargetingPack | .NET Framework 4.6 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.TargetingPack | .NET Framework 4 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET Framework 4 – 4.6 開發工具 | 16.0.28516.191 | 建議
Microsoft.VisualStudio.Component.AspNet45 | 進階的 ASP.NET 功能 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.Azure.Kubernetes.Tools | 適用於 Kubernetes 的 Visual Studio Tools | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.ResourceManager.Tools | Azure Resource Manager 核心工具 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.Azure.ServiceFabric.Tools | Service Fabric 工具 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.Azure.Waverton | Azure 雲端服務核心工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure 雲端服務建置工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Debugger.Snapshot | 快照集偵錯工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Debugger.TimeTravel | 時間移動偵錯工具 | 16.0.28714.129 | 建議
Microsoft.VisualStudio.Component.DiagnosticTools | .NET 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.Azure.CloudServices | Azure 雲端服務工具 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.ComponentGroup.Azure.ResourceManager.Tools | Azure Resource Manager 工具 | 16.0.28528.71 | 建議
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.SDK | .NET Framework 4.6.2 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET Framework 4.6.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.SDK | .NET Framework 4.7.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.TargetingPack | .NET Framework 4.7.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.SDK | .NET Framework 4.7 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET Framework 4.7 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET Framework 4.6.1 開發工具 | 16.0.28621.142 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET Framework 4.6.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET Framework 4.7.1 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET Framework 4.7 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.Core.Component.SDK.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET Core 2.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.NetCore.ComponentGroup.Web.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.Component.Azure.Storage.AzCopy | Azure 儲存體 AzCopy | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | Optional

## <a name="data-storage-and-processing"></a>資料儲存體和流程

**識別碼：** Microsoft.VisualStudio.Workload.Data

**描述：** 使用 SQL Server、Azure Data Lake 或 Hadoop 連線、開發及測試資料解決方案。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | 建議
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | 建議
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake 與串流分析工具 | 16.0.28720.110 | 建議
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.5.1.TargetingPack | .NET Framework 4.5.1 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.6.TargetingPack | .NET Framework 4.6 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.TargetingPack | .NET Framework 4 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 建議
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET Framework 4 – 4.6 開發工具 | 16.0.28516.191 | 建議
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 建議
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure 製作工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.ClientLibs | Azure Libraries for .NET | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure 計算模擬器 | 16.0.28720.110 | 建議
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure 儲存體模擬器 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.Azure.Waverton | Azure 雲端服務核心工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure 雲端服務建置工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | 建議
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | 建議
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 建議
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | 建議
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 建議
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.FSharp.Desktop | F# 桌面語言支援 | 16.0.28315.86 | Optional

## <a name="data-science-and-analytical-applications"></a>資料科學和分析應用程式

**識別碼：** Microsoft.VisualStudio.Workload.DataScience

**描述：** 用於建立資料科學應用程式的語言與工具，包括 Python 與 F#。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Component.PythonTools | Python 語言支援 | 16.0.28625.61 | 建議
Microsoft.Component.PythonTools.Minicondax64 | Python miniconda | 16.0.28625.61 | 建議
Microsoft.Component.PythonTools.Web | Python Web 支援 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.FSharp.Desktop | F# 桌面語言支援 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 建議
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 建議
Microsoft.Component.VC.Runtime.UCRTSDK | Windows 通用 CRT SDK | 16.0.28625.61 | Optional
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Python 原生開發工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.Component.Graphics.Tools | 適用於 DirectX 的圖形偵錯工具與 GPU 分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.140 | MSVC v140 - VS 2015 C++ 建置工具 (v14.00) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ 分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Windows10SDK | Windows 通用 C 執行階段 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | Optional

## <a name="net-desktop-development"></a>.NET 桌面開發

**識別碼：** Microsoft.VisualStudio.Workload.ManagedDesktop

**描述：** 使用 C#、Visual Basic 及 F# 來建置 WPF、Windows Forms 與主控台應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | .NET 桌面開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 必要
Component.Microsoft.VisualStudio.LiveShare | Live Share | 1.0.12 | 建議
Microsoft.ComponentGroup.Blend | Blend for Visual Studio | 16.0.28315.86 | 建議
Microsoft.Net.Component.4.5.1.TargetingPack | .NET Framework 4.5.1 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.6.TargetingPack | .NET Framework 4.6 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.TargetingPack | .NET Framework 4 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET Framework 4 – 4.6 開發工具 | 16.0.28516.191 | 建議
Microsoft.VisualStudio.Component.Debugger.JustInTime | Just-in-Time 偵錯工具 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.DiagnosticTools | .NET 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 工具 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.LiveUnitTesting | Live Unit Testing | 16.0.28315.86 | 建議
Component.Dotfuscator | PreEmptive Protection - Dotfuscator | 16.0.28528.71 | Optional
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | Optional
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.SDK | .NET Framework 4.6.2 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET Framework 4.6.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.SDK | .NET Framework 4.7.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.TargetingPack | .NET Framework 4.7.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.SDK | .NET Framework 4.7 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET Framework 4.7 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET Framework 4.6.1 開發工具 | 16.0.28621.142 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET Framework 4.6.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET Framework 4.7.1 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET Framework 4.7 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.Core.Component.SDK.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET Core 2.1 開發工具 | 16.0.28516.191 | Optional
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET Core 2.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.VisualStudio.Component.CodeClone | 程式碼複製品 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.CodeMap | Code Map | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | 即時相依性驗證 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.FSharp | F# 語言支援 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.FSharp.Desktop | F# 桌面語言支援 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.GraphDocument | DGML 編輯器 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | Optional
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.PortableLibrary | .NET 可攜式程式庫目標套件 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | 架構與分析工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | Optional

## <a name="game-development-with-unity"></a>使用 Unity 的遊戲程式開發

**識別碼：** Microsoft.VisualStudio.Workload.ManagedGame

**描述：** 使用強大的跨平台開發環境 Unity 來建立 2D 和 3D 遊戲。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Net.Component.3.5.DeveloperTools | .NET Framework 3.5 開發工具 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.1.TargetingPack | .NET Framework 4.7.1 目標套件 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Unity | Visual Studio Tools for Unity | 16.0.28315.86 | 必要
Component.UnityEngine.x64 | Unity 2018.3 64 位元編輯器 | 16.0.28707.178 | 建議
Component.UnityEngine.x86 | Unity 5.6 32 位元編輯器 | 16.0.28707.178 | 建議

## <a name="linux-development-with-c"></a>使用 C++ 的 Linux 程式開發

**識別碼：** Microsoft.VisualStudio.Workload.NativeCrossPlat

**描述：** 建立和偵錯 Linux 環境中執行的應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.MDD.Linux | 適用於 Linux 開發的 C++ | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Windows10SDK | Windows 通用 C 執行階段 | 16.0.28315.86 | 必要
Component.Linux.CMake | 適用於 Linux 的 C++ CMake 工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 建議
Component.MDD.Linux.GCC.arm | 內嵌與 IoT 開發工具 | 16.0.28625.61 | Optional

## <a name="desktop-development-with-c"></a>使用 C++ 的桌面開發

**識別碼：** Microsoft.VisualStudio.Workload.NativeDesktop

**描述：** 使用 Microsoft C++ 工具組、ATL 或 MFC 來建置 Windows 傳統型應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.ClassDesigner | 類別設計工具 | 16.0.28528.71 | 必要
Microsoft.VisualStudio.Component.CodeMap | Code Map | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.GraphDocument | DGML 編輯器 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++ 2019 可轉散發更新 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Native | 適用於 C++ 的架構工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | Visual C++ 核心桌面功能 | 16.0.28315.86 | 必要
Component.Microsoft.VisualStudio.LiveShare | Live Share | 1.0.12 | 建議
Microsoft.VisualStudio.Component.Debugger.JustInTime | Just-in-Time 偵錯工具 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.Graphics.Tools | 適用於 DirectX 的圖形偵錯工具與 GPU 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.VC.ATL | 適用於 v142 建置工具的 C++ ALT (x86 & x64) | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.VC.CMake.Project | 適用於 Windows 的 C++ CMake 工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.VC.TestAdapterForBoostTest | Boost.Test 的測試配接器 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.VC.TestAdapterForGoogleTest | 適用於 Google Test 的測試配接器 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 建議
Component.Incredibuild | IncrediBuild - 組建加速 | 16.0.28528.71 | Optional
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.3 | Optional
Microsoft.Component.VC.Runtime.UCRTSDK | Windows 通用 CRT SDK | 16.0.28625.61 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.VC.140 | MSVC v140 - VS 2015 C++ 建置工具 (v14.00) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.ATLMFC | 適用於 v142 建置工具的 C++ MFC (x86 & x64) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.CLI.Support | 適用於 v142 建置工具的 C++/CLI 支援 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | 適用於 v142 建置工具的 C++ 模組 (x64/x86 – 實驗性) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.v141.x86.x64 | MSVC v141 – VS 2017 C++ x64/x86 建置工具 (v14.16) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | Optional

## <a name="game-development-with-c"></a>使用 C++ 的遊戲程式開發

**識別碼：** Microsoft.VisualStudio.Workload.NativeGame

**描述：** 使用 C++ 的完整功能來建置採用 DirectX、Unreal 或 Cocos2d 技術的專業遊戲。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++ 2019 可轉散發更新 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Windows10SDK | Windows 通用 C 執行階段 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.Graphics.Tools | 適用於 DirectX 的圖形偵錯工具與 GPU 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | 建議
Component.Android.NDK.R16B | Android NDK (R16B) | 16.0.28728.38 | Optional
Component.Android.SDK25.Private | Android SDK 安裝程式 (API 層級 25) (可用於以 C++ 進行行動裝置開發的本機安裝) | 16.0.28625.61 | Optional
Component.Ant | Apache Ant (1.9.3) | 1.9.3.8 | Optional
Component.Cocos | Cocos | 16.0.28315.86 | Optional
Component.Incredibuild | IncrediBuild - 組建加速 | 16.0.28528.71 | Optional
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.3 | Optional
Component.MDD.Android | C++ Android 開發工具 | 16.0.28517.75 | Optional
Component.OpenJDK | OpenJDK (Microsoft 散發) | 16.0.28625.61 | Optional
Component.Unreal | Unreal Engine 安裝程式 | 16.0.28625.61 | Optional
Component.Unreal.Android | Unreal 引擎的 Android IDE 支援 | 16.0.28625.61 | Optional
Microsoft.Net.Component.4.5.1.TargetingPack | .NET Framework 4.5.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET Framework 4.6.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.TargetingPack | .NET Framework 4.6 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.TargetingPack | .NET Framework 4 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET Framework 4 – 4.6 開發工具 | 16.0.28516.191 | Optional
Microsoft.VisualStudio.Component.NuGet.BuildTools | NuGet 目標和建置工作 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | Optional
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | Optional

## <a name="mobile-development-with-c"></a>使用 C++ 的行動裝置程式開發

**識別碼：** Microsoft.VisualStudio.Workload.NativeMobile

**描述：** 使用 C++ 來建置 iOS、Android 或 Windows 的跨平台應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Android.SDK25.Private | Android SDK 安裝程式 (API 層級 25) (可用於以 C++ 進行行動裝置開發的本機安裝) | 16.0.28625.61 | 必要
Component.OpenJDK | OpenJDK (Microsoft 散發) | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | 必要
Component.Android.NDK.R16B | Android NDK (R16B) | 16.0.28728.38 | 建議
Component.Ant | Apache Ant (1.9.3) | 1.9.3.8 | 建議
Component.MDD.Android | C++ Android 開發工具 | 16.0.28517.75 | 建議
Component.Android.NDK.R16B_3264 | Android NDK (R16B) (32 位元) | 16.0.28728.38 | Optional
Component.Google.Android.Emulator.API25.Private | Google Android 模擬器 (API 層級 25) (本機安裝) | 16.0.28625.61 | Optional
Component.HAXM.Private | Intel Hardware Accelerated Execution Manager (HAXM) (本機安裝) | 16.0.28528.71 | Optional
Component.Incredibuild | IncrediBuild - 組建加速 | 16.0.28528.71 | Optional
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.3 | Optional
Component.MDD.IOS | C++ iOS 開發工具 | 16.0.28517.75 | Optional

## <a name="net-core-cross-platform-development"></a>.NET Core 跨平台開發

**識別碼：** Microsoft.VisualStudio.Workload.NetCoreTools

**描述：** 使用 .NET Core、ASP.NET Core、HTML/JavaScript 及包括 Docker 支援的容器來建置跨平台應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | 必要
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | 必要
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET Core 2.1 開發工具 | 16.0.28516.191 | 必要
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.FSharp | F# 語言支援 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.FSharp.WebTemplates | Web 專案的 F# 語言支援 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 必要
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 必要
Component.Microsoft.VisualStudio.LiveShare | Live Share | 1.0.12 | 建議
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure WebJobs 工具 | 16.0.28714.129 | 建議
Microsoft.VisualStudio.Component.AppInsights.Tools | 開發人員分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure 製作工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.ClientLibs | Azure Libraries for .NET | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure 計算模擬器 | 16.0.28720.110 | 建議
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure 儲存體模擬器 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Debugger.Snapshot | 快照集偵錯工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Debugger.TimeTravel | 時間移動偵錯工具 | 16.0.28714.129 | 建議
Microsoft.VisualStudio.Component.DiagnosticTools | .NET 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.LiveUnitTesting | Live Unit Testing | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure WebJobs 工具 | 16.0.28621.142 | 建議
Microsoft.VisualStudio.ComponentGroup.Web.CloudTools | 適用於 Web 開發的雲端工具 | 16.0.28621.142 | 建議
Microsoft.Net.Core.Component.SDK.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET Core 2.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.NetCore.ComponentGroup.Web.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | 開發時間的 IIS 支援 | 16.0.28315.86 | Optional

## <a name="mobile-development-with-net"></a>使用 .NET 的行動應用程式開發

**識別碼：** Microsoft.VisualStudio.Workload.NetCrossPlat

**描述：** 使用 Xamarin 來建置 iOS、Android 或 Windows 的跨平台應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Xamarin | Xamarin | 16.0.28625.61 | 必要
Component.Xamarin.RemotedSimulator | Xamarin Remoted Simulator | 16.0.28315.86 | 必要
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET Core 2.1 開發工具 | 16.0.28516.191 | 必要
Microsoft.VisualStudio.Component.FSharp | F# 語言支援 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.Merq | 通用的 Xamarin 內部工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.MonoDebugger | Mono 偵錯工具 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions.TemplateEngine | ASP.NET 範本引擎 | 16.0.28315.86 | 必要
Component.Android.SDK27 | Android SDK 安裝程式 (API 層級 27) | 16.0.28517.75 | 建議
Component.OpenJDK | OpenJDK (Microsoft 散發) | 16.0.28625.61 | 建議

## <a name="aspnet-and-web-development"></a>ASP.NET 與網頁程式開發

**識別碼：** Microsoft.VisualStudio.Workload.NetWeb

**描述：** 使用 ASP.NET、ASP.NET Core、HTML/JavaScript 及包括 Docker 支援的容器來建置 Web 應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | 必要
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | 必要
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET Core 2.1 開發工具 | 16.0.28516.191 | 必要
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.FSharp | F# 語言支援 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.FSharp.WebTemplates | Web 專案的 F# 語言支援 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 必要
Component.Microsoft.VisualStudio.LiveShare | Live Share | 1.0.12 | 建議
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure WebJobs 工具 | 16.0.28714.129 | 建議
Microsoft.Net.Component.4.5.1.TargetingPack | .NET Framework 4.5.1 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.6.TargetingPack | .NET Framework 4.6 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.TargetingPack | .NET Framework 4 目標套件 | 16.0.28517.75 | 建議
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET Framework 4 – 4.6 開發工具 | 16.0.28516.191 | 建議
Microsoft.VisualStudio.Component.AppInsights.Tools | 開發人員分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.AspNet45 | 進階的 ASP.NET 功能 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure 製作工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Azure.ClientLibs | Azure Libraries for .NET | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure 計算模擬器 | 16.0.28720.110 | 建議
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure 儲存體模擬器 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Debugger.Snapshot | 快照集偵錯工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.Debugger.TimeTravel | 時間移動偵錯工具 | 16.0.28714.129 | 建議
Microsoft.VisualStudio.Component.DiagnosticTools | .NET 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 工具 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.LiveUnitTesting | Live Unit Testing | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure WebJobs 工具 | 16.0.28621.142 | 建議
Microsoft.VisualStudio.ComponentGroup.Web.CloudTools | 適用於 Web 開發的雲端工具 | 16.0.28621.142 | 建議
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.SDK | .NET Framework 4.6.2 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET Framework 4.6.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.SDK | .NET Framework 4.7.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.TargetingPack | .NET Framework 4.7.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.SDK | .NET Framework 4.7 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET Framework 4.7 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET Framework 4.6.1 開發工具 | 16.0.28621.142 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET Framework 4.6.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET Framework 4.7.1 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET Framework 4.7 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.Core.Component.SDK.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET Core 2.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.NetCore.ComponentGroup.Web.2.2 | .NET Core 2.2 開發工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.Component.CodeClone | 程式碼複製品 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.CodeMap | Code Map | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | 即時相依性驗證 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.GraphDocument | DGML 編輯器 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.TestTools.WebLoadTest | Web 效能與負載測試工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | Optional
Microsoft.VisualStudio.ComponentGroup.AdditionalWebProjectTemplates | 其他專案範本 (舊版) | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | 架構與分析工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | 開發時間的 IIS 支援 | 16.0.28315.86 | Optional

## <a name="nodejs-development"></a>Node.js 開發

**識別碼：** Microsoft.VisualStudio.Workload.Node

**描述：** 使用非同步事件驅動的 JavaScript 執行階段 Node.js 來建置可調整網路應用程式。 

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Node.Tools | Node.js 開發工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 必要
Component.Microsoft.VisualStudio.LiveShare | Live Share | 1.0.12 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.AppInsights.Tools | 開發人員分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | Optional

## <a name="officesharepoint-development"></a>Office/SharePoint 程式開發

**識別碼：** Microsoft.VisualStudio.Workload.Office

**描述：** 使用 C#、VB 及 JavaScript 來建立 Office 與 SharePoint 增益集、SharePoint 解決方案，以及 VSTO 增益集。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | 必要
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | 必要
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.1.TargetingPack | .NET Framework 4.6.1 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.TargetingPack | .NET Framework 4 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.AppInsights.Tools | 開發人員分析工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | .NET 桌面開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Sharepoint.Tools | Office Developer Tools for Visual Studio | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.Workflow | Windows Workflow Foundation | 16.0.28315.86 | 必要
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.TeamOffice | Visual Studio Tools for Office (VSTO) | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.SDK | .NET Framework 4.6.2 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | .NET Framework 4.6.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.SDK | .NET Framework 4.7.1 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.1.TargetingPack | .NET Framework 4.7.1 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.SDK | .NET Framework 4.7 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.TargetingPack | .NET Framework 4.7 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET Framework 4.6.1 開發工具 | 16.0.28621.142 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET Framework 4.6.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET Framework 4.7.1 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET Framework 4.7 開發工具 | 16.0.28516.191 | Optional
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Optional
Microsoft.VisualStudio.ComponentGroup.Sharepoint.WIF | Windows Identity Foundation 3.5 | 16.0.28621.142 | Optional

## <a name="python-development"></a>Python 開發

**識別碼：** Microsoft.VisualStudio.Workload.Python

**描述：** 適用於 Python 的編輯、偵錯、互動式開發及原始檔控制。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Component.PythonTools | Python 語言支援 | 16.0.28625.61 | 必要
Component.CPython3.x64 | Python 3 64 位元 (3.7.2) | 3.7.2 | 建議
Component.Microsoft.VisualStudio.LiveShare | Live Share | 1.0.12 | 建議
Microsoft.Component.PythonTools.Minicondax64 | Python miniconda | 16.0.28625.61 | 建議
Microsoft.Component.PythonTools.Web | Python Web 支援 | 16.0.28517.75 | 建議
Microsoft.VisualStudio.Component.Common.Azure.Tools | 連接與發行工具 | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.WebDeploy | Web Deploy | 16.0.28517.75 | 建議
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 建議
Component.CPython2.x64 | Python 2 64 位元 (2.7.15) | 2.7.15 | Optional
Component.CPython2.x86 | Python 2 32 位元 (2.7.15) | 2.7.15 | Optional
Component.CPython3.x86 | Python 3 32 位元 (3.7.2) | 3.7.2 | Optional
Component.Microsoft.VisualStudio.RazorExtension | Razor 語言服務 | 16.0.28714.129 | Optional
Component.Microsoft.Web.LibraryManager | 程式庫管理員 | 16.0.28315.86 | Optional
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Optional
Microsoft.Component.VC.Runtime.UCRTSDK | Windows 通用 CRT SDK | 16.0.28625.61 | Optional
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Python 原生開發工具 | 16.0.28621.142 | Optional
Microsoft.Net.Component.4.5.2.TargetingPack | .NET Framework 4.5.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | Optional
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | Optional
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | Optional
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure 製作工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Azure.ClientLibs | Azure Libraries for .NET | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure 計算模擬器 | 16.0.28720.110 | Optional
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure 儲存體模擬器 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Azure.Waverton | Azure 雲端服務核心工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure 雲端服務建置工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.DockerTools | 容器開發工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Graphics.Tools | 適用於 DirectX 的圖形偵錯工具與 GPU 分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Managed 桌面工作負載核心 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC 驅動程式 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server Command Line Utilities | 16.0.28707.177 | Optional
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | Optional
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL 執行階段 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.SQL.DataSources | SQL Server 支援的資料來源 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Data Tools | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.140 | MSVC v140 - VS 2015 C++ 建置工具 (v14.00) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ 分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Web | ASP.NET 與網頁程式開發工具 | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Windows10SDK | Windows 通用 C 執行階段 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | Optional
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET 和 Web 開發工具的必要條件 | 16.0.28621.142 | Optional

## <a name="universal-windows-platform-development"></a>通用 Windows 平台開發

**識別碼：** Microsoft.VisualStudio.Workload.Universal

**描述：** 使用 C#、VB 或選用 C++，來建立適用於通用 Windows 平台的應用程式。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Component.NetFX.Native | .NET Native | 16.0.28315.86 | 必要
Microsoft.ComponentGroup.Blend | Blend for Visual Studio | 16.0.28315.86 | 必要
Microsoft.Net.Component.4.5.TargetingPack | .NET Framework 4.5 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Core.Component.SDK.2.1 | .NET Core 2.1 開發工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.AppInsights.Tools | 開發人員分析工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.DiagnosticTools | .NET 分析工具 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Graphics | 影像與 3D 模型編輯器 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript 診斷 | 16.0.28517.75 | 必要
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript 與 TypeScript 語言支援 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server 的 CLR 資料類型 | 16.0.28315.86 | 必要
Microsoft.VisualStudio.Component.TypeScript.3.3 | TypeScript 3.3 SDK | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | 必要
Microsoft.VisualStudio.ComponentGroup.UWP.NetCoreAndStandard | .NET Native 和.NET Standard | 16.0.28516.191 | 必要
Microsoft.VisualStudio.ComponentGroup.UWP.Support | 通用 Windows 平台工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | 適用於 Xamarin 的通用 Windows 平台工具 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET 與網頁程式開發 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Optional
Microsoft.Component.VC.Runtime.OSSupport | 適用於 v142 建置工具的 C++ 通用 Windows 平台執行階段 | 16.0.28625.61 | Optional
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.ClassDesigner | 類別設計工具 | 16.0.28528.71 | Optional
Microsoft.VisualStudio.Component.CodeClone | 程式碼複製品 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.CodeMap | Code Map | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | 即時相依性驗證 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.GraphDocument | DGML 編輯器 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Graphics.Tools | 適用於 DirectX 的圖形偵錯工具與 GPU 分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.UWP.VC.ARM64 | 適用於 v142 建置工具 (ARM64) 的 C++ 通用 Windows 平台支援 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++ 2019 可轉散發更新 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.ARM | MSVC v142 – VS 2019 C++ ARM 建置工具 (v14.20) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | MSVC v142 – VS 2019 C++ ARM64 建置工具 (v14.20) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.v141.ARM | MSVC v141 – VS 2017 C++ ARM 建置工具 (v14.16) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.v141.ARM64 | MSVC v141 – VS 2017 C++ ARM64 建置工具 (v14.16) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.v141.x86.x64 | MSVC v141 – VS 2017 C++ x64/x86 建置工具 (v14.16) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.IpOverUsb | USB 裝置連線 | 16.0.28320.51 | Optional
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | 架構與分析工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Native | 適用於 C++ 的架構工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | Visual C++ 核心桌面功能 | 16.0.28315.86 | Optional
Microsoft.VisualStudio.ComponentGroup.UWP.VC | C++ (v142) 通用 Windows 平台工具 | 16.0.28621.142 | Optional
Microsoft.VisualStudio.ComponentGroup.UWP.VC.v141 | C++ (v141) 通用 Windows 平台工具 | 16.0.28621.142 | Optional

## <a name="visual-studio-extension-development"></a>Visual Studio 擴充功能開發

**識別碼：** Microsoft.VisualStudio.Workload.VisualStudioExtension

**描述：** 建立適用於 Visual Studio 的增益集與延伸模組，包括新的命令、程式碼分析器與工具視窗。

### <a name="components-included-by-this-workload"></a>此工作負載所包含的元件

元件識別碼 | 名稱 | 版本 | 相依性類型
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.6.TargetingPack | .NET Framework 4.6 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.SDK | .NET Framework 4.7.2 SDK | 16.0.28517.75 | 必要
Microsoft.Net.Component.4.7.2.TargetingPack | .NET Framework 4.7.2 目標套件 | 16.0.28517.75 | 必要
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.7.2 開發工具 | 16.0.28516.191 | 必要
Microsoft.VisualStudio.Component.NuGet | NuGet 套件管理員 | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# 與 Visual Basic Roslyn 編譯程式 | 16.0.28714.129 | 必要
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# 和 Visual Basic | 16.0.28625.61 | 必要
Microsoft.VisualStudio.Component.VSSDK | Visual Studio SDK | 16.0.28315.86 | 必要
Microsoft.VisualStudio.ComponentGroup.VisualStudioExtension.Prerequisites | Visual Studio 擴充功能開發必要條件 | 16.0.28621.142 | 必要
Microsoft.VisualStudio.Component.DiagnosticTools | .NET 分析工具 | 16.0.28625.61 | 建議
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | 建議
Microsoft.VisualStudio.Component.TextTemplating | 文字範本轉換 | 16.0.28625.61 | 建議
Component.Dotfuscator | PreEmptive Protection - Dotfuscator | 16.0.28528.71 | Optional
Microsoft.Component.CodeAnalysis.SDK | .NET Compiler Platform SDK | 16.0.28625.61 | Optional
Microsoft.Component.VC.Runtime.OSSupport | 適用於 v142 建置工具的 C++ 通用 Windows 平台執行階段 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.AppInsights.Tools | 開發人員分析工具 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.ClassDesigner | 類別設計工具 | 16.0.28528.71 | Optional
Microsoft.VisualStudio.Component.CodeClone | 程式碼複製品 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.CodeMap | Code Map | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | 即時相依性驗證 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.DslTools | Modeling SDK | 16.0.28315.86 | Optional
Microsoft.VisualStudio.Component.GraphDocument | DGML 編輯器 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.ATL | 適用於 v142 建置工具的 C++ ALT (x86 & x64) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.ATLMFC | 適用於 v142 建置工具的 C++ MFC (x86 & x64) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.CoreIde | C++ 核心功能 | 16.0.28625.61 | Optional
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 建置工具 (v14.20) | 16.0.28625.61 | Optional
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | 架構與分析工具 | 16.0.28621.142 | Optional

## <a name="unaffiliated-components"></a>非附屬元件

這些是未隨附於任何工作負載但可選取來作為個別元件的元件。

元件識別碼 | 名稱 | 版本
--- | --- | ---
Component.GitHub.VisualStudio | Visual Studio 的 GitHub 擴充功能 | 2.5.9.5485
Component.Xamarin.Inspector | Xamarin Inspector | 16.0.28315.86
Component.Xamarin.Profiler | Xamarin Profiler | 16.0.28315.86
Component.Xamarin.Workbooks | Xamarin Workbooks | 16.0.28315.86
Microsoft.Component.ClickOnce | ClickOnce 發行 | 16.0.28707.177
Microsoft.Component.HelpViewer | 說明檢視器 | 16.0.28625.61
Microsoft.NetCore.1x.ComponentGroup.Web | 適用於網路的 .NET Core 1.0 - 1.1 開發工具 | 16.0.28621.142
Microsoft.VisualStudio.Component.AzureDevOps.OfficeIntegration | Azure DevOps Office 整合 | 16.0.28625.61
Microsoft.VisualStudio.Component.Git | 適用於 Windows 的 Git | 16.0.28625.61
Microsoft.VisualStudio.Component.LinqToSql | LINQ to SQL 工具 | 16.0.28625.61
Microsoft.VisualStudio.Component.TestTools.CodedUITest | 自動程式碼 UI 測試 | 16.0.28327.66
Microsoft.VisualStudio.Component.VC.ATL.ARM | 適用於 v142 建置工具的 C++ ALT (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM.Spectre | 適用於 v142 建置工具且具有 Spectre 風險降低功能的 C++ ATL (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM64 | 適用於 v142 建置工具的 C++ ALT (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM64.Spectre | 適用於 v142 建置工具且具有 Spectre 風險降低功能的 C++ ATL (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.Spectre | 適用於 v142 建置工具且具有 Spectre 風險降低功能的 C++ ATL (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATLMFC.Spectre | 適用於 v142 建置工具且具有 Spectre 風險降低功能的 C++ MFC (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM | 適用於 v142 建置工具的 C++ MFC (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM.Spectre | 適用於 v142 建置工具且具有 Spectre 風險降低功能的 C++ MFC (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM64 | 適用於 v142 建置工具的 C++ MFC (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM64.Spectre | 適用於 v142 建置工具且具有 Spectre 風險降低功能的 C++ MFC (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Redist.MSM | C++ 2019 可轉散發 MSM | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.ARM.Spectre | MSVC v142 – VS 2019 C++ ARM 已開啟 Spectre 風險降低功能的程式庫 (v14.20) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.ARM64.Spectre | MSVC v142 – VS 2019 C++ ARM64 已開啟 Spectre 風險降低功能的程式庫 (v14.20) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.x86.x64.Spectre | MSVC v142 – VS 2019 C++ x64/x86 已開啟 Spectre 風險降低功能的程式庫 (v14.20)  | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ARM.Spectre | MSVC v141 – VS 2017 C++ ARM 已開啟 Spectre 風險降低功能的程式庫 (v14.16) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ARM64.Spectre | MSVC v141 – VS 2017 C++ ARM64 已開啟 Spectre 風險降低功能的程式庫 (v14.16) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL | 適用於 v141 建置工具的 C++ ALT (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM | 適用於 v141 建置工具的 C++ ALT (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM.Spectre | 適用於 v141 建置工具且具有 Spectre 風險降低功能的 C++ ATL (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM64 | 適用於 v141 建置工具的 C++ ALT (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM64.Spectre | 適用於 v141 建置工具且具有 Spectre 風險降低功能的 C++ ATL (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.Spectre | 適用於 v141 建置工具且具有 Spectre 風險降低功能的 C++ ATL (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.CLI.Support | 適用於 v141 建置工具的 C++/CLI 支援 | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC | 適用於 v141 建置工具的 C++ MFC (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM | 適用於 v141 建置工具的 C++ MFC (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM.Spectre | 適用於 v141 建置工具且具有 Spectre 風險降低功能的 C++ MFC (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM64 | 適用於 v141 建置工具的 C++ MFC (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM64.Spectre | 適用於 v141 建置工具且具有 Spectre 風險降低功能的 C++ MFC (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.Spectre | 適用於 v141 建置工具且具有 Spectre 風險降低功能的 C++ MFC (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.x86.x64.Spectre | MSVC v141 – VS 2017 C++ x64/x86 已開啟 Spectre 風險降低功能的程式庫 (v14.16) | 16.0.28625.61
Microsoft.VisualStudio.Component.VisualStudioData | 資料來源與服務參考 | 16.0.28707.177
Microsoft.VisualStudio.Component.WinXP | 適用於 VS 2017 (v141) 工具的 C++ Windows XP 支援 [已淘汰] | 16.0.28625.61
Microsoft.VisualStudio.Web.Mvc4.ComponentGroup | ASP.NET MVC 4 | 16.0.28621.142
