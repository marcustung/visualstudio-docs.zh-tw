---
title: CrossSession | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: b9fcb9c3-7903-478c-9b7c-dbd94092fcba
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 05e1f2360b3257e44fde1af8be3554dd7fd95115
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2019
ms.locfileid: "54790329"
---
# <a name="crosssession"></a>CrossSession
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

VSPerfCmd.exe **CrossSession** 選項可讓分析工具從任何主控台工作階段中收集資料。 **CrossSession** 選項必須與 **Start** 選項搭配使用。  
  
 您可以使用縮寫 **CS** 取代 **CrossSession**。  
  
## <a name="syntax"></a>語法  
  
```  
VSPerfCmd.exe /Start:Method /CrossSession [Options]  
```  
  
#### <a name="parameters"></a>參數  
 無  
  
## <a name="valid-options"></a>有效選項  
 若要啟用另一個工作階段中的分析，必須指定含 **Start** 選項的 **CrossSession** 選項。 **CrossSession** 也必須指定於任何後續的 **VSPerfCmd Attach** 和 **Detach** 命令中。  
  
 **Start:** `Method`  
 **Start** 選項可將分析工具初始化為指定的分析方法。  
  
 **Attach:** _PID_[**,**_PID_]  
 開始分析指定的處理序。  
  
 **Detach**[**:**_PID_[,_PID_]]  
 停止分析指定的處理序。  
  
## <a name="example"></a>範例  
 在此範例中，**CrossSession** 選項是用來附加至已在另一個主控台工作階段中啟動的應用程式。  
  
```  
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /CrossSession  
VSPerfCmd.exe /Attach:12345 /CS  
```  
  
## <a name="see-also"></a>請參閱  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [對獨立應用程式進行程式碼剖析](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [對 ASP.NET Web 應用程式進行程式碼剖析](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [對服務進行程式碼剖析](../profiling/command-line-profiling-of-services.md)
