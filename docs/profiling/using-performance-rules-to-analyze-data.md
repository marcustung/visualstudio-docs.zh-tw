---
title: 使用效能規則分析資料 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1deed23e-b31b-4714-982f-08ceebfc3096
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e0e69de397f9c8f4160d81047f086a6db60741e8
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641646"
---
# <a name="use-performance-rules-to-analyze-data"></a>使用效能規則分析資料
[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 程式碼剖析工具的效能警告指出，正在進行程式碼剖析的應用程式中發生問題，可能會降低程式執行速度。 警告也可能表示您可能需要變更收集方法，以收集更有用的資料。 效能警告會在程式碼剖析工作階段中自動產生。 在 Visual Studio 中開啟程式碼剖析資料檔案時，警告會出現在 [錯誤清單] 視窗中。 您可以在 [錯誤清單] 視窗中找到問題的原始程式碼，並可以顯示有關錯誤的詳細資訊，例如有關如何解決問題的資訊。 您也可以將您不想要的警告停用。

> [!NOTE]
>  分析工具效能警告是由程式執行的動態分析所產生，並且和程式碼分析警告無關。 程式碼分析也可以根據原始程式碼的靜態分析，來產生 Managed 程式碼的效能警告。 如需詳細資訊，請參閱[分析受控程式碼品質](/visualstudio/code-quality/code-analysis-for-managed-code-overview)和[效能警告](../code-quality/performance-warnings.md)。

## <a name="in-this-section"></a>本節內容
- [如何：檢視效能警告](../profiling/how-to-view-performance-warnings.md)

 提供如何開啟 [錯誤清單] 視窗以檢視分析工具效能警告的相關資訊。

- [如何：設定效能規則](../profiling/how-to-configure-performance-rules.md)

 提供如何將個別效能警告開啟或關閉的相關資訊。

- [效能規則參考](../profiling/performance-rules-reference.md)

 提供有關分析工具效能警告的詳細資訊