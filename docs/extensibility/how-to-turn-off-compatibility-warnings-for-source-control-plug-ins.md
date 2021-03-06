---
title: 關閉原始檔控制外掛程式的相容性警告 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control plug-ins, turning off compatibility warnings
- compatibility warnings, turning off
ms.assetid: ba318e12-921b-4b7a-a8c2-12c712be1dbf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a1a113dc3b4a4b3a8a4482dd092878851d740c6e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60112199"
---
# <a name="how-to-turn-off-compatibility-warnings-for-source-control-plug-ins"></a>HOW TO：關閉原始檔控制外掛程式的相容性警告
使用者可能會採用原始檔控制中的看到數個相容性警告[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]。 顯示警告取決於原始檔控制外掛程式的功能，並且可以停用，如此處所示詳細。

### <a name="to-disable-the-warning-to-ensure-optimal-source-control-integration-with-visual-studio"></a>若要停用警告：「 若要確保最佳的原始檔控制整合，使用 Visual Studio"

- 設定下列登錄項目 （如有必要，請新增此值）：

   **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\DontDisplayCheckDotNETCompatible = dword: 00000001**

   這個警告會顯示所有非[!INCLUDE[vsvss](../extensibility/includes/vsvss_md.md)]外掛程式。

### <a name="to-disable-the-warning-the-installed-source-control-provider-does-not-support-all-the-capabilities"></a>若要停用警告：「 已安裝的原始檔控制提供者不支援所有功能 」

- 設定下列兩個登錄值 （如有必要，請加入的值）：

     **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\WarnedOldMSSCCIProvider = dword:00000000**

    **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\8.0\SourceControl\UseOldSCC = dword:00000001**

     如果原始檔控制外掛程式未明確支援重新進入的多個專案 （也就是如果它可以檢查只有一個檔案和專案中，一次），則會顯示此警告。

     建議您最好支援重新進入 (`SCC_CAP_REENTRANT`功能); 這麼做會移除這個警告。 不過，如果這項支援不可行，就可以設定這些登錄項目。

## <a name="see-also"></a>另請參閱
- [功能旗標](../extensibility/capability-flags.md)