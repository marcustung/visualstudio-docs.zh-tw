---
title: HOW TO：使用 RPC 偵錯對 COM 用戶端和伺服器 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.com
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- RPC (Remote Procedure Call), debugging COM clients and servers
- COM, debugging
- RPC (Remote Procedure Call)
- RPC (Remote Procedure Call), debugging
- COM clients, debugging
- COM servers, debugging
- out-of-process remote procedure call debugging
- remote debugging, RPC (Remote Procedure Call)
- in-process remote procedure call debugging
ms.assetid: 3e8526c8-43b5-4b87-8e0d-b22c24f0a3ea
caps.latest.revision: 26
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 2b40e7814fb809298c71d0078e644c12bd5a9a9e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60064956"
---
# <a name="how-to-debug-com-clients-and-servers-using-rpc-debugging"></a>HOW TO：使用 RPC 偵錯對 COM 用戶端和伺服器進行偵錯
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

您可使用遠端程序呼叫 (Remote Procedure Call，RPC) 偵錯功能，對 COM 用戶端/伺服器應用程式偵錯。 您必須啟用 RPC 偵錯才能使用它。 啟用 RPC 偵錯後，當您從用戶端逐步執行伺服器呼叫時，偵錯工具會附加至伺服器，讓您偵錯其程式碼。 附加偵錯工具後，您就能夠對用戶端和伺服器處理序，使用偵錯工具的所有功能。  
  
### <a name="to-enable-rpc-debugging"></a>若要啟用 RPC 偵錯  
  
1. 在 [ **工具** ] 功能表上按一下 [ **選項**]。  
  
2. 在 [選項] 對話方塊中按一下 [偵錯] 資料夾。  
  
3. 按一下 [原生] 頁面。  
  
4. 選取 [RPC 偵錯] 核取方塊。  
  
    > [!NOTE]
    >  若要偵錯 RPC 呼叫，您必須擁有系統管理員 (Administrator) 或進階使用者 (Power User) 權限。  
  
    > [!NOTE]
    >  RPC 若逐步執行到執行 Microsoft Windows Vista 的遠端伺服器中，則只有在該遠端伺服器已附加原生偵錯工具的情況下才能運作。 否則，RPC 呼叫將會失敗，而且不會產生錯誤訊息。 要不然，RPC 呼叫將會完成，但逐步執行 RPC 呼叫將沒有作用。  
  
## <a name="see-also"></a>另請參閱  
 [COM 伺服器和容器偵錯](../debugger/com-server-and-container-debugging.md)   
 [Visual Studio 偵錯](../debugger/debugging-in-visual-studio.md)
