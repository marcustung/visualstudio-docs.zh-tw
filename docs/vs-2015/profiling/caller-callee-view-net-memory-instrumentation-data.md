---
title: 呼叫端-被呼叫端檢視 - .NET 記憶體檢測資料 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- Caller/Callee view
ms.assetid: da624c06-8741-4afb-aad1-f8c0002f3de2
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2cd30b9dcc72ba2afd97577f69ac059a2e8a1d32
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47498528"
---
# <a name="callercallee-view---net-memory-instrumentation-data"></a>呼叫端/被呼叫端檢視 - .NET 記憶體檢測資料
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主題的最新的版本可從[呼叫端-被呼叫端檢視-.NET 記憶體檢測資料](https://docs.microsoft.com/visualstudio/profiling/caller-callee-view-net-memory-instrumentation-data)。  
  
使用檢測方法收集之 .NET 記憶體分析資料的 [呼叫端/被呼叫端] 檢視會顯示所選取函式及其父函式和子函式的配置和計時資料。 [呼叫端/被呼叫端] 檢視包含三個方格。  
  
 **目前的函式**會顯示在中間方格中，顯示所選取函式的記憶體分析資訊。 這些值包括對函式的所有取樣呼叫。  
  
 **呼叫目前函式的函式**會顯示在上方方格中，顯示所選取 (目前) 函式 (從呼叫端 (父) 函式的呼叫所產生) 的值數量。  
  
 **目前的函式所呼叫的函式**會顯示在下方方格中，顯示所選取函式之被呼叫端 (子) 函式 (由目前函式呼叫) 的記憶體分析資料。  
  
 按兩下呼叫端或被呼叫端函式資料列，讓該資料列變成目前的函式。  
  
## <a name="general"></a>一般  
  
|資料行|描述|  
|------------|-----------------|  
|**函式名稱**|函式的名稱。|  
|**函式位址**|函式的位址。|  
|**函式行號**|原始程式檔中這個函式的開頭行號。|  
|**呼叫次數**|呼叫此函式的總次數。|  
|**原始程式檔**|含有這個函式定義的原始程式檔。|  
|**模組名稱**|包含該函式的模組名稱。|  
|**模組路徑**|包含該函式的模組路徑。|  
|**處理序 ID**|分析執行的處理序 ID。|  
|**處理序名稱**|指派給處理序的名稱。|  
|**時間專有探查額外負荷**|檢測對此函式造成的時間額外負荷。 已經從所有專有時間減去探查額外負荷。|  
|**時間內含探查額外負荷**|檢測對此函式及其子函式造成的時間額外負荷。 已經從所有內含時間減去探查額外負荷。|  
|**Type**|函式的內容︰<br /><br /> **0** - 目前的函式<br /><br /> **1** - 呼叫目前函式的函式<br /><br /> **2** - 目前的函式所呼叫的函式<br /><br /> 只在[VSPerfReport](../profiling/vsperfreport.md) 命令列的報表中。|  
|**根函式名稱**|目前函式的名稱。 只存在於 [VSPerfReport](../profiling/vsperfreport.md) 命令列報表中。|  
  
## <a name="net-memory-allocation-values"></a>.NET 記憶體配置值  
  
|資料行|描述|  
|------------|-----------------|  
|**專有配置**|-  若為目前的函式，這是當函式執行函式主體中的程式碼時 (即函式位於呼叫堆疊的最上方) 所建立的物件數目。 這個數目不包含由此函式呼叫之函式建立的物件。<br />- 若為呼叫端函式，這是目前函式 (從此呼叫端函式的呼叫所產生) 的專有配置數目。<br />- 若為被呼叫端函式，這是此函式之執行個體 (由目前函式呼叫) 所建立的物件數目。 這個數目不包含被呼叫端函式呼叫之函式建立的物件。|  
|**專有配置 %**|在分析執行中建立的所有物件中，屬於此函式之專有配置的百分比。|  
|**內含配置**|- 若為目前的函式，這是函式在分析執行中所配置的物件數目。 這個數目包含由函式呼叫之被呼叫端中建立的物件。<br />- 若為呼叫端函式，這是目前函式 (從此呼叫端函式的呼叫所產生) 的內含配置數目。<br />- 若為被呼叫端函式，這是此函式之執行個體 (從目前函式的呼叫所產生) 所配置的物件數目。 這個數目包含由此被呼叫端函式所呼叫之函式所做的配置。|  
|**內含配置 %**|在分析執行中建立的所有物件中，屬於此函式之內含配置的百分比。|  
|**專有位元組**|- 若為目前的函式，這是函式在分析執行中所配置的記憶體位元組數目。 這個數目不包含由函式呼叫之被呼叫端函式中所配置的記憶體。<br />- 若為呼叫端函式，這是目前函式 (由此呼叫端函式呼叫所產生) 的專屬位元組數目。<br />- 若為被呼叫端函式，這是此函式之執行個體 (從目前函式的呼叫所產生) 所配置的位元組數目。 這個數目不包含由被呼叫端函式呼叫之函式所配置的位元組。|  
|**專有位元組 %**|在分析執行中配置的所有記憶體位元組中，屬於此函式之專有配置的百分比。|  
|**內含位元組**|- 若為目前的函式，這是函式在分析執行中所配置的記憶體位元組數目。 這個數目包含由函式呼叫之被呼叫端函式中所配置的記憶體。<br />- 若為呼叫端函式，這是目前函式之執行個體 (從此呼叫端函式的呼叫所產生) 的內含位元組數目。<br />- 若為被呼叫端函式，這是此函式之執行個體 (從目前函式的呼叫所產生) 所配置的位元組數目。 這個數目包含由此被呼叫端函式呼叫之函式所配置的位元組。|  
|**內含位元組 %**|在分析執行中配置的所有記憶體位元組中，屬於此函式之內含配置的百分比。|  
  
## <a name="elapsed-inclusive-values"></a>功能內含耗用值  
 功能內含耗用值表示函式在呼叫堆疊上的時間。 該時間包含在子函式中及呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。  
  
|資料行|描述|  
|------------|-----------------|  
|**功能內含耗用 (Elapsed Inclusive) 時間**|-  若為目前的函式，這是在函式中花費的時間。 該值包含在子函式中及呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。<br />-  若為呼叫端函式，這是目前函式 (從此呼叫端函式的呼叫所產生) 的功能內含耗用 (Elapsed Inclusive) 時間量。<br />- 若為被呼叫端函式，這是在此函式 (從目前函式的呼叫所產生) 所花費的時間。 該值包含在子函式中及呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。|  
|**功能內含耗用 (Elapsed Inclusive) 時間 %**|在分析執行的總功能內含耗用時間中，花費在此內容中此函式之功能內含耗用時間的百分比。|  
|**平均功能內含耗用 (Elapsed Inclusive) 時間**|在此內容中呼叫此函式的平均功能內含耗用 (Elapsed Inclusive) 時間。|  
|**最大功能內含耗用 (Elapsed Inclusive) 時間**|在此內容中呼叫此函式的最大功能內含耗用 (Elapsed Inclusive) 時間。|  
|**最小功能內含耗用 (Elapsed Inclusive) 時間**|在此內容中呼叫此函式的最小功能內含耗用 (Elapsed Inclusive) 時間。|  
  
## <a name="elapsed-exclusive-values"></a>功能專屬耗用值  
 功能專屬耗用值表示函式直接在呼叫堆疊最上方執行的時間。 該時間包含呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業，但不包含在子函式中花費的時間。  
  
|資料行|描述|  
|------------|-----------------|  
|**功能專屬耗用 (Elapsed Exclusive) 時間**|-  若為目前的函式，這是執行函式主體所花費的時間。 該值排除在子函式中所花費的時間，但包含呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。<br />-  若為呼叫端函式，這是目前函式 (從此呼叫端函式的呼叫所產生) 的功能專屬耗用 (Elapsed Exclusive) 時間量。<br />- 若為被呼叫端函式，這是在此函式 (從目前函式的呼叫所產生) 所花費的時間。 該值排除在被呼叫端之子函式中所花費的時間，但是包含呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。|  
|**功能專屬耗用 (Elapsed Exclusive) 時間 %**|在分析執行的總功能專屬耗用時間中，花費在此內容中此函式之總功能專屬耗用時間的百分比。|  
|**平均功能專屬耗用 (Elapsed Exclusive) 時間**|在此內容中呼叫此函式的平均功能專屬耗用 (Elapsed Exclusive) 時間。|  
|**最大功能專屬耗用 (Elapsed Exclusive) 時間**|在此內容中呼叫此函式的最大功能專屬耗用 (Elapsed Exclusive) 時間。|  
|**最小功能專屬耗用 (Elapsed Exclusive) 時間**|在此內容中呼叫此函式的最小功能專屬耗用 (Elapsed Exclusive) 時間。|  
  
## <a name="application-inclusive-values"></a>應用程式內含值  
 應用程式內含值表示函數在呼叫堆疊上的時間。 該時間不包含呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業，但包含在子函式中花費的時間。  
  
|資料行|描述|  
|------------|-----------------|  
|**應用程式內含 (Application Inclusive) 時間**|-  若為目前的函式，這是在函式及其子函式中花費的時間。 該值排除呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。<br />-  若為呼叫端函式，這是目前函式 (從此呼叫端函式的呼叫所產生) 的應用程式內含時間量。<br />- 若為被呼叫端函式，這是在此函式及其子函式 (從目前函式的呼叫所產生) 所花費的時間。 該值不包含呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。|  
|**應用程式內含 (Application Inclusive) 時間 %**|在分析執行的總功能內含耗用時間中，花費在此內容中此函式之總應用程式內含時間的百分比。|  
|**平均應用程式內含 (Application Inclusive) 時間**|在此內容中呼叫此函式的平均應用程式內含 (Application Inclusive) 時間。|  
|**最大應用程式內含 (Application Inclusive) 時間**|在此內容中呼叫此函式的最大應用程式內含 (Application Inclusive) 時間。|  
|**最小應用程式內含 (Application Inclusive) 時間**|在此內容中呼叫此函式的最小應用程式內含 (Application Inclusive) 時間。|  
  
## <a name="application-exclusive-values"></a>應用程式專屬值  
 應用程式專屬值表示在函式中花費的時間，排除在子函式中花費的時間。 所表示的時間也排除呼叫作業系統所花費的時間，例如內容切換和輸入/輸出作業。  
  
|資料行|描述|  
|------------|-----------------|  
|**應用程式專屬 (Application Exclusive) 時間**|-  若為目前的函式，這是執行函式主體所花費的時間。 這不包含在子函式中花費的時間，也不包含呼叫作業系統的時間，例如內容切換和輸入/輸出作業。<br />-  若為呼叫端函式，這是目前函式 (從此呼叫端函式的呼叫所產生) 的應用程式專屬時間量。<br />- 若為被呼叫端函式，這是在此函式 (從目前函式的呼叫所產生) 所花費的時間。 這不包含在被呼叫端函式之子函式中花費的時間，也不包含呼叫作業系統的時間，例如內容切換和輸入/輸出作業。|  
|**應用程式專屬 (Application Exclusive) 時間 %**|在分析執行的總功能專屬耗用時間中，花費在此內容中此函式之總應用程式專屬時間的百分比。|  
|**平均應用程式專屬 (Application Exclusive) 時間**|在此內容中呼叫此函式的平均應用程式專屬 (Application Exclusive) 時間。|  
|**最大應用程式專屬 (Application Exclusive) 時間**|在此內容中呼叫此函式的最大應用程式專屬 (Application Exclusive) 時間。|  
|**最小應用程式專屬 (Application Exclusive) 時間**|在此內容中呼叫此函式的最小應用程式專屬 (Application Exclusive) 時間。|  
  
## <a name="see-also"></a>另請參閱  
 [如何：自訂報表檢視資料行](../profiling/how-to-customize-report-view-columns.md)   
 [呼叫端/被呼叫端檢視 - .NET 記憶體取樣資料](../profiling/caller-callee-view-dotnet-memory-sampling-data.md)   
 [呼叫端/被呼叫端檢視 - 檢測資料](../profiling/caller-callee-view-instrumentation-data.md)   
 [呼叫端/被呼叫端檢視 - 取樣資料](../profiling/caller-callee-view-sampling-data.md)


