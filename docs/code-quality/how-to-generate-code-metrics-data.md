---
title: 從 IDE 或命令列產生程式碼度量
ms.date: 11/02/2018
ms.topic: conceptual
helpviewer_keywords:
- code metrics data
- code metrics results
- code metrics [Visual Studio]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4275e92b21289c5cf1e3243b2bc782a9e0821fde
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59232745"
---
# <a name="how-to-generate-code-metrics-data"></a>HOW TO：產生程式碼度量資料

您可以透過三種方式產生程式碼計量資料：

- 藉由安裝[FxCop 分析器](#fxcop-analyzers-code-metrics-rules)並讓它包含四個程式碼度量 （可維護性） 規則。

- 藉由選擇[**分析** > **計算程式碼度量**](#calculate-code-metrics-menu-command) Visual Studio 中的功能表命令。

- 從[命令列](#command-line-code-metrics)的C#和 Visual Basic 專案。

## <a name="fxcop-analyzers-code-metrics-rules"></a>FxCop 分析器，程式碼計量規則

[FxCopAnalyzers NuGet 套件](https://www.nuget.org/packages/Microsoft.CodeAnalysis.FxCopAnalyzers)包含數個程式碼度量[分析器](roslyn-analyzers-overview.md)規則：

- [CA1501](ca1501-avoid-excessive-inheritance.md)
- [CA1502](ca1502-avoid-excessive-complexity.md)
- [CA1505](ca1505-avoid-unmaintainable-code.md)
- [CA1506](ca1506-avoid-excessive-class-coupling.md)

預設會停用這些規則，但您也可以將它們從啟用[**方案總管**](use-roslyn-analyzers.md#set-rule-severity-from-solution-explorer)或在[規則集](using-rule-sets-to-group-code-analysis-rules.md)檔案。 例如，若要啟用規則 CA1502 為警告，.ruleset 檔案會包含下列項目：

```xml
<?xml version="1.0" encoding="utf-8"?>
<RuleSet Name="Rules" Description="Rules" ToolsVersion="16.0">
  <Rules AnalyzerId="Microsoft.CodeQuality.Analyzers" RuleNamespace="Microsoft.CodeQuality.Analyzers">
    <Rule Id="CA1502" Action="Warning" />
  </Rules>
</RuleSet>
```

### <a name="configuration"></a>組態

您可以設定的 FxCop 分析器中的程式碼度量規則封裝火災的臨界值。

1. 建立文字檔 例如，您可以將它命名*CodeMetricsConfig.txt*。

2. 以下列格式的文字檔案中加入想要的閾值：

   ```txt
   CA1502: 10
   ```

   在此範例中，規則[CA1502](ca1502-avoid-excessive-complexity.md)設定方法的循環複雜度大於 10 時引發。

3. 在 **屬性**視窗的 Visual Studio，或在專案檔中，標示為組態檔的建置動作[ **AdditionalFiles**](../ide/build-actions.md#build-action-values)。 例如: 

   ```xml
   <ItemGroup>
     <AdditionalFiles Include="CodeMetricsConfig.txt" />
   </ItemGroup>
   ```

## <a name="calculate-code-metrics-menu-command"></a>計算程式碼度量功能表命令

使用在 IDE 中產生的一個或所有開啟的專案程式碼度量**分析** > **計算程式碼度量**功能表。

### <a name="generate-code-metrics-results-for-an-entire-solution"></a>產生整個方案的程式碼度量結果

您可以使用下列任一方式來產生整個方案的程式碼度量結果：

- 從功能表列中，選擇**分析** > **計算程式碼度量** > **方案**。

- 在 **方案總管**，以滑鼠右鍵按一下方案，然後選擇**計算程式碼度量**。

- 在 **程式碼度量結果** 視窗中，選擇**計算方案的程式碼度量** 按鈕。

就會產生結果和**程式碼度量結果** 視窗隨即顯示。 若要檢視結果的詳細資訊，請展開 樹狀目錄中的**階層**資料行。

### <a name="generate-code-metrics-results-for-one-or-more-projects"></a>產生一個或多個專案的程式碼度量結果

1. 在 [**方案總管] 中**，選取一或多個專案。

1. 從功能表列中，選擇**分析** > **計算程式碼度量** > **針對選取的專案**。

就會產生結果和**程式碼度量結果** 視窗隨即顯示。 若要檢視結果的詳細資訊，請展開 樹狀目錄中的**階層**。

::: moniker range="vs-2017"

> [!NOTE]
> **計算程式碼度量**命令不適用於.NET Core 和.NET Standard 專案。 若要計算的.NET Core 或.NET Standard 專案的程式碼度量，您可以：
>
> - 計算從程式碼度量[命令列](#command-line-code-metrics)改為
>
> - 升級至[Visual Studio 2019](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019)

::: moniker-end

## <a name="command-line-code-metrics"></a>命令列程式碼度量

您可以從命令列來產生程式碼計量資料C#和.NET Framework、.NET Core 和.NET Standard 的應用程式的 Visual Basic 專案。 若要從命令列中執行程式碼度量資訊，請安裝[Microsoft.CodeAnalysis.Metrics NuGet 套件](#microsoftcodeanalysismetrics-nuget-package)或 建置[Metrics.exe](#metricsexe)可執行您自己。

### <a name="microsoftcodeanalysismetrics-nuget-package"></a>Microsoft.CodeAnalysis.Metrics NuGet 套件

若要從命令列產生程式碼度量資料的最簡單方式是安裝[Microsoft.CodeAnalysis.Metrics](https://www.nuget.org/packages/Microsoft.CodeAnalysis.Metrics/) NuGet 套件。 您已安裝封裝之後，執行`msbuild /t:Metrics`從包含您的專案檔的目錄。 例如：

```shell
C:\source\repos\ClassLibrary3\ClassLibrary3>msbuild /t:Metrics
Microsoft (R) Build Engine version 16.0.360-preview+g9781d96883 for .NET Framework
Copyright (C) Microsoft Corporation. All rights reserved.

Build started 1/22/2019 4:29:57 PM.
Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" on node 1 (Metrics target(s))
.
Metrics:
  C:\source\repos\ClassLibrary3\packages\Microsoft.CodeMetrics.2.6.4-ci\build\\..\Metrics\Metrics.exe /project:C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj /out:ClassLibrary3.Metrics.xml
  Loading ClassLibrary3.csproj...
  Computing code metrics for ClassLibrary3.csproj...
  Writing output to 'ClassLibrary3.Metrics.xml'...
  Completed Successfully.
Done Building Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" (Metrics target(s)).

Build succeeded.
    0 Warning(s)
    0 Error(s)
```

您可以藉由指定覆寫輸出檔名稱`/p:MetricsOutputFile=<filename>`。 您也可以取得[舊式](#previous-versions)藉由指定的程式碼度量資料`/p:LEGACY_CODE_METRICS_MODE=true`。 例如: 

```shell
C:\source\repos\ClassLibrary3\ClassLibrary3>msbuild /t:Metrics /p:LEGACY_CODE_METRICS_MODE=true /p:MetricsOutputFile="Legacy.xml"
Microsoft (R) Build Engine version 16.0.360-preview+g9781d96883 for .NET Framework
Copyright (C) Microsoft Corporation. All rights reserved.

Build started 1/22/2019 4:31:00 PM.
The "MetricsOutputFile" property is a global property, and cannot be modified.
Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" on node 1 (Metrics target(s))
.
Metrics:
  C:\source\repos\ClassLibrary3\packages\Microsoft.CodeMetrics.2.6.4-ci\build\\..\Metrics.Legacy\Metrics.Legacy.exe /project:C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj /out:Legacy.xml
  Loading ClassLibrary3.csproj...
  Computing code metrics for ClassLibrary3.csproj...
  Writing output to 'Legacy.xml'...
  Completed Successfully.
Done Building Project "C:\source\repos\ClassLibrary3\ClassLibrary3\ClassLibrary3.csproj" (Metrics target(s)).

Build succeeded.
    0 Warning(s)
    0 Error(s)
```

### <a name="code-metrics-output"></a>程式碼度量資訊輸出

產生的 XML 輸出的格式如下：

```xml
<?xml version="1.0" encoding="utf-8"?>
<CodeMetricsReport Version="1.0">
  <Targets>
    <Target Name="ConsoleApp20.csproj">
      <Assembly Name="ConsoleApp20, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null">
        <Metrics>
          <Metric Name="MaintainabilityIndex" Value="100" />
          <Metric Name="CyclomaticComplexity" Value="1" />
          <Metric Name="ClassCoupling" Value="1" />
          <Metric Name="DepthOfInheritance" Value="1" />
          <Metric Name="LinesOfCode" Value="11" />
        </Metrics>
        <Namespaces>
          <Namespace Name="ConsoleApp20">
            <Metrics>
              <Metric Name="MaintainabilityIndex" Value="100" />
              <Metric Name="CyclomaticComplexity" Value="1" />
              <Metric Name="ClassCoupling" Value="1" />
              <Metric Name="DepthOfInheritance" Value="1" />
              <Metric Name="LinesOfCode" Value="11" />
            </Metrics>
            <Types>
              <NamedType Name="Program">
                <Metrics>
                  <Metric Name="MaintainabilityIndex" Value="100" />
                  <Metric Name="CyclomaticComplexity" Value="1" />
                  <Metric Name="ClassCoupling" Value="1" />
                  <Metric Name="DepthOfInheritance" Value="1" />
                  <Metric Name="LinesOfCode" Value="7" />
                </Metrics>
                <Members>
                  <Method Name="void Program.Main(string[] args)" File="C:\source\repos\ConsoleApp20\ConsoleApp20\Program.cs" Line="7">
                    <Metrics>
                      <Metric Name="MaintainabilityIndex" Value="100" />
                      <Metric Name="CyclomaticComplexity" Value="1" />
                      <Metric Name="ClassCoupling" Value="1" />
                      <Metric Name="LinesOfCode" Value="4" />
                    </Metrics>
                  </Method>
                </Members>
              </NamedType>
            </Types>
          </Namespace>
        </Namespaces>
      </Assembly>
    </Target>
  </Targets>
</CodeMetricsReport>
```

### <a name="metricsexe"></a>Metrics.exe

如果您不想要安裝 NuGet 套件，您可以產生，並使用*Metrics.exe*直接可執行檔。 若要產生*Metrics.exe*可執行檔：

1. 複製品[dotnet/roslyn 分析器](https://github.com/dotnet/roslyn-analyzers)存放庫。
2. 系統管理員身分開啟 Visual studio 的開發人員命令提示字元。
3. 從根目錄**roslyn 分析器**存放庫中，執行下列命令： `Restore.cmd`
4. 將目錄變更為*src\Tools*。
5. 執行下列命令來建置**Metrics.csproj**專案：

   ```shell
   msbuild /m /v:m /p:Configuration=Release Metrics.csproj
   ```

   為可執行檔*Metrics.exe*就會發出*artifacts\bin*存放庫根目錄下的目錄。

#### <a name="metricsexe-usage"></a>Metrics.exe 使用量

若要執行*Metrics.exe*、 提供專案或方案，輸出 XML 檔案做為引數。 例如：

```shell
C:\>Metrics.exe /project:ConsoleApp20.csproj /out:report.xml
Loading ConsoleApp20.csproj...
Computing code metrics for ConsoleApp20.csproj...
Writing output to 'report.xml'...
Completed Successfully.
```

#### <a name="legacy-mode"></a>傳統模式

您可以選擇建置*Metrics.exe*中*舊版模式*。 舊版模式版本的工具會產生計量的值接近什麼[舊版的工具產生](#previous-versions)。 此外，在舊版模式下， *Metrics.exe*相同方法的集合類型，舊版的工具產生的程式碼度量資訊會產生程式碼度量資訊。 比方說，它不會產生程式碼度量資料欄位和屬性的初始設定式。 基於回溯相容性，或如果您有閘道簽入的程式碼程式碼度量數字，則舊版模式會很有用。 命令，以建置*Metrics.exe*處於傳統模式：

```shell
msbuild /m /v:m /t:rebuild /p:LEGACY_CODE_METRICS_MODE=true Metrics.csproj
```

如需詳細資訊，請參閱 <<c0> [ 啟用傳統模式產生程式碼度量](https://github.com/dotnet/roslyn-analyzers/pull/1841)。

### <a name="previous-versions"></a>舊版本

Visual Studio 2015 包含也呼叫的命令列程式碼度量工具*Metrics.exe*。 這個舊版本的工具沒有二進位檔的分析，也就是組件為基礎的分析。 新*Metrics.exe*工具會改為分析原始程式碼。 因為新*Metrics.exe*工具是來源的程式碼為基礎、 命令列的程式碼度量結果有差異，以便產生由 Visual Studio IDE 和舊版的那些*Metrics.exe*。

新的命令列的程式碼度量工具會計算計量，即使來源的程式碼錯誤，只要載入方案和專案。

#### <a name="metric-value-differences"></a>度量值的差異

`LinesOfCode`度量是更精確且可靠，在新的命令列程式碼度量資訊工具。 它是獨立於任何 codegen 差異並不會變更為工具組或執行階段變更時。 新的工具會計算實際的程式碼，包括空白的行和註解的行數。

其他計量，例如`CyclomaticComplexity`並`MaintainabilityIndex`使用相同的公式為舊版*Metrics.exe*，但新的工具會計算數`IOperations`（邏輯來源指示） 而不是中繼language (IL) 指令。 數字會稍有不同所產生的 Visual Studio ide 和舊版*Metrics.exe*。

## <a name="see-also"></a>另請參閱

- [使用程式碼度量結果視窗](../code-quality/working-with-code-metrics-data.md)
- [程式碼度量值](../code-quality/code-metrics-values.md)
