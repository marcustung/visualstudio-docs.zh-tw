---
title: 巢狀專案的精靈支援 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Add Item wizard
- nested projects, wizard support
- New Project wizard
ms.assetid: 1b496acc-b326-4cdb-bb48-e3b5c6f12e05
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6fd9871e794c2968bab3effce0717ea1cae508eb
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56603959"
---
# <a name="wizard-support-for-nested-projects"></a>巢狀專案的精靈支援
IDE 執行兩個可實作巢狀專案的父專案的精靈：**新的專案**精靈並**加入項目**精靈。

 如果使用者啟動**新的專案**精靈選取**新增專案**，然後按一下**新專案**[檔案] 功能表上，或藉由選取**新增**然後按一下滑鼠右鍵**新的專案**在 [方案總管] 中，IDE 會執行**AddProject**命令和父專案的實作**AddProject**命令會傳回範本專案檔中或具有一組內容參數的精靈 (.vsz) 檔案。

 同樣地，父專案的實作**AddItem**精靈會傳回具有一組不同的內容參數的.vsz 檔案。

 如需有關精靈的詳細資訊，請參閱[精靈 (。在 Vsz) 檔案](../../extensibility/internals/wizard-dot-vsz-file.md)，[內容參數](../../extensibility/internals/context-parameters.md)並[註冊專案和項目範本](../../extensibility/internals/registering-project-and-item-templates.md)。

## <a name="see-also"></a>另請參閱
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy>
- [巢狀專案](../../extensibility/internals/nesting-projects.md)