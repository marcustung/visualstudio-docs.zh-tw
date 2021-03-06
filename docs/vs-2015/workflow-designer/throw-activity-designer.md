---
title: Throw 活動設計工具 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Throw.UI
ms.assetid: 5e97c947-be39-4a1f-af04-000e2e09528a
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: db909618971eeab2d92506d1c29b06290aa9263b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944213"
---
# <a name="throw-activity-designer"></a>Throw 活動設計工具
**擲回**活動設計工具會用來建立及設定<xref:System.Activities.Statements.Throw>活動。  
  
## <a name="the-throw-activity"></a>Throw 活動  
 <xref:System.Activities.Statements.Throw> 活動會擲回例外狀況。  
  
### <a name="using-the-throw-activity-designer"></a>使用 Throw 活動設計工具  
 **擲回**活動設計工具可在**錯誤處理**分類**工具箱**，即可存取的哪一個**工具箱** 索引標籤上的左側[!INCLUDE[wfd2](../includes/wfd2-md.md)](或者，選取**工具列**從**檢視**功能表或 CTRL + ALT + X。)  
  
 **擲回**活動設計工具可以從拖曳**工具箱**，放入[!INCLUDE[wfd2](../includes/wfd2-md.md)]介面只要活動通常放置的例如內部<xref:System.Activities.Statements.Sequence>。 這會建立<xref:System.Activities.Statements.Throw>活動，具有預設值**DisplayName**的擲回。 <xref:System.Activities.Activity.DisplayName%2A>可以編輯的標頭中的值**擲回**活動設計工具或**DisplayName**屬性方格的方塊。 <xref:System.Activities.Statements.Throw.Exception%2A> 屬性必須在屬性方格中編輯。  
  
### <a name="the-throw-properties"></a>擲回屬性  
 下表顯示 <xref:System.Activities.Statements.Throw> 屬性，並且描述屬性在設計工具中的使用方式。  
  
|屬性名稱|必要|使用量|  
|-------------------|--------------|-----------|  
|<xref:System.Activities.Activity.DisplayName%2A>|False|指定 <xref:System.Activities.Statements.Throw> 活動選用的易記名稱。 預設為 Throw。|  
|<xref:System.Activities.Statements.Throw.Exception%2A>|True|要擲回的例外狀況。 此例外狀況必須衍生自 <xref:System.Exception>。 若要指定例外狀況，請在屬性方格中輸入 Visual Basic 運算式。|  
  
## <a name="see-also"></a>另請參閱  
 [集合](../workflow-designer/collection-activity-designers.md)   
 [重新擲回](../workflow-designer/rethrow-activity-designer.md)   
 [Throw 活動設計工具](../workflow-designer/throw-activity-designer.md)   
 [TryCatch](../workflow-designer/trycatch-activity-designer.md)