---
title: 自訂 infopath 的功能區
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- InfoPath [Office development in Visual Studio], Ribbon
- Ribbon [Office development in Visual Studio], InfoPath
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: bdd39b0ffa59342df669fa619ea5a86a41cef79b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602230"
---
# <a name="customize-a-ribbon-for-infopath"></a>自訂 infopath 的功能區
  當您在 Microsoft Office InfoPath 自訂功能區時，您必須考慮自訂功能區在應用程式中出現的位置。 [!INCLUDE[InfoPath_14_short](../vsto/includes/infopath-14-short-md.md)] 可以在下列三種 InfoPath 應用程式視窗中顯示功能區：

- 顯示在設計模式中開啟表單範本的視窗。

- 根據表單範本來顯示表單的視窗。

- 預覽列印視窗。

  **適用於：** 本主題中的資訊適用於 InfoPath 2010 的 VSTO 增益集專案。 如需詳細資訊，請參閱 <<c0> [ 依 Office 應用程式和專案類型提供的功能](../vsto/features-available-by-office-application-and-project-type.md)。

  使用者和設計人員會在設計模式開啟表單範本來修改範本的外觀和版面配置。 使用者開啟以表單範本為基礎的表單來加入內容。

  [預覽列印] 視窗可讓設計人員和使用者在列印前預覽表單或表單範本的頁面。

> [!NOTE]
>  [增益集]  索引標籤不會出現在 [預覽列印] 視窗。 如果您想要在 [預覽列印] 視窗中顯示自訂索引標籤，請確定索引標籤的 [OfficeId]  屬性未設定為 [TabAddIns] 。

 您必須指定每個要讓功能區出現在其中的視窗之功能區類型。

## <a name="specify-the-ribbon-type-in-the-ribbon-designer"></a>在 功能區設計工具中指定功能區類型
 如果您使用**功能區 （視覺化設計工具）** 項目，按一下**RibbonType**屬性中的功能區**屬性** 視窗中，然後選取任何功能區 Id下表所述。

|功能區 ID|當您執行專案時，會出現功能區的視窗|
|---------------|---------------------------------------------------------------------|
|**Microsoft.InfoPath.Designer**|顯示在設計模式中開啟表單範本的視窗。|
|**Microsoft.InfoPath.Editor**|根據表單範本來顯示表單的視窗。|
|**Microsoft.InfoPath.PrintPreview**|預覽列印視窗。|

 您可以加入多個功能區至專案。 如果有多個功能區共用功能區 ID，請覆寫在應用程式 `ThisAddin` 類別中的 `CreateRibbonExtensibilityObject` 方法，以指定要在執行階段顯示哪個功能區。 如需詳細資訊，請參閱 <<c0> [ 功能區概觀](../vsto/ribbon-overview.md)。

## <a name="specify-the-ribbon-type-by-using-ribbon-xml"></a>使用功能區 XML 來指定功能區類型
 如果您使用**功能區 (XML)** 項目，請檢查值*ribbonID*中的參數<xref:Microsoft.Office.Core.IRibbonExtensibility.GetCustomUI%2A>方法，並傳回適當的功能區。

 <xref:Microsoft.Office.Core.IRibbonExtensibility.GetCustomUI%2A> 方法會在功能區程式碼檔案中由 Visual Studio 自動產生。 *ribbonID* 參數是字串，用以識別 InfoPath 視窗中正開啟的類型。

 下列程式碼範例示範如何只在會顯示設計模式中表單範本的視窗中顯示自訂功能區。 要顯示的功能區會在 `GetResourceText()` 方法中指定，這是在功能區類別中產生的。 如需功能區類別的詳細資訊，請參閱 [Ribbon XML](../vsto/ribbon-xml.md)。

 [!code-csharp[Trin_RibbonInfoPathBasic#1](../vsto/codesnippet/CSharp/myinfopathproject/ribbon.cs#1)]
 [!code-vb[Trin_RibbonInfoPathBasic#1](../vsto/codesnippet/VisualBasic/myinfopathproject/ribbon.vb#1)]

## <a name="see-also"></a>另請參閱
- [在執行階段功能區的存取](../vsto/accessing-the-ribbon-at-run-time.md)
- [功能區概觀](../vsto/ribbon-overview.md)
- [功能區設計工具](../vsto/ribbon-designer.md)
- [Ribbon XML](../vsto/ribbon-xml.md)
