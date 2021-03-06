---
title: 管理模型與版本控制下的圖表 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- models, version control
ms.assetid: ca6443e3-6d11-4da8-aae7-ca7dcc410076
caps.latest.revision: 32
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2a7ba74c18097f7eb4b2f8ff50780dfd5ffb57df
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60080316"
---
# <a name="manage-models-and-diagrams-under-version-control"></a>在版本控制下管理模型與圖表
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

藉助 [使用 Team Foundation 版本控制或 Git](http://msdn.microsoft.com/library/33267cee-fe5f-4aa3-b2cd-6d22ceace314)，管理不同版本的模型專案和圖表，包含 Code Map (.dgml 檔案)；可搭配內部部署的 Team Foundation Server 或搭配 Visual Studio Team Services 在雲端使用。  
  
 若要查看哪些 Visual Studio 版本支援這項功能，請參閱 [Version support for architecture and modeling tools](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport)。  
  
> [!IMPORTANT]
>  當有多位使用者進行同一個模型專案時，請務必特別注意。 了解如何 [組織中型或大型專案中的模型](../modeling/structure-your-modeling-solution.md)。  
  
## <a name="ModelingProjects"></a> 模型專案中的檔案  
 模型專案上可以有多位使用者同時執行工作 (假設這些使用者處理不同的檔案)。  
  
 若要避免或解決不同使用者所做變更之間的衝突，請務必了解模型在檔案中儲存的方式。  
  
- 每一個套件都會儲存在個別的 **.uml** 檔案中，該檔案則保存在 **ModelDefinition** 專案資料夾內。 此模型同時具有 **.uml** 檔案。 如果其中一個檔案遭刪除或損毀，則會失去對應的套件或模型。  
  
- 每一個圖表都會儲存在兩個檔案中。 例如，類別圖表有：  
  
    - **DiagramName.classdiagram** - 如果此檔案遭刪除或損毀，則會失去圖表，但是它顯示的類別和關聯仍會保留在模型中，而且可以在 UML 模型總管中看見。  
  
    - **DiagramName.classdiagram.layout** - 如果刪除此檔案，圖形仍會在圖表中顯示，但是會失去其大小和位置。 每個配置檔案都是圖表檔的附屬項目。 若要顯示配置檔案，請在方案總管中按一下圖表檔旁邊的 [+]。  
  
> [!NOTE]
>  請務必維護檔案之間的一致性。 例如，若您使用原始檔控制回復 .uml 檔案中的變更，則必須同時回復 .*diagram 和 .layout 檔案中對應的變更。 中的項目表示。\*如果.uml 檔案中未也表示，圖表檔案將會遺失。  
  
## <a name="Shared"></a> 使用共用模型專案  
 若要減少並行處理專案的不同部分時發生的衝突：  
  
- 將您的模型專案分成數個套件，代表不同的工作區域。 請將整個模型移到套件內，而不要留在根模型中。 如需詳細資訊，請參閱 <<c0> [ 定義套件和命名空間](../modeling/define-packages-and-namespaces.md)。  
  
- 不同的使用者不應同時處理相同的套件或圖表。  
  
- 若您使用設定檔，請確定每個人都安裝相同的設定檔。 請參閱[來自訂您的模型，使用設定檔和造型](../modeling/customize-your-model-with-profiles-and-stereotypes.md)。  
  
- 為協助確定您僅變更由您所處理的套件：  
  
    - 請設定 UML 類別、元件或使用案例圖的 **LinkedPackage** 屬性。  
  
    - 在 UML 模型總管中，立即將剛建立的活動或互動拖曳至您的套件中。 這個項目會在您建立活動圖表或順序圖表的第一個節點時，出現在 UML 模型總管中。  
  
- 為幫助您追蹤套件，請重新命名此套件檔以反映實際的套件名稱。  
  
- 在 [!INCLUDE[esprscc](../includes/esprscc-md.md)]中，請務必在完整的模型專案上執行 [簽入]  和 [取得最新的版本]  作業，絕不要在個別檔案上執行。  
  
- 務必先立即執行 [取得]  作業，再接著簽入模型專案。  
  
- 務必先關閉所有圖表，再執行 [取得]  作業。  
  
    > [!NOTE]
    >  若在執行 [取得] 時有開啟的檔案，且此作業導致本機變更，則會提示您重新載入檔案。 在此情況下，請按一下 [否] ，然後重新載入整個專案。 以滑鼠右鍵按一下 **方案總管**中的模型專案節點，並按一下 [卸載專案] ，然後按一下 [重新載入專案] 。  
  
### <a name="Exclusive"></a> 需要獨佔存取權的模型變更  
 在您進行下列種類的變更之前，請先確定整個專案有「簽出」鎖定。  
  
- 重新命名或刪除從其他套件參考的項目。  
  
- 變更跨套件範圍的關聯性屬性。  
  
- 如需了解「簽出」鎖定，請參閱 [簽出和編輯檔案](http://msdn.microsoft.com/library/eb404d63-c448-4994-9416-3e6d50ec554a)。  
  
##### <a name="to-move-a-diagram-file-in-or-out-of-a-project-folder"></a>在專案資料夾中移入或移出圖表檔  
  
1. 啟動 **Visual Studio 的開發人員命令提示字元**。  
  
2. 使用 **tf rename** 移動圖表檔及其 **.layout** 檔案：  
  
     `tf rename sourcePath targetPath`  
  
3. 在方案總管中，以滑鼠右鍵按一下檔案，然後按一下 [從專案移除] 。  
  
4. 將檔案加入目的資料夾。  
  
     在方案總管中，以滑鼠右鍵按一下目的資料夾或專案，指向 [加入] ，然後按一下 [現有項目] 。 在對話方塊中選取圖表檔，然後按一下 [加入] 。 配置檔將自動加入。  
  
    > [!NOTE]
    >  您無法將此檔案移至不同的專案。  
  
## <a name="Merging"></a> 合併模型檔和圖表中的變更  
 多位使用者同時處理模型之後， [!INCLUDE[esprscc](../includes/esprscc-md.md)] 將提示您合併模型檔案中的變更。 依循前面幾節中所述之方法處理不同的專案，將可避免大部分的合併。 通常剩餘的衝突可安全無虞地自動合併。 下列變更應該很容易上手：  
  
- 生命線的類型。 當您將生命線加入互動 (順序圖表) 時，除非您是從現有的類型建立生命線，否則其類型會儲存到根模型中。  
  
- 新的活動和互動一開始會儲存到根模型中。  
  
- 加入項目和關聯性。  
  
- 重新命名或刪除僅在自身套件內參考的項目。  
  
## <a name="see-also"></a>另請參閱  
 [分析並製作架構模型](../modeling/analyze-and-model-your-architecture.md)   
 [共用模型及匯出圖表](../modeling/share-models-and-exporting-diagrams.md)
