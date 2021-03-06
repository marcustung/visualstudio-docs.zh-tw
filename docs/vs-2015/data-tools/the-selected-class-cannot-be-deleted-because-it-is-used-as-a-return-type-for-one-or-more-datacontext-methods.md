---
title: 無法刪除選取的類別，因為它一或多個 DataContext 方法的傳回型別當做使用 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
ms.assetid: d68254a0-f3a1-47e2-aed3-a83471e1d711
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d8eb5f93ef3770b0d275d71d818e44d52a067f83
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094680"
---
# <a name="the-selected-class-cannot-be-deleted-because-it-is-used-as-a-return-type-for-one-or-more-datacontext-methods"></a>無法刪除所選取的類別，因為它是用來當做一或多個 DataContext 方法的傳回類型。
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

有一個或多個 <xref:System.Data.Linq.DataContext> 方法的傳回型別是選取的實體類別 (Class)。 刪除被 <xref:System.Data.Linq.DataContext> 方法當做傳回型別的實體類別，會使專案編譯作業失敗。 若要刪除選取的實體類別，請識別使用它的 <xref:System.Data.Linq.DataContext> 方法，並將這些方法的傳回型別設定為不同的實體類別。  
  
 若要還原的傳回型別<xref:System.Data.Linq.DataContext>方法，以其原始自動產生的類型，第一次刪除<xref:System.Data.Linq.DataContext>方法，從方法窗格，然後拖曳的物件**伺服器總管**/ **資料庫總管**拖曳至 O/R 設計工具一次。  
  
### <a name="to-correct-this-error"></a>更正這個錯誤  
  
1. 找出<xref:System.Data.Linq.DataContext>作為傳回型別中的實體類別，藉由選取的方法<xref:System.Data.Linq.DataContext>方法中的方法窗格，並檢查**傳回型別**中的屬性**屬性**視窗.  
  
2. 將**傳回型別**設定為不同的實體類別，或從方法窗格中刪除 <xref:System.Data.Linq.DataContext> 方法。  
  
## <a name="see-also"></a>另請參閱  
 [LINQ to SQL 工具，在 Visual Studio 中](../data-tools/linq-to-sql-tools-in-visual-studio2.md)   
 [逐步解說：建立 LINQ to SQL 類別 （O-R 設計工具）](http://msdn.microsoft.com/library/35aad4a4-2e8a-46e2-ae09-5fbfd333c233)   
 [DataContext 方法 （O/R 設計工具）](../data-tools/datacontext-methods-o-r-designer.md)   
 [如何：變更 DataContext 方法的傳回型別 (O/R 設計工具)](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md)
