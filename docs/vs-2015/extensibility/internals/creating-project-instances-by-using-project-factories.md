---
title: 使用 Project Factory 建立專案執行個體 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- project factories
- projects [Visual Studio SDK], project factories
ms.assetid: 94c90012-8669-459c-af8e-307ac242c8c4
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: b33d5d1a09425a18f0c9489b15147e3355e45c99
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58941541"
---
# <a name="creating-project-instances-by-using-project-factories"></a>使用專案 Factory 建立專案執行個體
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

專案中的型別[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]使用*project factory*建立專案物件的執行個體。 專案的處理站是類似於標準的 class factory cocreatable COM 物件。 不過，專案物件不是 cocreatable： 只可以建立使用 project factory。  
  
 [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] IDE 呼叫 project factory 實作 VSPackage 中，當使用者載入現有的專案，或建立新的專案中[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]。 新的專案物件會提供 IDE，具有足夠的資訊填入 [方案總管] 中。 新的專案物件也會提供必要的介面以支援由 IDE 所起始的所有相關 UI 動作。  
  
 您可以實作<xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory>中您的專案中的類別介面。 一般而言，它位於自己的模組。  
  
 如需實作的範例`IVsProjectFactory`介面，請參閱包含在 PrjFac.cpp[基本專案](http://msdn.microsoft.com/385fd2a3-d9f1-4808-87c2-a3f05a91fc36)範例目錄。  
  
 專案，支援彙總的擁有者必須保存在其專案檔中的擁有者金鑰。 當<xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CreateProject%2A>專案呼叫方法，是將它與擁有者索引鍵，擁有的專案會將其擁有者索引鍵轉換成 GUID 然後呼叫專案 factory`CreateProject`要實際建立此專案處理站的方法。  
  
## <a name="creating-an-owned-project"></a>建立擁有的專案  
 擁有者會建立一個擁有的專案，在兩個階段：  
  
1. 藉由呼叫<xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory.PreCreateForOwner%2A>方法。 這可讓擁有的專案有機會建立彙總的 project 物件根據輸入控制`IUnknown`。 擁有的專案通過內部`IUnknown`和彙總的物件傳回至擁有者專案。 這可讓擁有的專案有機會儲存內部`IUnknown`。  
  
2. 藉由呼叫<xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory.InitializeForOwner%2A>方法。 擁有的專案沒有所有其具現化，而不是呼叫呼叫此方法時`IVsProjectFactory::CreateProject`不屬於專案的情況也是一樣。 輸入`VSOWNEDPROJECTOBJECT`列舉型別通常是彙總的擁有的專案。 擁有的專案可以使用這個變數來判斷是否已建立其專案物件 （cookie 不等於 NULL） 或必須建立 （cookie 等於 NULL）。  
  
   唯一的專案 GUID，類似於 cocreatable 的 COM 物件的 CLSID 來識別專案類型。 一般而言，雖然它可讓一個專案 factory 建立的單一專案類型的執行個體的一個專案 factory 控點會處理多個專案類型 GUID。  
  
   與特定的副檔名相關聯的專案類型。 當使用者嘗試開啟現有的專案檔案，或嘗試藉由複製範本建立新的專案時，則 IDE 會使用檔案副檔名來判斷對應的專案 GUID。  
  
   IDE 判斷它是否必須建立新的專案，或開啟現有的專案特定的類型，因為 IDE 使用資訊 [HKEY_LOCAL_MACHINE\Software\Microsoft\VisualStudio\8.0\Projects] 下的系統登錄中找出哪個VSPackage 實作必要的 project factory。 IDE 會載入此 VSPackage。 在 <xref:Microsoft.VisualStudio.Shell.Interop.IVsPackage.SetSite%2A>方法中，VSPackage 必須藉由呼叫與 IDE 中註冊其專案 factory<xref:Microsoft.VisualStudio.Shell.Interop.IVsRegisterProjectTypes.RegisterProjectType%2A>方法。  
  
   主要方法`IVsProjectFactory`介面是<xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory.CreateProject%2A>這應該處理兩種案例： 開啟現有的專案，並建立新的專案。 大多數專案的專案將其狀態儲存在專案檔中。 一般而言，建立新專案所進行的範本檔案的複本傳遞至`CreateProject`方法，然後開啟 的副本。 現有的專案由具現化直接開啟專案檔傳遞至`CreateProject`方法。 `CreateProject`方法可以視需要對使用者顯示其他 UI 功能。  
  
   專案可以也使用任何檔案，相反地，其專案將狀態儲存在檔案系統，例如資料庫或 Web 伺服器以外的儲存體機制。 在此情況下，檔案名稱參數傳遞至`CreateProject`方法不是實際檔案系統路徑，而唯一字串 — URL，以識別專案資料。 您不需要將傳遞至範本檔案複製`CreateProject`觸發要執行的適當建構順序。  
  
## <a name="see-also"></a>另請參閱  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsOwnedProjectFactory>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectFactory>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsRegisterProjectTypes>   
 [檢查清單：建立新的專案類型](../../extensibility/internals/checklist-creating-new-project-types.md)
