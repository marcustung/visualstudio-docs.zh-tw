---
title: 如何： 同步處理程式碼專案規則集，與 Team 專案簽入原則 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.codeanalysis.selecttfsruleset
ms.assetid: 9b02f934-2db6-41ec-aaff-9c31ceec2f04
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: d7d20680fdba3affa5da4ee917fb12bf1b98457b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47500600"
---
# <a name="how-to-synchronize-code-project-rule-sets-with-team-project-check-in-policy"></a>如何：同步處理具有 Team 專案簽入原則的程式碼專案規則集
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主題的最新的版本可從[如何： 使用 Team 專案簽入原則同步處理程式碼專案規則集](https://docs.microsoft.com/visualstudio/code-quality/how-to-synchronize-code-project-rule-sets-with-team-project-check-in-policy)。  
  
您可以同步至 team 專案簽入原則的程式碼專案的程式碼分析設定藉由指定規則集，其中包含最少的規則集簽入原則中指定的規則。 您的名稱和位置的規則集簽入原則，就會通知您的開發人員潛在客戶。 您可以使用下列選項之一，確保專案的程式碼分析會使用一組正確的規則：  
  
-   簽入原則會使用其中一個 Microsoft 內建規則集，如果開啟的程式碼專案的 屬性 對話方塊中，顯示程式碼分析 頁面中，並選取規則集的程式碼專案設定的程式碼分析 頁面上。 Microsoft 標準規則集隨 Visual Studio 自動安裝設定為唯讀，並不應編輯。 如果不編輯規則集，保證中的原則和本機規則集的規則比對。  
  
-   如果簽入原則會使用自訂規則集，執行規則集檔案的 「 取得 」 作業建立的本機複本的版本控制中。 然後該區域中指定位置的程式碼專案的程式碼分析設定。 規則来符合的規則集簽入原則的最新狀態是否保證。  
  
     如果您將版本控制的位置對應至本機資料夾中的相同關聯性 team 專案的根目錄為您的程式碼專案時，此規則的位置會設定使用相對路徑。 相對路徑可確保程式碼分析的程式碼專案設定，可以移至其他電腦。  
  
-   自訂規則集簽入原則中的程式碼專案的複本。 請確定新的規則集包含簽入原則中的所有規則和任何其他您想要包含的規則。 您必須確定規則集包含所有規則，在簽入原則設定的規則。  
  
### <a name="to-specify-a-microsoft-standard-rule-set"></a>若要指定的 Microsoft 標準規則設定  
  
1.  在 **方案總管**，以滑鼠右鍵按一下程式碼專案，然後按一下 **屬性**。  
  
2.  按一下 **程式碼分析**。  
  
3.  在 **執行此規則集**清單中，按一下 簽入原則規則集。  
  
### <a name="to-specify-a-custom-check-in-policy-rule-set"></a>若要指定自訂簽入原則規則設定  
  
1.  如有必要，執行指定的簽入原則的規則集檔案的 「 取得 」 作業。  
  
2.  在 **方案總管**，以滑鼠右鍵按一下程式碼專案，然後按一下 **屬性**。  
  
3.  按一下 **程式碼分析**。  
  
4.  在 [**執行此規則集**清單中，按一下**\<瀏覽] >**。  
  
5.  在 **開啟**對話方塊方塊中，指定的簽入原則規則集檔案。  
  
### <a name="to-create-a-custom-rule-set-for-a-code-project"></a>若要建立自訂規則設定程式碼專案  
  
1.  請遵循下列其中一個稍早在本主題，以選取專案的 [設定] 對話方塊的 [程式碼分析] 頁面上的 team 專案簽入原則中的程序。  
  
2.  按一下 **開啟**。  
  
3.  新增或移除規則使用 規則集編輯器。  
  
     如需詳細資訊，請參閱 <<c0> [ 建立自訂規則集](../code-quality/creating-custom-code-analysis-rule-sets.md)。  
  
4.  儲存修改過的規則設定為 本機電腦上的.ruleset 檔案或 UNC 路徑。  
  
5.  開啟 [屬性] 對話方塊中，程式碼專案，並顯示**程式碼分析**頁面。  
  
6.  在 [**執行此規則集**清單中，按一下**\<瀏覽] >**。  
  
7.  在 **開啟**對話方塊方塊中，指定的規則集檔案。


