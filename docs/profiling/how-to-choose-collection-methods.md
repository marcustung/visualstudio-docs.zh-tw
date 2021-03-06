---
title: 作法：選擇收集方法 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- performance tools, choosing collection method
- profiling tools, choosing collection method
- performance collection methods
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 344af8760dad3c66c32590b7d2d665bef833e583
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56638513"
---
# <a name="how-to-choose-collection-methods"></a>HOW TO：選擇收集方法

Visual Studio 分析工具支援三種效能資料收集方法︰取樣、檢測和並行。 您也可以使用取樣或檢測方法來收集 .NET 記憶體配置和存留期資料。

您可以使用效能工作階段 **Method** 屬性來指定最適合您的應用程式的收集方法。 您可以從 [效能精靈]、[效能總管] 或效能工作階段中的屬性頁面設定收集方法。 如果您使用命令列工具，請參閱[從命令列進行程式碼剖析](../profiling/using-the-profiling-tools-from-the-command-line.md)以了解詳細資訊。

## <a name="performance-wizard"></a>效能精靈

### <a name="to-select-a-collection-method-using-the-performance-wizard"></a>使用 [效能精靈] 選取收集方法

- 在精靈的第一個頁面上，選取下列其中一個選項︰

| 選項 | 說明 |
|----------------------------| - |
| **CPU 取樣** | 收集對初始分析和 CPU 使用率問題分析有用的應用程式統計資料。 |
| **檢測** | 收集對重點分析和輸入/輸出效能問題分析有用的詳細計時資料。 |
| **.NET 記憶體配置** | 使用取樣分析方法收集 [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] 記憶體配置資料。 |
| **並行** | 收集數值資源爭用資料。 |

## <a name="performance-explorer"></a>效能總管

### <a name="to-select-a-collection-method-using-performance-explorer"></a>使用 [效能總管] 選取收集方法

1. 在 [效能總管] 工具列上，按一下 [方法] 下拉式清單旁的箭號。

2. 按一下您偏好的收集方法。

## <a name="performance-session-property-pages"></a>效能工作階段屬性頁

### <a name="to-select-the-sampling-or-instrumentation-method-using-performance-session-properties"></a>使用效能工作階段屬性選取取樣或檢測方法

1. 在 [效能總管] 中，選取效能工作階段。

     效能工作階段檔案名稱的副檔名為 .*psess*。

2. 以滑鼠右鍵按一下效能工作階段，然後按一下 [屬性]。

3. 在 [屬性頁] 中，按一下 [一般] 頁面。

4. 按一下您偏好的收集方法。

    - 如需收集取樣資料時可用的其他選項的詳細資訊，請參閱[使用取樣收集效能統計資料](../profiling/collecting-performance-statistics-by-using-sampling.md)。

    - 如需收集取樣資料時可用的其他選項的詳細資訊，請參閱[使用檢測收集計時詳細資料](../profiling/collecting-detailed-timing-data-by-using-instrumentation.md)。

### <a name="to-select-net-memory-data-collection-by-using-performance-session-properties"></a>使用效能工作階段屬性選取 .NET 記憶體資料收集

1. 在 [效能總管] 中，選取效能工作階段。

     效能工作階段檔案名稱的副檔名為 .psess。

2. 以滑鼠右鍵按一下效能工作階段，然後按一下 [屬性]。

3. 在 [屬性頁] 中，按一下 [一般] 頁面。

4. 按一下 [取樣] 或 [檢測]。

5. 按一下 [收集 .NET 物件配置資訊] 以收集 [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] 物件配置的大小和數目。

6. (選擇性) 按一下 [同時收集 .NET 物件存留期的資訊]，以收集回收物件記憶體的記憶體回收層代相關資料。

     如需收集 .NET 記憶體資料時可用之其他選項的詳細資訊，請參閱[收集 .NET 記憶體配置和存留期資料](../profiling/collecting-dotnet-memory-allocation-and-lifetime-data.md)。

### <a name="to-select-concurrency-data-collection-by-using-performance-session-properties"></a>使用效能工作階段屬性選取並行資料收集

1. 在 [效能總管] 中，以滑鼠右鍵按一下效能工作階段，然後按一下 [屬性] 。

2. 在 [屬性頁] 中，按一下 [一般] 頁面。

3. 按一下 [並行]。

## <a name="see-also"></a>另請參閱

[設定效能工作階段](../profiling/configuring-performance-sessions.md)
[了解取樣資料值](../profiling/understanding-sampling-data-values.md)
[效能工作階段屬性](../profiling/performance-session-properties.md)