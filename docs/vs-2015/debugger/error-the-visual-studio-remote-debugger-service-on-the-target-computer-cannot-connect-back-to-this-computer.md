---
title: 錯誤：在目標電腦上的 Visual Studio 遠端偵錯工具服務無法連回這部電腦 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.debug.error.service_access_denied_oncallback
dev_langs:
- FSharp
- VB
- CSharp
- C++
ms.assetid: 89ecf99d-66bf-4da0-a840-aa95b0be1702
caps.latest.revision: 15
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 7e828d0150e3519e588702be95111126fd1e2c04
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60069233"
---
# <a name="error-the-visual-studio-remote-debugger-service-on-the-target-computer-cannot-connect-back-to-this-computer"></a>錯誤：目標電腦上的 Visual Studio 遠端偵錯工具服務無法連回這部電腦
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

這個錯誤指出，Visual Studio 遠端偵錯工具服務正在某個使用者帳戶下執行，但是當該帳戶嘗試連接您在其中進行偵錯的電腦時無法進行驗證。  
  
 下表顯示可以存取該電腦的帳戶：  
  
|||||  
|-|-|-|-|  
||LocalSystem 帳戶|網域帳戶|在兩台電腦上都具有相同使用者名稱和密碼的本機帳戶|  
|兩台電腦都位於相同的網域|是|是|是|  
|網域上具有雙向信任的兩台電腦|否|否|是|  
|工作群組中的一或兩台電腦|否|否|是|  
|不同網域上的電腦|否|否|是|  
  
 其他情況：  
  
- 您用來執行 Visual Studio 遠端偵錯工具服務的帳戶，必須是遠端機器上的系統管理者，這樣才能偵錯任何處理序。  
  
- 這個帳戶也必須在使用 [本機安全性原則] 系統管理工具的遠端電腦上，獲得 `Log on as a service` 使用權限。  
  
- 如果您使用本機帳戶存取電腦，就必須在本機帳戶下執行 Visual Studio 遠端偵錯工具服務。  
  
### <a name="to-correct-this-error"></a>更正這個錯誤  
  
1. 請確定已在遠端電腦上正確設定 Visual Studio 遠端偵錯工具服務。 如需詳細資訊，請參閱 <<c0> [ 設定 Up the Remote Tools 在裝置上](http://msdn.microsoft.com/library/90f45630-0d26-4698-8c1f-63f85a12db9c)。  
  
2. 在可以存取偵錯工具主機電腦的帳戶下執行遠端偵錯工具服務，如上表所示。  
  
### <a name="to-add-log-on-as-a-service-privilege"></a>若要加入「以服務方式登入」權限  
  
1. 在 [開始] 功能表上，選擇 [控制台]。  
  
2. 必要時，在 [控制台] 中選擇 [傳統檢視]。  
  
3. 連按兩下 [系統管理工具] 。  
  
4. 在 [系統管理工具] 視窗中按兩下 [本機安全性原則]。  
  
5. 在 [本機安全設定] 視窗中展開 [本機原則] 資料夾。  
  
6. 按一下 [使用者權限指派]。  
  
7. 在 [原則] 欄中按兩下 [以服務方式登入]，檢視 [以服務方式登入] 對話方塊中目前的本機群組原則指派。  
  
8. 若要新增使用者，請按一下 [新增使用者或群組] 按鈕。  
  
9. 完成新增使用者後，按一下 [確定]。  
  
### <a name="to-work-around-this-error"></a>若要解決這個錯誤  
  
- 將遠端偵錯監視當成應用程式執行，不要當成服務執行。  
  
## <a name="see-also"></a>另請參閱  
 [遠端偵錯錯誤和疑難排解](../debugger/remote-debugging-errors-and-troubleshooting.md)   
 [Remote Debugging](../debugger/remote-debugging.md)
