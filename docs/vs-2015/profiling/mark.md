---
title: 標記 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 1d72cef3-bb09-4bbb-8864-6ea0ab623ff9
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: e6d7902ec588af2687b048639a930847ec02b3fa
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2019
ms.locfileid: "54769086"
---
# <a name="mark"></a>標記
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe 的 [標記] 選項會將指定的資訊插入分析資料檔案中。 個別的 VSPerfReport 報表或分析工具 UI 的標記報表檢視中，則可以列出標記。 [標記] 可用以指定報表的起點和終點並檢視篩選。  
  
 [標記] 選項必須是命令列上指定的唯一選項。  
  
## <a name="syntax"></a>語法  
  
```  
VSPerfCmd.exe /Mark:MarkID,[MarkName]  
```  
  
#### <a name="parameters"></a>參數  
 `MarkID`  
 使用者定義的整數，在分析工具檢視和報表中列為標記識別碼。 `MarkID` 不必是唯一的。  
  
 `MarkName`  
 (選擇性) 使用者定義的字串，在分析工具檢視和報表中列為標記名稱。 如未指定 `MarkName`，標記清單的 [標記名稱] 欄位會是空的。 以引號括住包含空格或正斜線 ("/") 的字串。  
  
## <a name="example"></a>範例  
 本例會插入識別碼為 123、標記名稱為的 "TestMark" 的標記。  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp  
VSPerfCmd.exe /Launch:TestApp.exe  
VSPerfCmd.exe /Mark:123,TestMark  
```  
  
## <a name="see-also"></a>請參閱  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [對獨立應用程式進行程式碼剖析](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [對 ASP.NET Web 應用程式進行程式碼剖析](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [對服務進行程式碼剖析](../profiling/command-line-profiling-of-services.md)
