---
title: 並行視覺化檢視 | Microsoft Docs
ms.date: 07/11/2017
ms.topic: conceptual
f1_keywords:
- vs.cv.performance.viewnavigation
- vs.cv.overview
- vs.cv.performance.gettingstarted
- vs.cv.gettingstarted
helpviewer_keywords:
- Concurrency Visualizer, Concurrency Visualizer
ms.assetid: ae5879a0-1e1a-455a-ba72-148e57f59289
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f2ed469256036351fb0f7dd3991e0eee1d8c54cb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641399"
---
# <a name="concurrency-visualizer"></a>並行視覺化檢視
> [!NOTE]
>  並行視覺化檢視是 Visual Studio 的選擇性擴充功能。 從下列連結下載並行視覺化檢視和並行視覺化檢視收集工具：
>
> - 下載 [Visual Studio 2017 並行視覺化檢視](https://marketplace.visualstudio.com/items?itemName=VisualStudioProductTeam.ConcurrencyVisualizer2017#overview)延伸模組。
> - 下載[適用於 Visual Studio 2015 的並行視覺化檢視](https://marketplace.visualstudio.com/items?itemName=Diagnostics.ConcurrencyVisualizerforVisualStudio2015)延伸模組。
>   -   下載              [適用於 Visual Studio 2015 的並行視覺化檢視收集工具](http://www.microsoft.com/download/details.aspx?id=49103)。
>
>   [並行視覺化檢視命令列公用程式 (CVCollectionCmd.exe)](../profiling/concurrency-visualizer-command-line-utility-cvcollectioncmd.md) 讓您可以從命令列收集追蹤，在 Visual Studio 2015 的並行視覺化檢視中加以檢視。 此工具可以用於未安裝 Visual Studio 的電腦。

 透過使用並行視覺化檢視來查看多執行緒 App 的執行情況。 [並行視覺化檢視] 中的這些檢視會提供圖形、表格和文字資料，顯示程式和整體系統中執行緒之間的暫時關聯性。 您可以使用 [並行視覺化檢視] 找出效能瓶頸、CPU 使用率不彰、執行緒爭用、跨核心執行緒移轉、同步處理延遲、DirectX 活動、I/O 重疊區域以及其他資訊。 這些檢視透過將其圖形輸出連結至呼叫堆疊和原始程式碼的方式，來提供可採取動作的資料。

> [!NOTE]
>  [並行視覺化檢視] 不支援 Web 專案。

 [並行視覺化檢視] 的運作是依賴 [Windows 事件追蹤](http://go.microsoft.com/fwlink/?LinkId=234579) 功能。

## <a name="related-topics"></a>相關主題

|標題|說明|
|-----------|-----------------|
|[使用率檢視](../profiling/utilization-view.md)|說明如何跨所有處理器檢視和分析系統活動。|
|[執行緒檢視](../profiling/threads-view-parallel-performance.md)|說明如何分析程式中執行緒之間的互動。|
|[核心檢視](../profiling/cores-view.md)|說明如何分析跨核心的執行緒移轉。|
|[行為錯誤之多執行緒應用程式的常見模式](../profiling/common-patterns-for-poorly-behaved-multithreaded-applications.md)|描述常見的幾種模式，並示範它們是如何出現在 [並行視覺化檢視] 中。|
|[Visual Studio 部落格中的平行開發](http://go.microsoft.com/fwlink/?LinkId=235385)|提供 [並行視覺化檢視] 的秘訣和最佳作法。|
|[效能報告檢視](../profiling/performance-report-views.md)|提供 Visual Studio 程式碼剖析工具的報表和檢視的參考資訊。|
|[並行視覺化檢視 SDK](../profiling/concurrency-visualizer-sdk.md)|描述如何檢測您的原始程式碼，以便在 [並行視覺化檢視] 中顯示其他資訊。|
|[並行視覺化檢視命令列公用程式 (CVCollectionCmd)](../profiling/concurrency-visualizer-command-line-utility-cvcollectioncmd.md)|描述如何使用 [並行視覺化檢視] 命令列公用程式 (CVCollectionCmd.exe) 來收集及處理沒有安裝 Visual Studio 的電腦上的追蹤資料。|

## <a name="see-also"></a>另請參閱
- [Visual Studio 中的分析](../profiling/index.md)
- [初步認識分析工具](../profiling/profiling-feature-tour.md)
