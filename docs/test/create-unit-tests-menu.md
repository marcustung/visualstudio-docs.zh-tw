---
title: 建立單元測試方法虛設常式
ms.date: 04/01/2019
ms.topic: conceptual
helpviewer_keywords:
- unit testing, create unit tests
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e7eb72f104560991f1bb191e62641041879df071
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2019
ms.locfileid: "58857719"
---
# <a name="create-unit-test-method-stubs-with-the-create-unit-tests-command"></a>使用建立單元測試命令來建立單元測試方法虛設常式

**Create Unit Tests** 命令可建立單元測試方法 Stub。 此功能允許輕鬆設定測試專案、測試類別，以及其內的測試方法虛設常式。

> [!NOTE]
> [建立單元測試] 功能表命令僅供以 .NET Framework 為目標 (非 .NET Core) 的受控程式碼使用。

[建立單元測試] 功能表命令可延伸，並可用來產生 MSTest、MSTest V2、NUnit 和 xUnit 測試。

## <a name="get-started"></a>開始使用

若要開始，請以滑鼠右鍵按一下您想要測試之專案程式碼編輯器中的方法、類型或命名空間，然後選擇 [建立單元測試]。 [建立單元測試] 對話方塊隨即開啟，您可以在此設定想要建立的測試方式。

![使用建立單元測試命令](media/createunittestcommand.png)

## <a name="set-unit-test-traits"></a>設定單元測試特性

如果您計劃執行這些測試作為測試自動化程序的一部分，則可能會考慮在另一個測試專案中建立測試 (上述對話方塊中的第二個選項)，以及設定單元測試的單元測試特性。 這可讓您更輕鬆地包含或排除這些特定測試作為持續整合或持續部署管線的一部分。 特性是透過直接將中繼資料新增至單元測試所設定，如下所示。

![設定單元測試特性](media/createunittest.png)

## <a name="use-third-party-unit-test-frameworks"></a>使用協力廠商單元測試架構

若要自動產生 NUnit 或 xUnit 的單元測試，請從 Visual Studio Marketplace 安裝下列其中一個測試架構延伸模組：

* [測試產生器的 NUnit 延伸模組](https://marketplace.visualstudio.com/items?itemName=NUnitDevelopers.TestGeneratorNUnitextension)
* [測試產生器的 xUnit.net 延伸模組](https://marketplace.visualstudio.com/items?itemName=BradWilson.xUnitnetTestExtensions)

## <a name="when-should-i-use-this-feature"></a>何時應該使用這項功能？

每當您需要建立單元測試，特別是當您要測試僅有少量或沒有測試涵蓋範圍，且沒有文件的現有程式碼時，請使用此功能。 換句話說，其中具有有限或不存在的程式碼規格。 它會有效地實作與[類似的方法](https://devblogs.microsoft.com/devops/introducing-smart-unit-tests/)，描述觀察到的程式碼行為特性。

不過，這項功能也同樣適用於開發人員開始撰寫一些程式碼，並用它啟動單元測試的情況。 在編碼流程內，開發人員可能想要快速建立特定程式碼片段的單元測試方法 Stub (具有適當的測試類別和測試專案)。

## <a name="see-also"></a>另請參閱

- [使用 [建立單元測試] 建立單元測試方法 Stub](https://devblogs.microsoft.com/devops/creating-unit-test-method-stubs-with-create-unit-tests/)
- [單元測試部落格文章](https://devblogs.microsoft.com/devops/?s=unit+testing)
