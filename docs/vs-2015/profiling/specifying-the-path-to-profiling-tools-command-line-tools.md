---
title: 指定分析工具命令列工具的路徑 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 7047bf18-5779-4f6e-872c-66e2fc47c969
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 7fadcff84c4b927a7718d7d4ad1311918ae0f18a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60066932"
---
# <a name="specifying-the-path-to-profiling-tools-command-line-tools"></a>指定程式碼剖析工具命令列工具的路徑
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 程式碼分析工具命令列工具的路徑不會加入 PATH 環境變數中。 在 32 位元電腦上，這些工具會在一個目錄中。 在 64 位元電腦上，程式碼分析工具有 32 位元和 64 位元兩種版本。  
  
## <a name="32-bit-computers"></a>32 位元電腦  
 在 32 位元電腦上，預設的分析工具目錄是*磁碟機*\Program Files\Microsoft Visual Studio 11.0\Team Tools\Performance Tools。  
  
## <a name="64-bit-computers"></a>64 位元電腦  
 在 64 位元電腦上，則會根據已進行程式碼剖析之應用程式的目標平台指定路徑。  
  
- 若是 32 位元應用程式，預設程式碼剖析工具目錄是：  
  
     *磁碟機*\Program Files (x86)\Microsoft Visual Studio 11.0\Team Tools\Performance Tools  
  
- 若是 64 位元應用程式，預設程式碼剖析工具目錄是：  
  
     *磁碟機*\Program Files (x86)\Microsoft Visual Studio 11.0\Team Tools\Performance Tools\x64
