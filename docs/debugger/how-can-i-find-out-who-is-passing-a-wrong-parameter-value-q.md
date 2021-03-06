---
title: 了解誰傳錯參數值 |Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.parameters
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], parameters
- parameters [debugger]
- passing parameters, troubleshooting wrong values
- functions [debugger], detecting wrong parameter values
- parameter values, troubleshooting
ms.assetid: 1f1ae455-0e25-4e9d-b33f-53908f5bd6ce
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 548851a4e5811864e60d3a14368d6380f14f9e7e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60089389"
---
# <a name="how-can-i-find-out-who-is-passing-a-wrong-parameter-value"></a>如何發現誰傳錯參數值？
## <a name="problem-description"></a>問題說明
 我的函式中傳入了一個錯誤的參數。 這個函式會從許多地方呼叫。 我該如何確定錯誤值是誰傳出的？

## <a name="solution"></a>方案

#### <a name="to-resolve-this-problem"></a>若要解決這個問題

1. 在函式的開頭設定位置中斷點。

2. 以滑鼠右鍵按一下中斷點並選取 [條件]。

3. 在 [中斷點條件] 對話方塊中，按一下 [條件] 核取方塊。 請參閱[進階中斷點](../debugger/using-breakpoints.md#BKMK_Specify_a_breakpoint_condition_using_a_code_expression)。

4. 在文字方塊中輸入運算式，例如 `Var==3`；其中 `Var` 是含有錯誤值的參數名稱，而 `3` 則是傳入的錯誤值。

5. 選取 [為 True] 選項按鈕，然後按一下 [確定] 按鈕。

6. 現在再次執行程式。 當 `Var` 參數的值是 `3` 時，中斷點會造成程式暫止在函式的開頭。

7. 然後您可以使用 [呼叫堆疊] 視窗來找出呼叫函式並且巡覽原始程式碼。 如需詳細資訊，請參閱[如何：使用 [呼叫堆疊] 視窗](../debugger/how-to-use-the-call-stack-window.md)。

## <a name="see-also"></a>另請參閱
- [偵錯機器碼常見問題集](../debugger/debugging-native-code-faqs.md)
- [中斷點](https://msdn.microsoft.com/library/fe4eedc1-71aa-4928-962f-0912c334d583)
- [偵錯機器碼](../debugger/debugging-native-code.md)