---
title: Office UI 自訂逐步解說
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- actions panes, walkthroughs
- smart documents, walkthroughs
- walkthroughs [Office development in Visual Studio], smart tags
- walkthroughs [Office development in Visual Studio], action panes
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 95561f1404da1efd71ff3418f9154392f393795c
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596590"
---
# <a name="office-ui-customization-walkthroughs"></a>Office UI 自訂逐步解說
  下列逐步解說示範使用文件層級自訂和 VSTO 增益集來自訂 Microsoft Office 應用程式使用者介面 (UI) 的方法。

## <a name="actions-pane-walkthroughs"></a>執行窗格逐步解說
- [逐步解說：從 [動作] 窗格中的文件中插入文字](../vsto/walkthrough-inserting-text-into-a-document-from-an-actions-pane.md)示範如何建立 Word 文件中的 [動作] 窗格中。 執行窗格包含會將使用者輸入傳送至文件的兩個控制項。

- [逐步解說：將資料繫結至 Word 執行窗格上的控制項](../vsto/walkthrough-binding-data-to-controls-on-a-word-actions-pane.md)示範如何在 Word 中的執行窗格上的控制項繫結至資料。 這些控制項會顯示 SQL Server 資料庫中資料表之間的主要/詳細資料關聯。

- [逐步解說：將資料繫結至 Excel 執行窗格上的控制項](../vsto/walkthrough-binding-data-to-controls-on-an-excel-actions-pane.md)說明如何將控制項繫結至資料來源，以便在 Excel 中的 [動作] 窗格。

## <a name="custom-task-pane-walkthroughs"></a>自訂工作窗格逐步解說
- [逐步解說：自動化運用自訂工作窗格應用程式](../vsto/walkthrough-automating-an-application-from-a-custom-task-pane.md)示範如何建立自訂工作窗格包含可自動化主應用程式，當使用者按一下控制項的控制項。

- [逐步解說：與功能區按鈕同步處理自訂工作窗格](../vsto/walkthrough-synchronizing-a-custom-task-pane-with-a-ribbon-button.md)示範如何建立自訂工作窗格的使用者可以隱藏或顯示按一下功能區上的切換按鈕。

- [逐步解說：在 Outlook 中顯示與電子郵件訊息的自訂工作窗格](../vsto/walkthrough-displaying-custom-task-panes-with-e-mail-messages-in-outlook.md)示範如何顯示自訂工作窗格與每個電子郵件訊息中所建立或開啟 Outlook 中的唯一執行個體。

## <a name="ribbon-walkthroughs"></a>功能區逐步解說
- [逐步解說：使用功能區設計工具建立自訂的索引標籤](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)示範如何使用功能區設計工具建立自訂功能區索引標籤。 索引標籤包含可用來隱藏或顯示執行窗格的按鈕。

- [逐步解說：更新在執行階段的功能區上的控制項](../vsto/walkthrough-updating-the-controls-on-a-ribbon-at-run-time.md)示範如何使用功能區載入至 Office 應用程式之後，更新功能區上的控制項的功能區物件模型。

- [逐步解說：使用功能區 XML 建立自訂的索引標籤](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)示範如何使用功能區 XML，而不是使用功能區設計工具建立自訂功能區索引標籤。

## <a name="controls-on-word-documents"></a>Word 文件上的控制項
- [逐步解說：將控制項加入文件中的 VSTO 增益集的執行階段中](../vsto/walkthrough-adding-controls-to-a-document-at-run-time-in-a-vsto-add-in.md)示範如何使用 VSTO 增益集，將控制項加入至文件。

- [逐步解說：變更文件格式使用 CheckBox 控制項](../vsto/walkthrough-changing-document-formatting-using-checkbox-controls.md)示範如何變更文件層級自訂中使用核取方塊中的 Word 文件的格式。

- [逐步解說：使用按鈕文件中的文字方塊中顯示的文字](../vsto/walkthrough-displaying-text-in-a-text-box-in-a-document-using-a-button.md)示範如何使用 Word 文件上的按鈕和文字方塊。

- [逐步解說：更新使用選項按鈕的文件中的圖表](../vsto/walkthrough-updating-a-chart-in-a-document-using-radio-buttons.md)示範如何使用文件層級自訂中的選項按鈕來變更圖表樣式中的 Word 文件。

## <a name="controls-on-excel-worksheets"></a>Excel 工作表的控制項
- [逐步解說：將控制項加入工作表，在 VSTO 增益集專案中的執行階段](../vsto/walkthrough-adding-controls-to-a-worksheet-at-run-time-in-vsto-add-in-project.md)示範如何使用 VSTO 增益集，將控制項加入至工作表。

- [逐步解說：變更工作表的格式使用 CheckBox 控制項](../vsto/walkthrough-changing-worksheet-formatting-using-checkbox-controls.md)示範基本概念的 Excel 工作表上使用核取方塊變更格式。

- [逐步解說：使用按鈕在工作表中的文字方塊中顯示文字](../vsto/walkthrough-displaying-text-in-a-text-box-in-a-worksheet-using-a-button.md)示範 Excel 工作表上使用按鈕和文字方塊的基本概念。

- [逐步解說：更新使用選項按鈕在工作表中的圖表](../vsto/walkthrough-updating-a-chart-in-a-worksheet-using-radio-buttons.md)顯示 Excel 工作表上使用選項按鈕變更圖表樣式的基本概念。

## <a name="see-also"></a>另請參閱
- [使用 Word 的逐步解說](../vsto/walkthroughs-using-word.md)
- [使用 Excel 的逐步解說](../vsto/walkthroughs-using-excel.md)
- [Office 方案逐步解說中的資料](../vsto/data-in-office-solutions-walkthroughs.md)
- [安全性和部署的逐步解說](../vsto/security-and-deployment-walkthroughs.md)
- [開始使用&#40;在 Visual Studio 中的 Office 程式開發&#41;](../vsto/getting-started-office-development-in-visual-studio.md)
- [在 Office 程式設計中的一般工作](../vsto/common-tasks-in-office-programming.md)
- [設計和建立 Office 方案](../vsto/designing-and-creating-office-solutions.md)
