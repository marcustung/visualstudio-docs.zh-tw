---
title: 使用分層圖驗證程式碼 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- layer diagrams, validating
- validation, layer diagrams
- validation, code
- code exploration, validating
- architecture, validating
- Visual Studio Ultimate, validating code
- validation, architecture
- validation, dependencies
- MSBuild, tasks
- MSBuild, layer diagrams
- MSBuild, validating code
ms.assetid: 70cbe55d-4b33-4355-b0a7-88c770a6f75c
caps.latest.revision: 84
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 143daa7f54179867325206f62a852fd685852a6f
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60051813"
---
# <a name="validate-code-with-layer-diagrams"></a>使用分層圖驗證程式碼
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

若要確定程式碼不會與其設計相衝突，請在 Visual Studio 中以分層圖驗證程式碼。 這可協助您：  
  
- 尋找在您的程式碼與分層圖相依性之間的衝突。  
  
- 尋找可能會受到建議變更所影響的相依性。  
  
   例如，您可以編輯圖層圖表來顯示潛在的架構變更，然後驗證程式碼，以便查看受影響的相依性。  
  
- 將程式碼重構或移轉至不同設計。  
  
   在您將程式碼移至不同的架構時，請尋找需要運作的程式碼或相依性。  
  
  **需求**  
  
- Visual Studio  
  
- 在您的 Team Foundation Build 伺服器的 Visual Studio 使用 Team Foundation Build 自動驗證程式碼  
  
