---
title: IDE 定義的命令、 功能表和群組 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- commands, environment-defined
- .vsct files, environment-defined constants
- command groups, environment-defined
ms.assetid: 86b3af13-7163-48c6-986b-7beeedbc26cc
caps.latest.revision: 28
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 32e8135328c11fd74311371d07645a525426371e
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58945651"
---
# <a name="ide-defined-commands-menus-and-groups"></a>IDE 定義的命令、功能表和群組
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

許多的功能表、 命令和命令群組已經定義以供[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]IDE。 當您擴充時，還有可供您使用這些命令[!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]。  
  
## <a name="finding-environment-defined-commands"></a>尋找環境定義的命令  
 一組四個.vsct 檔案中定義的環境命令：  
  
- SharedCmdDef.vsct  
  
- SharedCmdPlace.vsct  
  
- ShellCmdDef.vsct  
  
- ShellCmdPlace.vsct  
  
  這些檔案位於 *\<Visual Studio SDK 安裝路徑 >* \VisualStudioIntegration\Common\Inc\\。 這些檔案提供的定義與功能表和群組，您可以使用 VSPackage 的命令資料表 (.vsct) 的組態檔中做為容器為您自己的功能表、 群組和命令的 Guid。  
  
## <a name="in-this-section"></a>本節內容  
 [Visual Studio 功能表的 GUID 和 ID](../../extensibility/internals/guids-and-ids-of-visual-studio-menus.md)  
 提供在 Visual Studio 功能表列上的功能表和其所包含的群組的 GUID 和 ID 值。  
  
 [Visual Studio 工具列的 GUID 和 ID](../../extensibility/internals/guids-and-ids-of-visual-studio-toolbars.md)  
 提供在 Visual Studio IDE 中，工具列和其所包含的群組的 GUID 和 ID 值。  
  
 [Visual Studio 命令的 GUID 和 ID](../../extensibility/internals/guids-and-ids-of-visual-studio-commands.md)  
 提供 Visual Studio IDE 所定義的命令 GUID 和 ID 的值。  
  
## <a name="see-also"></a>另請參閱  
 [Visual Studio 命令資料表 (。Vsct) 檔案](../../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)   
 [IDE 定義的命令，來擴充專案系統](../../extensibility/internals/ide-defined-commands-for-extending-project-systems.md)   
 [VSPackage 如何新增使用者介面元素](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)
