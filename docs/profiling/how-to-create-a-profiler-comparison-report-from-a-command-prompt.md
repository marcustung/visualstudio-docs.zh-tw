---
title: 作法：從命令提示字元建立分析工具比較報表 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 00548d16-eb5b-46f7-8a65-862f98a43831
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 11a3850073068cf280901a6948565329e83f4629
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56638487"
---
# <a name="how-to-create-a-profiler-comparison-report-from-a-command-prompt"></a>作法：從命令提示字元建立分析工具比較報表
您可以產生 [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] 分析工具報表，以比較兩個分析資料 (.*vsp* 或 .*vsps*) 檔案的效能資料。 這份報表會顯示兩個分析工作階段所發生的差異、效能衰退和改善。 報表中的值呈現與您所指定之第一個檔案的基準線的差異或變更。 這項差異的計算是透過判斷舊值 (即基準值) 與新分析中結果值之間的差異。 分析工具資料的比較可以根據程式碼中的函式、應用程式中的模組、程式行、指令指標 (IP) 及型別。

 若要列出比較類別和欄位的識別碼，請鍵入下列命令列：

 **VSPerfReport /querydifftables**  *VspFileName1* *VspFileName2*

 使用下列語法來建立比較報表：

 **VSPerfReport /diff**  `VspFileName1` *VspFileName2* [**/**`Options`]

 您可以將下表中的選項新增至 **VSPerfReport /diff** 命令列。

|選項|說明|
|------------|-----------------|
|**DiffThreshold:**[*值*]|如果低於這個百分比臨界值，則忽略差異。 此外，將不會顯示值低於此臨界值的新資料。|
|**DiffTable:***TableName*|使用此資料表來比較檔案。 預設會使用函式資料表。 指定 **VSPerfReport /querydifftables** 中所列的識別碼。|
|**DiffColumn:***ColumnName*|使用此資料行來比較值。 預設會使用專有樣本百分比資料行。 指定 **VSPerfReport /querydifftables** 中所列的識別碼。|