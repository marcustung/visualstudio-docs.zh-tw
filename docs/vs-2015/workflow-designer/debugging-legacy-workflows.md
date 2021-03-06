---
title: 偵錯舊版工作流程 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- workflows, debugging
- debugging, workflows
- debugging workflows
ms.assetid: e6097b47-760a-4b30-a92c-ae70cdbda49f
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b98c520dc96b6f3c6467bbcaf8e48d9cff8791d2
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60048732"
---
# <a name="debugging-legacy-workflows"></a>偵錯舊版工作流程
如果您在 [!INCLUDE[wfd1](../includes/wfd1-md.md)] 中使用舊版 [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] 來建置以 .NET Framework 3.0 或 3.5 為目標的 [!INCLUDE[wf](../includes/wf-md.md)] 應用程式，您可以像任何其他程式一樣，藉由設定中斷點、附加至處理序，並檢查執行緒和呼叫堆疊，來偵錯您的工作流程。 您也可以選擇遠端偵錯。  
  
> [!NOTE]
>  如果您的電腦上曾經安裝及解除安裝多個版本的 Visual Studio，WF3 偵錯會因為下列兩種可能性之一而失敗：  
> 
> - 未達到您的中斷點。  
>   - 畫面顯示下列訊息：  
> 
>   **無法開始偵錯 web 伺服器上。未正確安裝偵錯工具。無法偵錯所要求的程式碼型別。執行安裝程式來安裝或修復偵錯工具。**  
> 
>   如果在偵錯 .NET Framework 3.0 或 3.5 工作流程時，發生上述任一案例，則執行 Visual Studio 安裝的修復。  
  
 [!INCLUDE[wf2](../includes/wf2-md.md)] 會與以下標準 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 偵錯視窗整合：  
  
- **中斷點**:運作如預期般運作，但您指定的函式名稱的活動。  
  
- **呼叫堆疊**:修改，以提供已在工作流程執行個體中執行之活動的概述。 中的項目**呼叫堆疊**視窗是深度優先搜尋執行中活動。 您可以按兩下項目，將焦點放在選取的活動上。  
  
- **執行緒**:提供正在偵錯工作流程執行個體的執行個體識別碼。  
  
  Visual Studio for Windows Workflow Foundation 不支援以下偵錯功能：  
  
- 設計介面上的條件中斷點。  
  
- 快速監看式。  
  
- 設定 Next 陳述式。  
  
- 執行至游標處。  
  
- 編輯後繼續。  
  
- Just-In-Time 偵錯。  
  
- 混合模式偵錯。  
  
## <a name="in-this-section"></a>本節內容  
 [叫用 Visual Studio Debugger for Windows Workflow Foundation (舊版)](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [停用 Visual Studio Debugger for Windows Workflow Foundation (舊版)](../workflow-designer/disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md)  
  
 [如何：對 ASP.NET 工作流程進行偵錯 (舊版)](../workflow-designer/how-to-debug-aspnet-based-workflows-legacy.md)  
  
 [如何：在工作流程中設定中斷點 (舊版)](../workflow-designer/how-to-set-breakpoints-in-workflows-legacy.md)  
  
 [從遠端電腦偵錯工作流程 (舊版)](../workflow-designer/debugging-workflows-from-a-remote-computer-legacy.md)  
  
 [偵錯逐步執行選項 (舊版)](../workflow-designer/debug-stepping-options-legacy.md)  
  
 [如何：變更偵錯逐步執行選項 (舊版)](../workflow-designer/how-to-change-the-debug-stepping-option-legacy.md)