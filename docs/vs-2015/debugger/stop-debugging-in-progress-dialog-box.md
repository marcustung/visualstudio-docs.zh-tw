---
title: 停止 [進度] 對話方塊中的偵錯 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.stopnow
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- SQL
- VB
- CSharp
- C++
helpviewer_keywords:
- Stop Debugging in Progress dialog box
ms.assetid: ed7ef49d-e25f-4a4d-9396-9bc7b4143117
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: c29754937d3b1ff7f4c44fc87929d84844743387
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58943876"
---
# <a name="stop-debugging-in-progress-dialog-box"></a>停止進行中的偵錯對話方塊
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

如果偵錯工具嘗試停止偵錯工作階段，但是工作階段需要一些時間才會停止，這個對話方塊就會出現。 停止偵錯工作階段通常很快就能完成，所以不會出現這個對話方塊。 不過，有時可能需要多花一些時間才能從所有正在偵錯的處理序中斷連結。 如果停止工作階段需花費數秒 (或是發生中斷連結錯誤)，這個對話方塊就會出現。 如果經常發生這種情況，可能是因為內部問題，建議您連絡產品支援服務。  
  
 您可以等候處理序中斷連結和此對話方塊消失，也可使用 [立即停止] 按鈕強制立即終止。  
  
 [立即停止]  
 按一下這個按鈕會立即結束偵錯工作階段。 使用**立即停止**會終止，而不是中斷連結正在進行偵錯的處理程序。 如果您正在偵錯系統處理序，使用 [立即停止] 終止這些處理序可能會產生非預期且不想要的結果。  
  
## <a name="see-also"></a>另請參閱  
 [偵錯工具安全性](../debugger/debugger-security.md)   
 [中斷連結程式](http://msdn.microsoft.com/f2c756c2-8079-474b-94c2-01c19a141a01)
