---
title: 在偵錯工具外執行我的程式時，如何偵錯存取違規？ | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.access
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- access violation debugging
- debugging [Visual Studio], access violations
ms.assetid: 780a298a-132e-4245-8370-8c82ca27c6c1
caps.latest.revision: 22
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 7cfdf356d21558f2024cb83e00bdfc930284b1d8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944758"
---
# <a name="how-can-i-debug-access-violations-when-running-my-program-outside-the-debugger"></a>在偵錯工具外執行我的程式時，如何偵錯存取違規？
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

問題說明  
 我的程式在 Visual Studio 環境裡執行正常，但是當我以 Windows 作業系統獨立執行它時，它會產生存取違規。 我該如何偵錯這個問題？  
  
## <a name="solution"></a>方案  
 設定 [ 偵錯](../debugger/just-in-time-debugging-in-visual-studio.md)選項並獨立執行您的程式，直到發生存取違規為止。 然後，在 [存取違規] 對話方塊中，您可以按一下 [取消] 來啟動偵錯工具。  
  
 請參閱知識庫 (Knowledge Base) 文件 Q133174「How to Locate Where a General Protection (GP) Fault Occurs」。 您可以在 MSDN Library CD 上或藉由搜尋找到知識庫文件[ http://support.microsoft.com/ ](http://support.microsoft.com/)。  
  
## <a name="see-also"></a>另請參閱  
 [對機器碼進行偵錯的常見問題集](../debugger/debugging-native-code-faqs.md)   
 [偵錯機器碼](../debugger/debugging-native-code.md)