- 包含具有分層圖的模型專案的方案。 這張分層圖必須與您想要驗證的 Visual C# .NET 或 Visual Basic .NET 的成品連結。 請參閱[從您的程式碼建立分層圖](../modeling/create-layer-diagrams-from-your-code.md)。  
  
  若要查看哪些 Visual Studio 版本支援這項功能，請參閱 [Version support for architecture and modeling tools](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport)。  
  
  您可以在 Visual Studio 中的開放分層圖或從命令提示字元手動驗證程式碼。 您也可以在執行本機組建或 Team Foundation Build 時自動驗證程式碼。 請參閱[Channel 9 影片：設計和驗證架構使用圖層圖表](http://go.microsoft.com/fwlink/?LinkID=252073)。  
  
> [!IMPORTANT]
>  如果您要以 Team Foundation Build 執行圖層驗證，您也必須在您的組建伺服器上安裝相同版本的 Visual Studio。  
  
- [項目是否支援驗證](#SupportsValidation)  
  
- [包含其他.NET 組件和專案來進行驗證](#IncludeReferences)  
  
- [手動驗證程式碼](#ValidateManually)  
  
- [自動驗證程式碼](#ValidateAuto)  
  
- [針對圖層驗證問題進行疑難排解](#TroubleshootingValidation)  
  
- [了解並解決圖層驗證錯誤](#UnderstandingValidationErrors)  
  
## <a name="SupportsValidation"></a> 項目是否支援驗證  
 您可以將圖層連結到網站、Office 文件、純文字檔以及跨多個應用程式共用之專案中的檔案，不過，驗證流程不包含這些檔案。 對於連結至個別圖層之專案或組件的參考，如果這些圖層之間沒有任何相依性，則不會出現驗證錯誤。 除非程式碼使用這些參考，否則不會考量此類參考的相依性。  
  
1. 在分層圖中，選取一或多個圖層，以滑鼠右鍵按一下您的選擇，然後按一下**檢視連結**。  
  
2. 在 **圖層總管**，看看**支援驗證**資料行。 如果值為 false，則這個項目不支援驗證。  
  
## <a name="IncludeReferences"></a> 包含其他.NET 組件和專案來進行驗證  
 當您拖曳項目到分層圖時，對應的.NET 組件或專案的參考會自動加入至**圖層參考**模型專案中的資料夾。 這個資料夾包含組件的參考以及驗證期間分析的專案。 您也可以手動加入其他 .NET 組件和專案以進行驗證，而不用手動拖曳到分層圖。  
  
1. 在**方案總管**，以滑鼠右鍵按一下模型專案或**圖層參考**資料夾，然後再按一下**加入參考**。  
  
2. 在 [**加入參考**] 對話方塊中，選取組件或專案，然後按一下**確定**。  
  
## <a name="ValidateManually"></a> 手動驗證程式碼  
 如果您有開啟分層圖連結到方案項目時，您可以執行**驗證**從圖表的捷徑命令。 您也可以使用命令提示字元執行**msbuild**命令搭配**validatearchitecture**自訂的屬性設定為**True**。 例如，在您變更程式碼時定期執行圖層驗證，以便早期攔截相依性衝突。  
  
#### <a name="to-validate-code-from-an-open-layer-diagram"></a>若要從開啟的圖層圖表驗證程式碼  
  
1. 以滑鼠右鍵按一下圖表介面，然後按一下**驗證架構**。  
  
    > [!NOTE]
    >  根據預設，**建置動作**上的圖層圖表 (.layerdiagram) 檔案的屬性設定為**Validate** ，讓圖表納入驗證程序。  
  
     **錯誤清單**視窗會報告所發生的任何錯誤。 如需有關驗證錯誤的詳細資訊，請參閱 <<c0> [ 了解並解決圖層驗證的錯誤](#UnderstandingValidationErrors)。  
  
2. 若要檢視每個錯誤的來源，請連按兩下中的錯誤**錯誤清單**視窗。  
  
    > [!NOTE]
    >  [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 可能會顯示 Code Map，而非錯誤來源。 如果程式碼具有並非由圖層圖表所指定的組件相依性，或是程式碼遺失了圖層圖表所指定的相依性，則會出現此情況。 請檢閱 Code Map 或程式碼，以判斷相依性是否應存在。 如需 code map 的詳細資訊，請參閱[對應方案之間的相依性](../modeling/map-dependencies-across-your-solutions.md)。  
  
3. 若要管理錯誤，請參閱[管理驗證錯誤](#ManageErrors)。  
  
#### <a name="to-validate-code-at-the-command-prompt"></a>若要在命令提示字元驗證程式碼  
  
1. 開啟 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 命令提示字元。  
  
2. 選擇下列其中一項：  
  
   - 若要根據方案中的特定模型專案來驗證程式碼，請使用下列自訂屬性執行 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]。  
  
     ```  
     msbuild <FilePath+ModelProjectFileName>.modelproj /p:ValidateArchitecture=true  
     ```  
  
     - 或 -  
  
       瀏覽至包含模型專案 (.modelproj) 檔案和圖層圖表的資料夾，然後使用下列自訂屬性執行 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]：  
  
     ```  
     msbuild /p:ValidateArchitecture=true   
     ```  
  
   - 若要根據方案中的所有模型專案來驗證程式碼，請使用下列自訂屬性執行 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]：  
  
     ```  
     msbuild <FilePath+SolutionName>.sln /p:ValidateArchitecture=true   
     ```  
  
     - 或 -  
  
       瀏覽至方案資料夾 (其中必須包含圖層圖表所在的模型專案)，然後使用下列自訂屬性執行 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]：  
  
     ```  
     msbuild /p:ValidateArchitecture=true  
     ```  
  
     發生的任何錯誤都將列出。 如需詳細資訊[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]，請參閱 < [MSBuild](../msbuild/msbuild.md)並[MSBuild 工作](../msbuild/msbuild-task.md)。  
  
   如需有關驗證錯誤的詳細資訊，請參閱 <<c0> [ 了解並解決圖層驗證的錯誤](#UnderstandingValidationErrors)。  
  
### <a name="ManageErrors"></a> 管理驗證錯誤  
 在開發過程中，您可以隱藏驗證期間已報告過的某些衝突。 例如，您可能會想要隱藏已經處理的錯誤，或是與特定情節無關的錯誤。 當您隱藏錯誤時，最好在 [!INCLUDE[esprfound](../includes/esprfound-md.md)] 中記錄工作項目。  
  
> [!WARNING]
>  您必須先連接 TFS 原始程式碼控制 (SCC) 才能建立或連結工作項目。 若您嘗試開啟連接至不同的 TFS SCC，Visual Studio 會自動關閉目前方案。 請先確認您已連接至適當的 SCC，再嘗試建立或連結至工作項目。 在更新版本的 Visual Studio 中，如果沒有連接至 SCC 即無法使用功能表命令。  
  
##### <a name="to-create-a-work-item-for-a-validation-error"></a>若要針對驗證錯誤建立工作項目  
  
- 在 **錯誤清單**視窗中，以滑鼠右鍵按一下錯誤，指向**建立工作項目**，然後按一下您想要建立的工作項目類型。  
  
  使用這些工作來管理中的驗證錯誤**錯誤清單**視窗：  
  
|**若要**|**請遵循下列步驟**|  
|------------|----------------------------|  
|在驗證期間隱藏選取的錯誤|以滑鼠右鍵按一下一或多個選取的錯誤、 指向**管理驗證錯誤**，然後按一下**隱藏錯誤**。<br /><br /> 隱藏的錯誤會以刪除線的格式出現。 當您下一次執行驗證時，這些錯誤將不會出現。<br /><br /> 隱藏的錯誤會在對應圖層圖表檔案的 .suppressions 檔案中追蹤。|  
|停止隱藏選取的錯誤|以滑鼠右鍵按一下選取的隱藏的錯誤，並指向**管理驗證錯誤**，然後按一下**停止隱藏錯誤**。<br /><br /> 選取的隱藏錯誤將會在下一次執行驗證時出現。|  
|還原所有隱藏的錯誤**錯誤清單**視窗|以滑鼠右鍵按一下任何一處**錯誤清單** 視窗中，指向**管理驗證錯誤**，然後按一下**顯示所有隱藏的錯誤**。|  
|隱藏所有隱藏的錯誤**錯誤清單**視窗|以滑鼠右鍵按一下任何一處**錯誤清單** 視窗中，指向**管理驗證錯誤**，然後按一下**隱藏所有隱藏的錯誤**。|  
  
## <a name="ValidateAuto"></a> 自動驗證程式碼  
 您可以在每次執行本機組建時執行圖層驗證。 如果您的小組使用 Team Foundation Build，可以閘道簽入來執行圖層驗證，其中您可以藉由建立自訂 MSBuild 工作來指定，以及使用組建報告收集驗證錯誤。 若要建立閘道的簽入組建，請參閱[使用閘道的簽入建置流程來驗證變更](http://msdn.microsoft.com/library/9cfc8b9c-1023-40fd-8ab5-1b1bd9c172ec)。  
  
#### <a name="to-validate-code-automatically-during-a-local-build"></a>在本機組建執行期間自動驗證程式碼  
  
- 使用文字編輯器來開啟模型專案 (.modelproj) 檔案，然後加入下列屬性：  
  
```  
<ValidateArchitecture>true</ValidateArchitecture>  
```  
  
 \-或-  
  
1. 在 **方案總管**，以滑鼠右鍵按一下模型專案包含圖層圖表或圖表，然後按一下**屬性**。  
  
2. 在 **屬性**視窗中，將模型專案的**驗證架構**屬性設**True**。  
  
    這會將模型專案納入驗證程序中。  
  
3. 在 [**方案總管] 中**，按一下您想要用於驗證的圖層圖表 (.layerdiagram) 檔案。  
  
4. 中**屬性** 視窗中，請確定圖表**建置動作**屬性設定為**Validate**。  
  
    這會將圖層圖表納入驗證程序中。  
  
   若要管理 [錯誤清單] 視窗中的錯誤，請參閱[管理驗證錯誤](#ManageErrors)。  
  
#### <a name="to-validate-code-automatically-during-a-team-foundation-build"></a>在 Team Foundation Build 執行期間自動驗證程式碼  
  
1. 在  **Team Explorer**，按兩下組建定義之後，，然後按一下**程序**。  
  
2. 底下**建置流程參數**，展開**編譯**，然後輸入下列**MSBuild 引數**參數：  
  
    `/p:ValidateArchitecture=true`  
  
   如需有關驗證錯誤的詳細資訊，請參閱 <<c0> [ 了解並解決圖層驗證的錯誤](#UnderstandingValidationErrors)。 如需 [!INCLUDE[esprbuild](../includes/esprbuild-md.md)] 的詳細資訊，請參閱：  
  
- [建置應用程式](http://msdn.microsoft.com/library/a971b0f9-7c28-479d-a37b-8fd7e27ef692)  
  
- [使用預設範本建置程序](http://msdn.microsoft.com/library/43930b12-c21b-4599-a980-2995e3d16e31)  
  
- [修改根據 UpgradeTemplate.xaml 的舊版建置](http://msdn.microsoft.com/library/ee1a8259-1dd1-4a10-9563-66c5446ef41c)  
  
- [自訂建置流程範本](http://msdn.microsoft.com/library/b94c58f2-ae6f-4245-bedb-82cd114f6039)  
  
- [執行中組建的監視進度](http://msdn.microsoft.com/library/e51e3bad-2d1d-4b7b-bfcc-c43439c6c8ef)  
  
## <a name="TroubleshootingValidation"></a> 針對圖層驗證問題進行疑難排解  
 下列表格描述圖層驗證的問題及其解決方式。 這些問題不同於因程式碼與設計衝突而導致的錯誤。 如需有關這些錯誤的詳細資訊，請參閱 <<c0> [ 了解並解決圖層驗證的錯誤](#UnderstandingValidationErrors)。  
  
|**問題**|**可能的原因**|**解決方法**|  
|---------------|------------------------|--------------------|  
|發生非預期的驗證錯誤。|若圖層圖表是從方案總管中的其他圖層圖表或是從相同模型專案中的圖層圖表複製來的，系統即不會對此圖層圖表進行驗證。 以這種方式複製的圖層圖表所包含的參考會與原始圖層圖表相同。|將新圖層圖表加入至模型專案。<br /><br /> 將來源圖層圖表中的項目複製到新圖表。|  
  
## <a name="UnderstandingValidationErrors"></a> 了解並解決圖層驗證錯誤  
 當您針對分層圖驗證程式碼時，如果程式碼設計發生衝突便會產生驗證錯誤。 例如，下列條件可能造成圖層驗證發生錯誤：  
  
- 成品指派給錯誤的圖層。 在此情況下，請移動成品。  
  
- 類別之類的成品以與架構發生衝突的方式使用另一個類別。 在此情況下，請重構程式碼以移除相依性。  
  
  若要解決這些錯誤，請更新程式碼直到驗證時不再出現錯誤為止。 您可以透過互動方式執行這項工作。  
  
  以下章節說明用於這些錯誤的語法，解釋這些錯誤的意義，並且建議解析或管理這些錯誤的作法。  
  
|**語法**|**描述**|  
|----------------|---------------------|  
|*ArtifactN*(*ArtifactTypeN*)|*ArtifactN*是與分層圖的圖層相關聯的成品。<br /><br /> *ArtifactTypeN*是種*ArtifactN*，例如**類別**或是**方法**，例如：<br /><br /> MySolution.MyProject.MyClass.MyMethod(Method)|  
|*NamespaceNameN*|命名空間的名稱。|  
|*LayerNameN*|圖層圖表上圖層的名稱。|  
|*DependencyType*|之間的相依性關聯性的類型*Artifact1*並*Artifact2*。 例如， *Artifact1*已**呼叫**關聯性*Artifact2*。|  
  
|**錯誤語法**|**錯誤描述**|  
|----------------------|---------------------------|  
|AV0001:無效的相依性：*Artifact1*(*ArtifactType1*) --> *Artifact2*(*ArtifactType2*)<br /><br /> 圖層：*LayerName1*， *LayerName2* &#124;相依性：*DependencyType*|*Artifact1*中*LayerName1*上不應該有相依性*Artifact2*中*LayerName2*因為*LayerName1*沒有直接相依*LayerName2*。|  
|AV1001:無效的命名空間：*成品*<br /><br /> 圖層：*LayerName* &#124;必要的命名空間：*NamespaceName1* &#124;目前的命名空間：*NamespaceName2*|*LayerName*要求其相關的成品必須屬於*NamespaceName1*。 *成品*處於*NamespaceName2*，而非*NamespaceName1*。|  
|AV1002:依存於禁止的命名空間：*Artifact1*(*ArtifactType1*) &#124; *Artifact2*(*ArtifactType2*)<br /><br /> 圖層：*LayerName* &#124;禁止的命名空間：*NamespaceName* &#124;相依性：*DependencyType*|*LayerName*要求其相關的成品必須相依於*NamespaceName*。 *Artifact1*不能依賴*Artifact2*因為*Artifact2*處於*NamespaceName*。|  
|AV1003:在禁止的命名空間：*Artifact*(*ArtifactType*)<br /><br /> 圖層：*LayerName* &#124;禁止的命名空間：*NamespaceName*|*LayerName*要求其相關的成品不能屬於*NamespaceName*。 *成品*所屬*NamespaceName*。|  
|AV3001:遺漏連結：圖層 '*LayerName*'連結到'*成品*' 找不到其中。 您是否遺漏了組件參考?|*LayerName*連結至找不到的成品。 例如，類別的連結可能因為模型專案遺漏包含該類別之組件的參考而遺失。|  
|AV9001:架構分析發現內部錯誤。 結果可能不完整。 如需詳細資訊，請參閱詳細建置事件記錄檔或輸出視窗。|如需詳細資訊，請參閱建置事件記錄檔或輸出視窗。|  
  
## <a name="security"></a>安全性  
  
## <a name="see-also"></a>另請參閱  
 [在開發期間驗證您的系統](../modeling/validate-your-system-during-development.md)
