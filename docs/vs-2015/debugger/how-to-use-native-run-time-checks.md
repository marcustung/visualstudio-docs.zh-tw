---
title: HOW TO：使用原生執行階段檢查 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- c.runtime.errorchecks
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- VB
- CSharp
- C++
helpviewer_keywords:
- /RTC compiler option [C++], /O compiler option
- run-time checks, native
- stack, pointer corruption
- stack pointers, corruption
- /O compiler option, /RTC option
- run-time errors, error checks
- O compiler option, /RTC option
- debugger, runtime errors
- variables [debugger], loss of data
- runtime_checks pragma
- variables [debugger], catching dependencies on uninitialized local variables
- run-time errors, debugging
- debugger, native run-time checks
- optimized build option
- RTC compiler option, /O compiler option
- native run-time checks
- run-time checks
- debugging arrays
- stack pointers
- arrays [Visual Studio], debugging
ms.assetid: dc7b2f1e-5ff6-42e0-89b3-dc9dead83ee1
caps.latest.revision: 24
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 02f619d727b83e681d9dda6dd851c43f168f1311
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60101674"
---
# <a name="how-to-use-native-run-time-checks"></a>HOW TO：使用原生執行階段檢查
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

您可以在 Visual C++ 中使用原生 [runtime_checks](http://msdn.microsoft.com/library/ae50b43f-f88d-47ad-a2db-3389e9e7df5b) 來攔截最常見的執行階段錯誤，例如：  
  
- 堆疊指標損壞  
  
- 區域陣列滿溢  
  
- 堆疊損壞  
  
- 未初始化之區域變數的相依性  
  
- 指派至較短變數時流失資料  
  
  如果使用具有最佳化 ( **/O** ) 組建的 **/RTC**，便會造成編譯器錯誤。 如果您在最佳化組建中使用 `runtime_checks` Pragma，此 Pragma 會失效。  
  
  如果要偵錯的程式已啟用執行階段錯誤檢查，則當這個程式發生執行階段錯誤時，預設動作是停止和中斷偵錯工具。 您可以變更任何執行階段檢查的這個預設行為。 如需詳細資訊，請參閱 <<c0> [ 偵錯工具管理例外狀況](../debugger/managing-exceptions-with-the-debugger.md)。  
  
  下列程序描述如何在偵錯組建中啟用原生執行階段檢查，以及如何修改原生執行階段檢查行為。  
  
  本節的其他主題提供下列資訊：  
  
- [自訂使用 C 語言執行階段程式庫的執行階段檢查](../debugger/native-run-time-checks-customization.md)  
  
- [不使用 C 語言執行階段程式庫進行執行階段檢查](../debugger/using-run-time-checks-without-the-c-run-time-library.md)  
  
### <a name="to-enable-native-run-time-checks-in-a-debug-build"></a>在偵錯組建中啟用原生的執行階段檢查  
  
- 使用 **/RTC** 選項，並與 C 語言執行階段程式庫的偵錯版本建立連結 (例如 /MDd)。  
  
### <a name="to-modify-native-run-time-check-behavior"></a>修改原生的執行階段檢查行為  
  
- 使用 `runtime_checks` Pragma。  
  
## <a name="see-also"></a>另請參閱  
 [Visual Studio 偵錯](../debugger/debugging-in-visual-studio.md)   
 [runtime_checks](http://msdn.microsoft.com/library/ae50b43f-f88d-47ad-a2db-3389e9e7df5b)   
 [執行階段錯誤檢查](http://msdn.microsoft.com/library/c965dd01-57ad-4a3c-b1d6-5aa04f920501)
