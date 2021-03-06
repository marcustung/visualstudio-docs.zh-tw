---
title: 程式碼分析問題疑難排解
ms.date: 11/04/2016
ms.topic: troubleshooting
ms.assetid: 61c7e44d-2780-4df5-9bcb-49e40c1152fc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 936428b82e721a1df6003a4bb0eecefe5b696b4c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60079995"
---
# <a name="troubleshooting-code-analysis-issues"></a>程式碼分析問題疑難排解
本主題包含下列 Visual Studio 程式碼分析問題的疑難排解資訊。

- [舊版 Visual Studio 不會反映 Visual Studio 2010 規則集變更](#ChildRuleSetChangesInPreviousVersions)

## <a name="ChildRuleSetChangesInPreviousVersions"></a> 舊版 Visual Studio 不會反映 Visual Studio 2010 規則集變更
 當您在 [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] 中建立包含子規則集的規則集時，於使用舊版 Visual Studio 的電腦上，子規則集變更可能不會套用至程式碼分析回合。 若要解決此問題，您必須強制重寫父代規則集 (即包含子規則集的規則集)。

1. 在 [!INCLUDE[vs_dev10_long](../code-quality/includes/vs_dev10_long_md.md)] 中，開啟父代規則集。

2. 進行變更 (例如新增或移除規則)，然後儲存規則集。

3. 重新開啟規則集，並回復變更，然後重新儲存規則集。

## <a name="see-also"></a>另請參閱

- [分析應用程式品質](../code-quality/code-analysis-for-managed-code-overview.md)
- [分析 Managed 程式碼品質](../code-quality/code-analysis-for-managed-code-overview.md)
- [使用規則集分組程式碼分析規則](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)