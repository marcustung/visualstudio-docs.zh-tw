---
title: 逐步解說：XSLT Profiler |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 87387c9a-2e89-4801-ad51-83740cd6ea25
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: db9937a09c8260bd595b6c0311501920bf960aaf
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60100309"
---
# <a name="walkthrough-xslt-profiler"></a>逐步解說：XSLT 分析工具
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XSLT 分析工具可建立詳細的 XSLT 效能報告，協助您測量、評估並解決 XSLT 程式碼中與效能相關的問題。 XSLT 分析工具包含 XSL 和 XSLT 樣式表最佳化的實用提示。 就需要最大效能的 XSLT 應用程式而言，此工具是非常基本的。  
  
## <a name="prerequisites"></a>必要條件  
 下列逐步解說中的程序需要 Visual Studio 2010 和 .NET Framework 4.0 版。 XSLT 分析工具僅適用於搭配使用已安裝程式碼剖析工具的 Microsoft Visual Studio Team System。  
  
### <a name="create-the-performance-report"></a>建立效能報告  
  
1. 在 Visual Studio 中開啟 XSLT 文件。  
  
2. 按一下 **分析 XSLT** XML 功能表中可用的選項。  
  
3. 提供輸入 XML 文件。 如果尚未開啟任何 XML 文件，系統會提示您開啟檔案。  
  
4. 開始分析時會出現一個進度列，顯示編輯器中的進度。  
  
5. XSLT 輸出會顯示在輸出窗格中。  
  
6. 效能工作階段結束後，請查看效能報告。 儲存在效能報告中的資料可讓您檢視並分析 XSLT 效能。  
  
### <a name="get-all-the-available-views"></a>取得所有可用的檢視  
  
1. 按一下 **目前檢視**下拉式清單，以取得所有可用的檢視。  
  
2. 選取 **摘要檢視**選項**目前檢視**下拉式清單。 根據預設，效能報表會顯示在**摘要檢視**。 這個檢視是透過 XSLT 文件判斷效能問題的起點。 **摘要檢視**列出下列資料點：  
  
    - 最常呼叫的函式  
  
    - 含有最多個別工作的函式  
  
    - 執行時間最長的函式  
  
3. 根據預設，每個資料點中有三個資料行：函式的名稱、呼叫的次數 (絕對值)，以及具名函式佔總函式呼叫次數的百分比值。 從每個資料點**摘要檢視**，您可以巡覽至更詳細的檢視，以滑鼠右鍵按一下函式的資料點。  
  
4. 選取 **函式檢視**選項**目前檢視**下拉式清單。 **函式檢視**列出分析期間呼叫的函式。 您可以按一下資料行名稱來排序資料。 預設顯示的資料行為：  
  
    - **函式名稱**  
  
    - **功能內含耗用 (Elapsed Inclusive) 時間**  
  
    - **功能專屬耗用 (Elapsed Exclusive) 時間**  
  
    - **應用程式內含 (Application Inclusive) 時間**  
  
    - **應用程式專屬 (Application Exclusive) 時間**  
  
    - **呼叫次數**  
  
5. 所有時間資料行均會同時顯示絕對值和百分比。 詞彙**獨佔**專用於其他函式所花費的時間執行期間執行此函式呼叫的函式是指的總時間。  
  
6. 詞彙**Inclusive**呼叫它是否屬於這些呼叫的函式呼叫其他函式是指函式花費在執行，包括之所有函式的執行時間的總時間。  
  
### <a name="select-callercallee-view"></a>選取呼叫端/被呼叫端檢視  
  
1. 選取 **呼叫端/被呼叫端**檢視中**目前檢視**下拉式清單。  
  
2. **呼叫端/被呼叫端**檢視有下列三個不同的部分：  
  
    - **函式呼叫**:呼叫特定函式的所有函式會列在檢視的上半部。  
  
    - **目前的函式**:呼叫特定函式會列在檢視的中間部分。  
  
    - **所呼叫的函式**:所有的特定函式所呼叫的函式會列在檢視的下半部。  
  
3. 如果名為 `SyncToNavigator` 的函式出現在檢視的中間部分，則所有呼叫 `SyncToNavigator` 函式的函式都會出現在檢視的上半部，而所有被 `SyncToNavigator` 呼叫的函式會出現在檢視的下半部。  
  
4. 您可以按兩下檢視中其他兩個部分列出的任何一個函式，以變更檢視中間部分的函式。 然後檢視會自動更新以反映變更。  
  
5. 您也可以按一下資料行名稱以排序資料。  
  
### <a name="select-calltree-view"></a>選取呼叫樹狀圖檢視  
  
1. 選取 **呼叫樹狀圖檢視**中**目前檢視**下拉式清單。 此檢閱是程式執行的樹狀檢閱。  
  
2. **呼叫樹狀圖檢視**顯示處理序名稱為樹狀的根目錄。 函式即為樹狀的節點。 此檢視可讓您深入查看特定的呼叫追蹤，並且分析哪些追蹤會對效能造成最大的影響。 檢視是類似**呼叫堆疊檢視**偵錯期間可用。 中的資料行除了**函式檢視**，請在**呼叫樹狀圖檢視**，沒有額外的資料行，以顯示**模組名稱**。  
  
3. 選取 **標記**中**目前檢視**下拉式清單。  
  
4. 使用 SLT 分析工具時，資料集合資料流中會出現標記及相關的註解。 標記放置在具有計數器的程式碼中。 當您指示 XSLT 分析工具收集 XSLT 效能計數器時，該工具就會在每次執行其中一個標記時收集計數器。 資料會顯示在一個資料表，其中包含**標記 ID**，**標示名稱**(**啟動程式**，**結束程式**)，而**時間戳記**。 標記 不會彙總及顯示在 依時間先後順序**標記 檢視**的效能報告。  
  
### <a name="select-modules-in-the-current-view"></a>在目前的檢視中選取模組  
  
1. 選取 **模組**中**目前檢視**下拉式清單。  
  
2. 模組檢視是彙總為模組層級之所有函式的一般清單。 請展開或摺疊模組名稱來顯示或關閉模組效能資料的檢視。 您可以按一下資料行名稱來排序資料。 根據預設中,，有絕對值和百分比數字，如**功能內含耗用時間**，**功能專屬耗用時間**，**應用程式內含時間**， **應用程式專屬時間**，並**的呼叫數**。  
  
3. 選取 **程序**中**目前檢視**下拉式清單。  
  
4. 處理序檢視會顯示包含的資料表**處理序識別碼**，**處理序名稱**，**開始時間**，而**結束時間**。 按一下資料行名稱即可排序資料。  
  
## <a name="see-also"></a>另請參閱  
 [逐步解說：使用 XSLT 階層](../xml-tools/walkthrough-using-xslt-hierarchy.md)
