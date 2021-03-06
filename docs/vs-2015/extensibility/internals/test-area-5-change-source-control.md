---
title: 測試區域 5：變更原始檔控制 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], changing
- source control plug-ins, changing source control
ms.assetid: fdf09e00-108c-4d51-bbd5-72452d52a490
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d79281e2fef6a7ae77a2ba6c8375f47dc6520b3a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58939446"
---
# <a name="test-area-5-change-source-control"></a>測試區域 5：變更原始檔控制
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

此原始檔控制外掛程式的測試區域涵蓋變更原始檔控制，透過**變更原始檔控制**命令。  
  
 **變更原始檔控制**命令為使用者提供四個基本的函式：  
  
- **繫結：**  
  
   可讓使用者建立或重新建立方案/專案和版本存放區之間的原始檔控制 連結。  
  
- **解除繫結：**  
  
   移除每個連線為基礎的原始檔控制專案/方案。  
  
- **連接/中斷連線：**  
  
  切換連線或離線狀態的受控制的解決方案，區域 3 中所含。 如需詳細資訊，請參閱[測試區域 3:簽出 / 復原簽出](../../extensibility/internals/test-area-3-check-out-undo-checkout.md)。  
  
## <a name="command-menu-access"></a>命令功能表存取  
 下列[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]與測試案例中會使用整合式的開發環境功能表路徑。  
  
 變更原始檔控制：**檔案**，**原始檔控制**，**變更原始檔控制**。  
  
## <a name="test-cases"></a>測試案例  
 以下是針對特定測試案例**變更原始檔控制**命令測試區域。  
  
### <a name="case-5a-bind"></a>案例 5a:繫結  
 繫結可讓使用者選取的專案和方案中新增來源的程式碼控制資訊。 若要識別這些是要加入原始檔控制中的專案通常提示使用者。 使用者不可能的這項作業 （與加入原始檔控制的高對比） 一部分的原始檔控制中建立新的專案。  
  
|動作|測試步驟|若要確認預期的結果|  
|------------|----------------|--------------------------------|  
|繫結至空的位置|1.建立專案。<br />2.您可以將方案加入原始檔控制。<br />3.開啟**變更原始檔控制** 對話方塊 (**檔案**，**原始檔控制**，**變更原始檔控制**)。<br />4.按一下 **解除繫結**。<br />5.如果出現，請接受 [警告] 對話方塊。<br />6.選取所有項目。<br />7.按一下 **繫結**。<br />8.瀏覽至原始檔控制存放區中的空白位置。<br />9.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />10.按一下 **繼續使用這些繫結**確認對話方塊中。<br />11.按一下 **確定**在警告對話方塊中，如果有出現。<br />12.簽入所有項目。 如果這個步驟成功，則會繼續至下一個步驟。<br />13.從原始檔控制開啟方案，新的位置。|`Result from Step 12:`<br /><br /> 方案和專案繫結至並寫入至新的目標版本存放區中。<br /><br /> 簽入的方案和專案的檔案。<br /><br /> 版本存放區專案階層比對專案，在磁碟上的資料夾階層。<br /><br /> `Result from Step 13:`<br /><br /> 下載專案的所有項目。|  
|繫結至與用戶端同步的位置|1.建立專案。<br />2.您可以將方案加入原始檔控制。<br />3.版本存放區中建立方案和專案的複本 (共用以及建立分支，如果使用[!INCLUDE[vsvss](../../includes/vsvss-md.md)])。<br />4.開啟**變更原始檔控制** 對話方塊 (**檔案**，**原始檔控制**，**變更原始檔控制**)。<br />5.解除所有繫結。<br />6.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />7.重新開啟**變更原始檔控制** 對話方塊。<br />8.全選。<br />9.按一下 **繫結**。<br />10.瀏覽至方案和專案分支位置 （來自步驟 3）<br />11.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />12.取得最新的以遞迴方式的所有項目。|Get 之後 get 之前一樣，將檔案內容。|  
|繫結至與用戶端不同步的位置|1.建立專案。<br />2.您可以將方案加入原始檔控制。<br />3.版本存放區中建立方案和專案的複本 (共用以及建立分支，如果使用[!INCLUDE[vsvss](../../includes/vsvss-md.md)])。<br />4.修改版本存放區中分支的專案中的檔案。<br />5.開啟**變更原始檔控制** 對話方塊 (**檔案**，**原始檔控制**，**變更原始檔控制**)。<br />6.解除所有繫結。<br />7.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />8.重新開啟**變更原始檔控制** 對話方塊。<br />9.全選。<br />10.按一下 **繫結**。<br />11.瀏覽至分支方案和專案的位置。<br />12.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />13.如果出現，請接受 [警告] 對話方塊。<br />14.取得最新的遞迴的所有項目。|步驟 4 中已修改的檔案也會在本機修改。|  
|繫結是永遠不會在原始檔控制下的方案|1.原始檔控制中建立空的資料夾。<br />2.建立用戶端專案。<br />3.開啟**變更原始檔控制** 對話方塊 (**檔案**，**原始檔控制**，**變更原始檔控制**)。<br />4.將方案繫結至原始檔控制中的空白位置。<br />5.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />6.按一下 **繼續使用這些繫結**確認對話方塊中。<br />7.按一下 **確定**在警告對話方塊中，如果有出現。|方案會隨即加入至原始檔控制中。<br /><br /> 方案和專案簽出。|  
|取消繫結|1.建立專案。<br />2.您可以將方案加入原始檔控制。<br />3.開啟 [變更原始檔控制] 對話方塊。<br />4.解除所有繫結。<br />5.按一下 **確定**按鈕以關閉對話方塊。 如果這個步驟成功，則會繼續至下一個步驟。<br />6.重新開啟**變更原始檔控制** 對話方塊。<br />7.繫結至不相關的位置。<br />8.按一下 [取消]。|`Result from Step 5:`<br /><br /> 解決方案不會再受到原始檔控制<br /><br /> `Result from Step 8:`<br /><br /> 解決方案是仍不會在原始檔控制。|  
  
