---
title: 選項、文字編輯器、基本 (VB)、進階
ms.date: 01/16/2019
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Visual_Basic.Editor
- VS.ToolsOptionsPages.Text_Editor.Basic.Editor
- VS.ToolsOptionsPages.Visual_Basic_Editor.Editor
- VS.ToolsOptionsPages.Text_Editor.Basic.SimplifiedEditorPage
- VS.ToolsOptionsPages.Text_Editor.Basic
- VS.ToolsOptionsPages.Text_Editor.Basic.Advanced
- VS.ToolsOptionsPages.Text_Editor.Basic.VB_Specific
helpviewer_keywords:
- Basic Text Editor Options dialog box
ms.assetid: 5a8cafca-f7b4-4a2d-92ce-6894a7673d00
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8a7ea9c2efd6a204932e24de0ef250ba143b8b34
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55925458"
---
# <a name="options-text-editor-basic-visual-basic-advanced"></a>選項、文字編輯器、基本 (Visual Basic)、進階
位於 [選項] ([工具] 功能表) 對話方塊上 [文字編輯器] 資料夾的 [基本] 資料夾中的 [VB 專用] 屬性頁面包含下列屬性：

## <a name="analysis"></a>分析

- 啟用完整解決方案分析

   除了開啟程式碼檔案之外，您也必須為解決方案中的所有檔案啟用程式法分析。 如需詳細資訊，請參閱[完整解決方案分析](../../code-quality/how-to-enable-and-disable-full-solution-analysis-for-managed-code.md)。

## <a name="using-directives"></a>using 指示詞

- 排序 using 時先放置 'System' 指示詞

   選取後，快顯功能表中的 [移除並排序 Using] 命令會對 `using` 指示詞進行排序，並將 'System' 命名空間置於清單頂端。

- 使用指示詞群組來進行分隔

   選取後，快顯功能表中的 [移除並排序 Using] 命令會透過在具有相同根命名空間的指示詞群組之間插入空白行來分隔 `using` 指示詞。

- 為參考組件中的類型建議 Using
- 為 NuGet 套件中的類型建議 Using

   選取這些選項後，[快速動作](../quick-actions.md)可用來安裝 NuGet 套件，並為未參考的類型新增 `using` 指示詞。

   ![在 Visual Studio 中安裝 NuGet 套件的快速動作](media/nuget-lightbulb.png)


## <a name="highlighting"></a>醒目提示

 **啟用參考和關鍵字的反白顯示**

文字編輯器可以反白顯示符號的所有執行個體或子句中的所有關鍵字，例如 `If..Then`、`While...End While` 或 `Try...Catch...Finally`。 您可以按 **Ctrl** + **Shift** + **向下鍵**或 **Ctrl** + **Shift** + **向上鍵**，在反白顯示的參考或關鍵字之間巡覽。

## <a name="outlining"></a>大綱

**啟用大綱模式**

當您在程式碼編輯器中開啟檔案時，可以使用大綱模式檢視文件。 如需詳細資訊，請參閱[大綱](../../ide/outlining.md)。 選取此選項後，在您開啟檔案時將會啟動大綱功能。

**顯示程序行分隔符號**

文字編輯器會指出程序的可見範圍。 會在專案的 *.vb* 原始程式檔中描繪一行，而這些原始程式檔是位於下表所列的位置：

|vb 原始程式檔中的位置|行位置的範例|
|---------------------------------|------------------------------|
|在區塊宣告建構關閉之後|-   在類別、結構、模組、介面和列舉的結尾處<br />-   在屬性、函式或子函式之後<br />-   不在屬性中的 get 與 set 子句之間|
|在一組的單一行建構之後|-   在重要的陳述式之後，類別檔中的型別定義之前<br />-   在類別中宣告的變數之後，任何程序之前|
|在單一行宣告 (非區塊層級宣告) 之後|-   接在重要的陳述式、繼承陳述式、變數宣告、事件宣告、委派宣告和 DLL 宣告陳述式之後|

## <a name="block-structure-guides"></a>區塊結構輔助線

選取時，編輯器中會出現對齊結構化程式碼區塊的垂直線，可讓您輕鬆地識別個別程式碼區塊。 例如，您會在 `Sub` 陳述式中的 `Sub` 與 `EndSub` 之間看到線條。

## <a name="editor-help"></a>編輯器說明

**程式碼美化排列 (重新格式化)** 文字編輯器會適當地重新格式化您的程式碼。 選取此選項後，程式碼編輯器將會：

-   將您的程式碼對齊正確的定位點位置

-   重新將關鍵字、變數和物件指定為正確的大小寫

-   將遺漏的 `Then` 新增至 `If...Then` 陳述式

-   將括弧新增至函式呼叫

-   將遺漏的結尾引號新增至字串

-   重新格式化指數標記法

-   重新格式化日期

**自動插入 End 建構**

在您輸入 (例如，程序宣告 `Sub Main` 的第一行 ) 並按 **Enter** 時，文字編輯器會新增對稱的 `End Sub` 行。 同樣地，如果新增 [For](/dotnet/visual-basic/language-reference/statements/for-next-statement) 迴圈，則文字編輯器會新增對稱的 `Next` 陳述式。 選取此選項後，程式碼編輯器會自動新增 End 建構。

**自動插入 Interface 及 MustOverride 成員**

當您認可 `Implements` 陳述式或類別的 `Inherits` 陳述式時，文字編輯器就會插入必須各自實作或覆寫之成員的原型。

**啟用錯誤修正建議**

文字編輯器可以提供一般錯誤的解決方案建議，並讓您選取要套用到程式碼的適當修正措施。

## <a name="see-also"></a>另請參閱

- [選項對話方塊、環境、一般](../../ide/reference/general-environment-options-dialog-box.md)
- [索引標籤、所有語言、文字編輯器、選項](../../ide/reference/options-text-editor-all-languages-tabs.md)
