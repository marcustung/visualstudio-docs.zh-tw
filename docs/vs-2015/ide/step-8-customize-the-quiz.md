---
title: 步驟 8：自訂測驗 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: dc8edb13-1b23-47d7-b859-8c6f7888c1a9
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 75bde59c6e4b61c2775f188383fc9058a6c31242
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60109747"
---
# <a name="step-8-customize-the-quiz"></a>步驟 8：自訂測驗
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

在本教學課程的最後一部分，您將探索一些方法來自訂測驗，以及延伸您已經學習過的內容。 例如，請了解程式如何建立答案絕不是分數的隨機除法問題。 若要深入了解，請將 `timeLabel` 控制項轉換為不同的色彩，並提供受測者的提示。  
  
### <a name="to-customize-the-quiz"></a>自訂測驗  
  
- 測驗只剩五秒時，請將 [timeLabel] 控制項轉換為紅色，方法是設定其 [BackColor] 屬性 (`timeLabel.BackColor = Color.Red;`)。 在測驗結束時重設色彩。  
  
- 在 NumericUpDown 控制項中輸入正確答案時，播放音效來提供受測者的提示 (您必須撰寫每個控制項之 `ValueChanged()` 事件的事件處理常式，而只要受測者變更控制項的值時就會引發該事件)。  
  
### <a name="to-continue-or-review"></a>若要繼續或檢視  
  
- 若要下載測驗的完整版，請參閱[Complete Math Quiz tutorial sample](http://code.msdn.microsoft.com/Complete-Math-Quiz-8581813c)(完整的數學測驗教學課程範例)。  
  
- 若要前往下一個教學課程，請參閱[教學課程 3：建立配對遊戲](../ide/tutorial-3-create-a-matching-game.md)。  
  
- 若要回到上一個教學課程步驟，請參閱[步驟 7：新增乘法和除法問題](../ide/step-7-add-multiplication-and-division-problems.md)。
