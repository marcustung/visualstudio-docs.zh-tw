---
title: HOW TO：指定要啟動的二進位檔 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.performance.property.itemlaunch
helpviewer_keywords:
- profiling tools, launching
- performance tools, launching
- performance sessions, launching
ms.assetid: ba77fcf4-8d78-49f1-b8f3-7dd0acf84306
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 919e84393cf4aef929a504aadbefe905afe24bfb
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60098424"
---
# <a name="how-to-specify-the-binary-to-start"></a>HOW TO：指定要啟動的二進位檔
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

若要剖析二進位檔 (如 DLL)，您必須在 [\<目標> 屬性頁] 對話方塊中輸入資訊。 這項資訊會指示 DLL 專案可以在何處找到呼叫的應用程式。  
  
 **需求**  
  
- [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)]、[!INCLUDE[vsPreLong](../includes/vsprelong-md.md)]、[!INCLUDE[vsPro](../includes/vspro-md.md)]  
  
### <a name="to-specify-the-executable-to-start"></a>指定要啟動的可執行檔  
  
1. 在 [效能總管] 中，以滑鼠右鍵按一下目標二進位檔，然後按一下 [屬性]。  
  
2. 在 [屬性頁] 對話方塊中，按一下 [啟動] 屬性。  
  
3. 選取 [覆寫專案屬性] 核取方塊。  
  
4. 在 [要啟動的可執行檔] 文字方塊中，指定檔案位置。  
  
5. 在 [引數] 文字方塊中，指定啟動應用程式所需的引數。  
  
6. 在 [工作目錄] 文字方塊中，指定目錄位置。  
  
7. 按一下 [確定] 。  
  
## <a name="see-also"></a>另請參閱  
 [設定效能工作階段](../profiling/configuring-performance-sessions.md)
