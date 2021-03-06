---
title: 篩選巢狀專案的 AddItem 對話方塊 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- filtering, nested projects
- nested projects, AddItem dialog box filtering
ms.assetid: 5b3e352e-7f18-4f66-be16-b0ad55637ce5
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 38b56753bfc56a1143d8c5423ddf7714f0b2f21e
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56606026"
---
# <a name="filter-the-additem-dialog-box-for-nested-projects"></a>篩選巢狀專案的 AddItem 對話方塊
當您顯示**AddItem**巢狀的專案時，父專案的對話方塊可以控制哪些項目會顯示在對話方塊中。

 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFilterAddProjectItemDlg2>介面可讓您篩選會在節點**AddItem**  對話方塊。 當子專案不會顯示**AddItem**  對話方塊中，可以實作父系`IVsFilterAddProjectItemDlg`介面和篩選器會顯示子系的專案中的項目。

 當專案會依特定父專案下的函式時，您可以實作`IVsFilterAddProjectItemDlg`當使用者選取**加入專案項目**中巢狀專案的捷徑功能表上。 實作`IvsFilterAddProjectItemDlg displays`只有專案項目，或專屬於該群組的檔案。 其他群組的專案項目會濾除對話方塊中，即使它們儲存在相同的目錄。

 當使用者在開啟**AddItem**對話方塊中，子系，父專案的實作`IVsFilterAddProjectItemDlg`介面稱為。

 `IVsFilterAddProjectItemDlg`介面也可以實作依類別篩選。 如需詳細資訊，請參閱 <<c0> [ 項目加入 [加入新項目] 對話方塊中](../../extensibility/internals/adding-items-to-the-add-new-item-dialog-boxes.md)並[註冊專案和項目範本](../../extensibility/internals/registering-project-and-item-templates.md)。

## <a name="see-also"></a>另請參閱
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsFilterAddProjectItemDlg2>
- [將項目新增至 [加入新項目] 對話方塊](../../extensibility/internals/adding-items-to-the-add-new-item-dialog-boxes.md)
- [註冊專案和項目範本](../../extensibility/internals/registering-project-and-item-templates.md)
- [巢狀專案](../../extensibility/internals/nesting-projects.md)