---
title: HOW TO：建立分析工具呼叫追蹤報表 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- performance tools, viewing ETW data
- ETW [Visual Studio ALM], viewing data
ms.assetid: 7640520a-7d3c-456c-b184-872a5d2f82f3
caps.latest.revision: 24
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c92f5cd8f268b249e8f29ddd706860ff18b2f87c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60117820"
---
# <a name="how-to-create-a-profiling-tools-call-trace-report"></a>HOW TO：建立程式碼剖析工具呼叫追蹤報表
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 分析工具的「呼叫追蹤報表」會列出您應用程式函式每個進入點和結束點的計時資訊，以及您的函式對其他函式的每次呼叫。 只有使用檢測方法收集分析資料時，呼叫追蹤報表才能用於資料分析。  
  
> [!NOTE]
>  您無法在 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 中顯示呼叫追蹤報表。 您必須使用 **VSPerfReport** 命令列工具來產生逗號分隔值 (.csv) 或 Xml 檔案。 如需此工具的詳細資訊，請參閱 [VSPerfReport](../profiling/vsperfreport.md)。  
  
### <a name="to-create-a-call-trace-report"></a>建立呼叫追蹤報表  
  
1. 開啟 [命令提示字元] 視窗。  
  
2. 在命令提示字元中輸入下列命令：  
  
     *ToolsPath* **VSPerfReport** *VSPFile*  **/CallTrace [/Xml]**  
  
    |||  
    |-|-|  
    |*ToolsPath*|分析工具命令列工具的路徑。 如需詳細資訊，請參閱[指定命令列工具的路徑](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)。|  
    |*VSPFile*|分析資料檔 (.vsp 或 .vsps)。 可接受完整和部分路徑。|  
    |Xml|產生 XML 格式化的報表。|  
  
## <a name="see-also"></a>另請參閱  
 [如何：收集事件追蹤 Windows (ETW) 資料](../profiling/how-to-collect-event-tracing-for-windows-etw-data.md)   
 [程式碼剖析工具 API](../profiling/profiling-tools-apis.md)
