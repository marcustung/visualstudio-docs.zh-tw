---
title: 收集階層互動資料 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.tierinteraction
helpviewer_keywords:
- Profiling Tools,ADO.NET profiling
- tier interaction profiling method
- Profiling Tools,tier-interaction method
- ADO.NET performance profiling
ms.assetid: 47a944c2-3098-497c-8fc7-e1f43d750bbc
caps.latest.revision: 18
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a20266c870316be9b6be67e661d13eb4e6fdbaee
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60047221"
---
# <a name="collecting-tier-interaction-data"></a>收集階層互動資料
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

階層互動分析提供透過 ADO.NET 服務與資料庫通訊之多介層應用程式函式執行時間的其他資訊。 只針對同步函式呼叫收集資料。  
  
 **Visual Studio 版本**  
  
 您可以使用 Visual Studio Ultimate、Visual Studio Premium 或 Visual Studio Professional 收集階層互動分析資料。 不過，只能在 VS Ultimate 和 VS Premium 檢視階層互動分析資料。  
  
 **Windows 8 和 Windows Server 2012**  
  
 若要在 Windows 8 傳統型應用程式和 Windows Server 2012 應用程式上收集階層互動資料，您必須使用檢測方法。 您無法收集 Windows 市集應用程式的階層互動資料。 請參閱 [Windows 8 和 Windows Server 2012 應用程式的效能工具](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md)。 其他支援的 Windows 版本上的所有程式碼剖析方法都可以包含階層互動資料。  
  
 **效能精靈**  
  
 因為效能精靈中有錯誤 (bug)，所以您必須從 [效能總管] 將階層互動資料收集選項加入分析執行。 您也必須將專案、可執行檔或網站加入 [效能總管] 的 [目標] 節點。  
  
### <a name="to-add-tier-interaction-data-to-a-profiling-run-by-using-the-performance-session-property-pages"></a>使用效能工作階段屬性頁將階層互動資料加入分析執行  
  
1. 在 [效能總管] 中，從操作功能表選擇 [屬性]。  
  
2. 選取 [階層互動] 頁面，然後按一下 [啟用階層互動分析] 核取方塊。  
  
3. 在 [效能總管] 中，選取 [目標] 節點，然後指定您想要分析的專案、可執行檔或網站。  
  
## <a name="see-also"></a>請參閱  
 [階層互動檢視](../profiling/tier-interactions-view.md)
