---
title: 開啟和儲存專案項目 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- projects [Visual Studio SDK], file persistence
- files [Visual Studio], opening and saving
- editors [Visual Studio SDK], file persistence
ms.assetid: f71898ad-335f-4c43-a177-4da87078afd1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7ca83cb6d2913e0c0a91f4a6e874640ae57c7708
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602425"
---
# <a name="opening-and-saving-project-items"></a>開啟和儲存專案項目
當您新增新的專案類型時，您必須管理的開啟和儲存您的專案檔案中[!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]整合式的開發環境 (IDE)。 下列主題討論不同的方法，來開啟和儲存檔案。

## <a name="in-this-section"></a>本節內容
- [使用開啟檔案命令顯示檔案](../../extensibility/internals/displaying-files-by-using-the-open-file-command.md)

 提供 IDE 的處理方式的逐步說明**開啟檔案**命令，並在回應此命令的專案的角色。

- [使用開啟方式命令顯示檔案](../../extensibility/internals/displaying-files-by-using-the-open-with-command.md)

 提供 IDE 的處理方式的詳細的逐步說明**開啟**命令，提示檔案具有一些選擇的標準編輯器開啟。

- [如何：開啟專案特定的編輯器](../../extensibility/how-to-open-project-specific-editors.md)

 提供逐步指示，來指定，應該使用專案特定編輯器中開啟專案中的特定類型的檔案。

- [如何：開啟標準編輯器](../../extensibility/how-to-open-standard-editors.md)

 提供逐步指示，來指定如何啟用 IDE 中您的專案類型開啟檔案的標準編輯器。

- [如何：開啟編輯器開啟的文件](../../extensibility/how-to-open-editors-for-open-documents.md)

 提供逐步指示，開啟專案特定的編輯器開啟的檔案。

- [儲存標準文件](../../extensibility/internals/saving-a-standard-document.md)

 提供 IDE 的處理方式的詳細的說明**儲存**，**另存新檔**，並**全部儲存**標準編輯器中開啟的文件的命令。

- [儲存自訂文件](../../extensibility/internals/saving-a-custom-document.md)

 提供的圖表和詳細的說明如何處理 IDE**儲存**，**另存新檔**，並**全部儲存**在自訂編輯器中開啟的文件的命令。

- [決定要開啟專案中檔案的編輯器](../../extensibility/internals/determining-which-editor-opens-a-file-in-a-project.md)

 討論 IDE 來選取適當的編輯器或設計工具檔案會遵循的程序。

## <a name="related-sections"></a>相關章節
- [建立自訂編輯器和設計工具](../../extensibility/creating-custom-editors-and-designers.md)

 列出四種類型的編輯器在 IDE 可以裝載，並提供每個編輯器的說明。

- [專案類型](../../extensibility/internals/project-types.md)

 討論專案如何控制的程式碼進行編譯和建置的方式、 如何開啟編輯器，以及如何格式化專案項目。