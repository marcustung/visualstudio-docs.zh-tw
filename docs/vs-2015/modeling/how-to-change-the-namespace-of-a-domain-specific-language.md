---
title: HOW TO：變更定義域專屬語言命名空間 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, namespace
ms.assetid: f20c47e5-230d-4f0e-812f-5c6edb86866c
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 57ec75ec116b3b107b01a139621d3c59ca8ecac9
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094907"
---
# <a name="how-to-change-the-namespace-of-a-domain-specific-language"></a>HOW TO：變更特定領域語言的命名空間
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

您可以變更特定領域語言的命名空間。 您必須進行的變更**DSL explorer**、 Dsl 封裝專案屬性，以及組件資訊。  
  
### <a name="to-change-the-namespace-of-a-domain-specific-language"></a>若要變更的特定領域語言命名空間  
  
1. 在  **DSL Explorer**，按一下**Dsl**節點。  
  
2. 在 **屬性**視窗中，變更**命名空間**屬性。  
  
3. 儲存方案，並轉換範本。  
  
4. 在 **專案**功能表上，按一下**Dsl 屬性**。  
  
     您的專案的屬性會出現。  
  
5. 按一下 [應用程式]  索引標籤。  
  
6. 變更**預設命名空間**屬性設為新的命名空間名稱。  
  
7. 如果您也想要變更的組件名稱，變更**組件名稱屬性。**  
  
8. 如果您已變更的組件名稱，請開啟 DslPackage\Package.tt，並更新這一行：  
  
     `string dslAssembly = "YourDSLassembly.Dsl.dll";`  
  
9. 如果您已撰寫的自訂程式碼，確定變更程式碼檔案中的命名空間和類別的參考。  
  
10. 重設 Visual Studio 實驗執行個體。  
  
    1. 刪除**\Users\\**_{name}_**\AppData\Local\Microsoft\VisualStudio\\\*Exp**  
  
    2. 在 Windows 上**開始**功能表上，選擇**所有程式**， **Microsoft Visual Studio 2010 SDK**，**工具**，**重設實驗執行個體**。  
  
11. 在 **建置**功能表上，選擇**重建方案**。  
  
## <a name="see-also"></a>另請參閱  
 [Domain-Specific Language Tools Glossary](http://msdn.microsoft.com/ca5e84cb-a315-465c-be24-76aa3df276aa) (特定領域語言工具字彙表)
