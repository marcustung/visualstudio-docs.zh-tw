---
title: HOW TO：偵錯最佳化程式碼 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- breakpoints, in optimized code
- debugging [C++], optimized code
- optimization, debug builds
- debug builds, optimizing
- optimized code, debugging
ms.assetid: fc8eeeb8-6629-4c9b-99f7-2016aee81dff
caps.latest.revision: 28
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 35a5fc722a0d7b2ececa4aaa198381cdd3390a7b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944264"
---
# <a name="how-to-debug-optimized-code"></a>HOW TO：對最佳化程式碼進行偵錯
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

注意]
>  根據您目前使用的設定或版本，您所看到的對話方塊與功能表命令可能會與 [說明] 中描述的不同。 若要變更設定，請從 [工具] 功能表中選擇 [匯入和匯出設定]。 如需詳細資訊，請參閱 [在 Visual Studio 中自訂開發設定](http://msdn.microsoft.com/22c4debb-4e31-47a8-8f19-16f328d7dcd3)  
  
> [!NOTE]
>  [/Zo (增強最佳化的偵錯)](http://msdn.microsoft.com/library/eea8d89a-7fe0-4fe1-86b2-7689bbebbd7f) 編譯器選項 (在 Visual Studio Update 3 引入) 會針對最佳化程式碼 (不使用 **/Od** 編譯器選項建置的專案) 產生更豐富的偵錯資訊。 請參閱 [/O 選項 (最佳化程式碼)](http://msdn.microsoft.com/library/77997af9-5555-4b3d-aa57-6615b27d4d5d))。 這包括改善對於本機變數和內嵌函式的偵錯支援。  
>   
>  使用 **/Zo** 編譯器選項時，會停用 [編輯後繼續](../debugger/edit-and-continue-visual-csharp.md)。  
  
 當編譯器最佳化程式碼時，它會重新調整位置並重新組織指令。 這會產生較有效率的已編譯程式碼。 因為這種重新安排，偵錯工具不一定能辨識對應到一組指令的原始程式碼。  
  
 最佳化會影響：  
  
- 區域變數，這些區域變數可能會由最佳化程式移除，或是移至偵錯工具不認識的位置。  
  
- 函式內部的位置，這些位置在最佳化程式合併程式碼區塊時會變更。  
  
- 呼叫堆疊上框架的函式名稱，這個名稱在最佳化程式合併兩個函式時可能會出錯。  
  
  不過，假設所有框架都有符號，則您在呼叫堆疊上看見的框架幾乎一定是正確的。 如果您有堆疊損毀、以組件語言撰寫的函式，或是呼叫堆疊上的作業系統框架沒有相符的符號時，呼叫堆疊上的框架就會出錯。  
  
  全域變數和靜態變數一定會正確顯示， 結構配置也會。 如果您有結構的指標，而且指標的值是正確的，則結構的每個成員變數都會顯示正確的值。  
  
  由於這些限制，您應該盡可能地使用程式的非最佳化版本來進行偵錯。 根據預設，在 Visual C++ 程式的 [偵錯] 組態中會關閉最佳化，而在 [發行] 組態中會啟用最佳化。  
  
  然而，有時錯誤可能只出現在程式的最佳化版本中。 在這種情況下，您必須偵錯最佳化程式碼。  
  
### <a name="to-turn-on-optimization-in-a-debug-build-configuration"></a>若要啟動偵錯組建組態的最佳化  
  
1. 當您建立新專案時，選取 `Win32 Debug` 目標。 在您完成程式的偵錯，並準備好建置 `Win32 Release` 目標以前，請使用 `Win32``Debug` 目標。 編譯器不會最佳化 `Win32 Debug` 目標。  
  
2. 在 [方案總管] 中選取專案。  
  
3. 在 [檢視] 功能表上按一下 [屬性頁]。  
  
4. 請確認在 [屬性頁] 對話方塊的 [組態] 下拉式清單中，選取 `Debug`。  
  
5. 在左邊的資料夾檢視中，選取 **C/C++** 資料夾。  
  
6. 在 **C++** 資料夾下方，選取 `Optimization`。  
  
7. 在右邊的屬性清單裡，尋找 `Optimization`。 其旁邊的設定可能是 `Disabled (`[/Od](http://msdn.microsoft.com/library/b1ac31b7-e086-4eeb-be5e-488f7513f5f5)`)`。 從其他項目 (`Minimum Size``(`[/O1](http://msdn.microsoft.com/library/2d1423f5-53d9-44da-8908-b33a351656c2)`)`、`Maximum Speed``(`[/O2](http://msdn.microsoft.com/library/2d1423f5-53d9-44da-8908-b33a351656c2)`)`、`Full Optimization``(`[/Ox](http://msdn.microsoft.com/library/3ad7c30b-c615-428c-b1d0-2e024f81c760)`)` 或 `Custom`) 中選擇一個項目。  
  
8. 如果您選擇 `Custom` 的 `Optimization` 選項，現在就可以為其他顯示在屬性清單裡的任一屬性設定其選項。  
  
9. 選取 [組態屬性 | C/c + +，命令列] 節點的 [專案屬性] 頁面中，並新增`(` [/Zo](http://msdn.microsoft.com/library/eea8d89a-7fe0-4fe1-86b2-7689bbebbd7f) `)`來**其他選項**文字方塊。  
  
    > [!WARNING]
    >  `/Zo` 需要 Visual Studio 2013 Update 3 或更新版本。  
    >   
    >  新增 `/Zo` 將會停用 [編輯後繼續](../debugger/edit-and-continue-visual-csharp.md)。  
  
   偵錯最佳化程式碼時，使用 [反組譯碼] 視窗來查看哪些指令已經確實建立和執行。 設定中斷點時，您必須了解中斷點可能會隨著指令移動。 例如，請參考下列程式碼：  
  
```  
for (x=0; x<10; x++)  
```  
  
 假設您在這行設定中斷點。 您可以預期會叫用 10 次中斷點，但是如果程式碼已完成最佳化，便只會叫用中斷點一次。 原因是第一個指令會將 `x` 值設為 0。 編譯器會辨識這個動作只需做一次，並且將它移出迴圈外。 中斷點會隨著移動。 迴圈內部則仍保留比較和累加 `x` 的指令。 當您檢視 [反組譯碼] 視窗時，為取得更佳控制，[步驟單位](http://msdn.microsoft.com/8791dac9-64d1-4bb9-b59e-8d59af1833f9)會自動設為指令，這在逐步執行最佳化程式碼時非常有用。  
  
## <a name="see-also"></a>另請參閱  
 [偵錯工具安全性](../debugger/debugger-security.md)   
 [偵錯機器碼](../debugger/debugging-native-code.md)
