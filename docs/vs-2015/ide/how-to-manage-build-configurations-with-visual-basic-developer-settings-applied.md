---
title: 如何：在套用 Visual Basic 開發者設定的情況下管理組建組態 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio, building with Visual Basic settings
- MSBuild, debug build
- advanced build configurations
- building with Visual Basic developer settings
- debug builds
- MSBuild, release build
- release builds
ms.assetid: eaea6e0b-6c61-4869-8d63-d372c745a23c
caps.latest.revision: 11
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0b0587f6c1c5d7577d8fddffb73db31f09248fae
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60075645"
---
# <a name="how-to-manage-build-configurations-with-visual-basic-developer-settings-applied"></a>如何：在套用 Visual Basic 開發者設定的情況下管理組建組態
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

根據預設，所有進階組建組態選項會隱藏，並套用 [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] Developer 設定。 本主題說明如何手動啟用這些設定。  
  
## <a name="enabling-advanced-build-configurations"></a>啟用進階組建組態  
 根據預設，[!INCLUDE[vbprvb](../includes/vbprvb-md.md)] Developer 設定會隱藏開啟 [Configuration Manager] 對話方塊和[專案設計工具](http://msdn.microsoft.com/898dd854-c98d-430c-ba1b-a913ce3c73d7)中的 [組態] 和 [平台] 清單的選項。  
  
#### <a name="to-enable-advanced-build-configurations"></a>啟用進階組建組態  
  
1. 在 [ **工具** ] 功能表上按一下 [ **選項**]。  
  
2. 展開 [專案和方案]，然後按一下 [一般]。  
  
    > [!NOTE]
    >  即使未核取 [顯示所有設定] 選項，都可以看到 [一般] 節點。 如果您想要查看每個可用的選項，請按一下 [顯示所有設定]。  
  
3. 按一下 [顯示進階組建組態]。  
  
4. 按一下 [確定]。  
  
     在 [組建] 功能表上，現在已可使用 [Configuration Manager]，而且 [組態] 和 [平台] 清單也會顯示在專案設計工具中。  
  
## <a name="see-also"></a>請參閱  
 [了解組建組態](../ide/understanding-build-configurations.md)   
 [編譯和建置](../ide/compiling-and-building-in-visual-studio.md)
