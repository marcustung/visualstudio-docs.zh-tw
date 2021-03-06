---
title: 作法：使用分析工具命令列以檢測原生服務並收集詳細計時資料 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: dfe58b39-63f8-4a87-ab3a-2b5b14faa8d0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: b2be1ac0818f7efd31fb30981e50eff5e42df7af
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56634782"
---
# <a name="how-to-instrument-a-native-service-and-collect-detailed-timing-data-by-using-the-profiler-command-line"></a>HOW TO：使用分析工具命令列以檢測原生服務並收集詳細計時資料
本文描述如何使用 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 分析工具命令列工具來檢測原生 (C/C++) 服務，並收集詳細的計時資料。

> [!NOTE]
>  如果某項服務無法在電腦啟動後重新啟動 (這類服務只會在作業系統啟動時啟動)，則無法使用檢測方法來分析服務。
>
>  若要取得分析工具的路徑，請參閱[指定命令列工具的路徑](../profiling/specifying-the-path-to-profiling-tools-command-line-tools.md)。 在 64 位元電腦上，64 位元和 32 位元版本的工具都可以使用。 若要使用程式碼剖析工具命令列工具，必須將工具路徑加入至命令提示字元視窗的 PATH 環境變數，或將它加入至命令本身。

 若要使用檢測方法從原生服務收集詳細的計時資料，您可使用 [VSInstr.exe](../profiling/vsinstr.md) 工具產生已檢測的元件版本。 然後以檢測過的版本取代未經檢測的服務版本，確認服務設定為手動啟動。 然後啟動分析工具。

 啟動服務後，計時資料會自動收集到資料檔案。 程式碼剖析工作階段期間，您可以暫停和繼續資料收集。

 若要結束分析工作階段，請關閉服務，然後明確關閉分析工具。

## <a name="start-the-application-with-the-profiler"></a>使用分析工具啟動應用程式

#### <a name="to-start-profiling-a-native-service"></a>開始分析原生的服務

1. 開啟 [命令提示字元] 視窗。

2. 使用 [VSInstr] 工具產生服務二進位檔的已檢測版本。

3. 以檢測過的版本取代原始二進位檔。 在 Windows 服務控制管理員中，確定服務的啟動類型設定為 [手動]。

4. 啟動分析工具。 類型：

    **VSPerfCmd** [/start](../profiling/start.md) **:trace**  [/output](../profiling/output.md) **:** `OutputFile` [`Options`]

   - **/start:trace** 選項會將分析工具初始化。

   - **/output:**`OutputFile` 選項必須搭配 **/start** 使用。 `OutputFile` 指定分析資料 (.*vsp*) 檔案的名稱和位置。

     您可以使用下列任一選項搭配 **/start:trace** 選項。

   > [!NOTE]
   >  **/user** 和 **/crosssession** 選項通常是 ASP.NET 應用程式的必要選項。

   | 選項 | 說明 |
   | - | - |
   | [/user](../profiling/user-vsperfcmd.md) **:**[`Domain`**\\**]`UserName` | 指定擁有 ASP.NET 背景工作處理序之帳戶的網域和使用者名稱。 如果以登入的使用者之外的使用者身分執行處理序，就需要這個選項。 處理序擁有者會列在 [Windows 工作管理員] [處理序] 索引標籤上的 [使用者名稱] 資料行。 |
   | [/crosssession](../profiling/crosssession.md) | 在其他登入工作階段啟用處理序程式碼剖析。 如果 ASP.NET 應用程式是在不同的工作階段中執行，就需要這個選項。 工作階段識別碼會列在 [Windows 工作管理員] 之 [處理程序] 索引標籤上的 [工作階段識別碼] 資料行中。 **/crosssession** 可縮寫成 **/CS**。 |
   | [/waitstart](../profiling/waitstart.md)[**:**`Interval`] | 指定在分析工具傳回錯誤之前，等候它初始化的秒數。 如果未指定 `Interval`，分析工具會無限期等候。 根據預設，**/start** 會立即傳回。 |
   | [/globaloff](../profiling/globalon-and-globaloff.md) | 若要啟動暫停資料收集的程式碼剖析工具，請將 **/globaloff** 選項新增到 **/start** 命令列。 使用 **/globalon** 以繼續程式碼剖析。 |
   | [/counter](../profiling/counter.md) **:** `Config` | 從 Config 中指定的處理器效能計數器收集資訊。計數器資訊會新增至在每個分析事件收集的資料。 |
   | [/wincounter](../profiling/wincounter.md) **:** `WinCounterPath` | 指定程式碼剖析期間要收集的 Windows 效能計數器。 |
   | [/automark](../profiling/automark.md) **:** `Interval` | 只能搭配 **/wincounter** 使用。 指定 Windows 效能計數器收集事件間隔的毫秒數。 預設值為 500 毫秒。 |
   | [/events](../profiling/events-vsperfcmd.md) **:** `Config` | 指定程式碼剖析期間要收集的 Windows 事件追蹤 (ETW) 事件。 ETW 事件會收集至個別的 (.*etl*) 檔案。 |


5. 從服務控制管理員啟動服務。

## <a name="control-data-collection"></a>控制資料收集
 當服務執行時，您可以使用 *VSPerfCmd.exe* 選項開始和停止將資料寫入至分析工具資料檔案。 控制資料收集可讓您收集特定程式執行 (例如啟動或關閉服務) 的資料。

#### <a name="to-start-and-stop-data-collection"></a>開始和停止資料收集

-   下列成對的 **VSPerfCmd** 選項會開始和停止資料收集。 請在個別的命令列上指定各個選項。 您可以多次開始和停止資料收集。

    |選項|說明|
    |------------|-----------------|
    |[/globalon /globaloff](../profiling/globalon-and-globaloff.md)|開始 (**/globalon**) 或停止 (**/globaloff**) 所有處理序的資料收集。|
    |[/processon](../profiling/processon-and-processoff.md) **:** `PID` [/processoff](../profiling/processon-and-processoff.md) **:** `PID`|開始 (**/processon**) 或停止 (**/processoff**) 處理序 ID (`PID`) 指定的處理序資料收集。|
    |[/threadon](../profiling/threadon-and-threadoff.md) **:** `TID` [/threadoff](../profiling/threadon-and-threadoff.md) **:** `TID`|開始 (**/threadon**) 或停止 (**/threadoff**) 執行緒識別碼 (`TID`) 所指定執行緒的資料收集。|

## <a name="end-the-profiling-session"></a>結束程式碼剖析工作階段
 若要結束分析工作階段，請停止正在執行已檢測元件的服務，然後呼叫 **VSPerfCmd** [/shutdown](../profiling/shutdown.md) 選項以關閉分析工具，結束分析資料檔案。

#### <a name="to-end-a-profiling-session"></a>結束程式碼剖析工作階段

1.  從服務控制管理員停止服務。

2.  關閉分析工具。 類型：

     **VSPerfCmd /shutdown**

3.  以原始模組取代檢測過的模組。 如有必要，請重新設定服務的啟動類型。

## <a name="see-also"></a>另請參閱
- [分析服務](../profiling/command-line-profiling-of-services.md)
- [檢測方法資料檢視](../profiling/instrumentation-method-data-views.md)