### <a name="case-5b-unbind"></a>案例 5b:解除繫結  
 解除繫結移除來源的程式碼從專案和其解決方案的控制項資訊。 受影響的專案和方案都根據使用者選取和方式的項目已加入至原始檔控制的混合。  
  
|動作|測試步驟|若要確認預期的結果|  
|------------|----------------|--------------------------------|  
|解除繫結包含一個檔案系統或本機 IIS Web 專案和一個用戶端專案的方案|1.建立檔案系統或本機 IIS Web 專案。<br />2.您可以將方案加入原始檔控制。<br />3.將新的用戶端專案加入方案。<br />4.如果出現提示時，請接受簽出的解決方案。<br />5.開啟**變更原始檔控制** 對話方塊。<br />6.按一下 **解除繫結**。<br />7.按一下 [確定]  關閉對話方塊。<br />8.嘗試簽出方案、 專案、 方案項目、 專案項目。|方案和專案不是原始檔控制之下。<br /><br /> 看不到原始檔控制 功能表命令。|  
|取消解除繫結|1.建立專案。<br />2.您可以將方案加入原始檔控制。<br />3.開啟**變更原始檔控制** 對話方塊。<br />4.按一下 **解除繫結所有**。<br />5.按一下 [取消]。|解決方案是在原始檔控制。|  
  
### <a name="case-5c-rebind"></a>案例 5 c:重新繫結  
 重新繫結是只要解除繫結和繫結的組合 — 的重新繫結專案/方案先前已在原始檔控制，而且已解除繫結程序。  
  
|動作|測試步驟|若要確認預期的結果|  
|------------|----------------|--------------------------------|  
|重新繫結方案和專案，不需關閉**變更原始檔控制**對話方塊|1.建立專案。<br />2.您可以將方案加入原始檔控制。<br />3.開啟**變更原始檔控制** 對話方塊。<br />4.按一下 **解除繫結**。<br />5.選取所有資料列。<br />6.按一下 **繫結**。<br />7.按一下 [ **[確定]** 以關閉**變更原始檔控制**] 對話方塊。<br />8.如果出現提示，請接受簽出。|方案和專案受到原始檔控制。|  
|只有未關閉的專案重新繫結**變更原始檔控制**對話方塊|1.建立專案。<br />2.只有專案加入原始檔控制使用 (檔案]-> [原始檔控制]-> [新增所選專案加入原始檔控制。<br />3.開啟 [變更原始檔控制] 對話方塊。<br />4.解除繫結的專案。<br />5.繫結的專案。|解決方案會維持未受控制的。<br /><br /> 專案會保留受控制的。|  
|只需關閉方案重新繫結**變更原始檔控制**對話方塊|1.建立專案。<br />2.將只有方案加入原始檔控制使用 (**檔案**，**原始檔控制**，**將所選專案加入至原始檔控制**。<br />3.開啟**變更原始檔控制** 對話方塊。<br />4.解除繫結的解決方案 (請不要關閉**變更原始檔控制** 對話方塊。)<br />5.繫結的解決方案。<br />6.按一下 [確定]  關閉對話方塊。<br />7.簽出方案和方案項目 （如果有的話）|解決方案會保留受控制的。<br /><br /> 專案會維持未受控制的。|  
|只有當相同的目錄中的方案/專案重新繫結|1.建立專案。<br />2.只有專案加入原始檔控制使用 (**檔案**，**原始檔控制**，**將所選專案加入至原始檔控制**。<br />3.關閉方案。<br />4.建立新的方案包含至少兩個專案。<br />5.您可以將方案加入原始檔控制。<br />6.加入在步驟 1 中建立從原始檔控制的專案。<br />7.如果出現提示，請接受簽出的解決方案。<br />8.簽入整個方案。<br />9.開啟**變更原始檔控制** 對話方塊。<br />10.選取 新增的專案 （來自步驟 6)，然後按一下**解除繫結**。<br />11.按一下 [確定]  關閉對話方塊。<br />12.如果出現提示，請接受簽出。<br />13.重新開啟**變更原始檔控制** 對話方塊。<br />14.選取 新增的專案 （來自步驟 6)，然後按一下**繫結**。<br />15.選取的原始位置。|方案和專案保持受控制的。|  
  
## <a name="see-also"></a>另請參閱  
 [原始檔控制外掛程式測試指南](../../extensibility/internals/test-guide-for-source-control-plug-ins.md)
