---
title: 延遲活動設計工具 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Delay.UI
ms.assetid: f51742a8-2c9a-47d1-8a23-18459d03ae19
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 528317a97a9b2582442dacfcf9ba8a35943736e8
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58946005"
---
# <a name="delay-activity-designer"></a>Delay 活動設計工具
**延遲**活動設計工具會用來建立及設定<xref:System.Activities.Statements.Delay>活動。  
  
## <a name="the-delay-activity"></a>Delay 活動  
 <xref:System.Activities.Statements.Delay> 活動會延遲某個工作流程的執行，等候指定的時間長度。  
  
### <a name="using-the-delay-activity-designer"></a>使用 Delay 活動設計工具  
 **延遲**活動設計工具可在**基本型別**分類**工具箱**，即可存取的哪一個**工具箱**索引標籤[!INCLUDE[wfd2](../includes/wfd2-md.md)](或者，選取**工具列**從**檢視**功能表或 CTRL + ALT + X。)  
  
 **延遲**活動設計工具可以從拖曳**工具箱**，放入[!INCLUDE[wfd2](../includes/wfd2-md.md)]介面只要活動通常放置的例如內部<xref:System.Activities.Statements.Sequence>。 這會建立一個 <xref:System.Activities.Statements.Delay> 活動，具有 Delay 的預設 <xref:System.Activities.Activity.DisplayName%2A>。 <xref:System.Activities.Activity.DisplayName%2A>可以的標頭中編輯**延遲**活動設計工具或**DisplayName**屬性方格的方塊。  
  
### <a name="the-delay-properties"></a>Delay 屬性  
 下表顯示 <xref:System.Activities.Statements.Delay> 屬性，並且描述屬性在設計工具中的使用方式。 這些屬性可以在屬性方格中進行編輯，其中有一些可以在 [!INCLUDE[wfd2](../includes/wfd2-md.md)] 設計工具介面上編輯。  
  
|屬性名稱|必要|使用量|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|<xref:System.Activities.Statements.Delay> 活動的易記名稱。 預設為 Delay。 雖然 <xref:System.Activities.Activity.DisplayName%2A> 值並非絕對必要，但建議您盡量使用。|  
|<xref:System.Activities.Statements.Delay.Duration%2A>|True|延遲工作流程的時間長度。 這個屬性會在屬性方格中設定。 輸入常值 <xref:System.TimeSpan> (使用 00:00:00 格式) 或 Visual Basic 運算式，即可指定時間長度。|  
  
## <a name="see-also"></a>另請參閱  
 [基本項目](../workflow-designer/primitives-activity-designers.md)   
 [指派](../workflow-designer/assign-activity-designer.md)   
 [Delay 活動設計工具](../workflow-designer/delay-activity-designer.md)   
 [叫用方法](../workflow-designer/invokemethod-activity-designer.md)   
 [WriteLine](../workflow-designer/writeline-activity-designer.md)