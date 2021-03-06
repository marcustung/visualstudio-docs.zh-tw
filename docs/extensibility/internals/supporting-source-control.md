---
title: 支援原始檔控制 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], supporting
ms.assetid: 567acde3-354e-4f39-8d99-0ef86c103396
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 35fb66927272435e773dbaee44019103892b028d
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56616985"
---
# <a name="supporting-source-control"></a>支援原始檔控制
[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] 支援檔案簽出、 簽入，並為您的專案或編輯器的其他原始檔控制作業。 原始檔控制用戶端，作為[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]設計成與原始檔控制封裝時，這類互動[!INCLUDE[vsvss](../../extensibility/includes/vsvss_md.md)]，可保存、 版本控制，與以動態方式定義的一組檔案的控制等機能。

## <a name="in-this-section"></a>本節內容
- [原始檔控制套件的模型](../../extensibility/internals/model-for-source-control-packages.md)

 描述專案型別必須實作的介面來支援原始檔控制。

- [設計決策](../../extensibility/internals/source-control-design-decisions.md)

 提供的問題的答案可讓您變更專案類型的實作方式。

- [組態詳細資料](../../extensibility/internals/source-control-configuration-details.md)

 描述如何變更支援原始檔控制專案類型的實作。

- [專案和編輯器適用的其他方針](../../extensibility/internals/additional-source-control-guidelines-for-projects-and-editors.md)

 討論專案類型和編輯器的最佳做法。

- [執行階段詳細資料](../../extensibility/internals/source-control-runtime-details.md)

 說明如何註冊的專案，當使用者將其新增至原始檔控制系統。

## <a name="reference"></a>參考資料
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsQueryEditQuerySave2> 表示檔案是在記憶體中變更或儲存的原始檔控制封裝的環境。

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2> 可讓專案和階層來自行註冊與原始檔控制，並取得原始檔控制狀態的相關資訊。

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2> 在專案檔和專案項目提供原始檔控制的專案系統中實作。

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocuments2> 由專案使用查詢來加入、 移除或重新命名檔案或目錄，在方案中的權限的環境。

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsTrackProjectDocumentsEvents2> 通知用戶端的專案檔案或目錄所做的變更。

## <a name="related-sections"></a>相關章節
- [專案類型](../../extensibility/internals/project-types.md)

 提供專案的概觀，做為基本建置組塊的[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]整合式的開發環境 (IDE)。 說明專案如何控制建置和編譯程式碼的其他主題會提供連結。