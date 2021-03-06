---
title: CommandPlacement 元素 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- CommandPlacements element (VSCT XML schema)
- VSCT XML schema elements, CommandPlacements
ms.assetid: 2cbd7ac8-c55a-43d8-a26d-713b3d790016
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 43fd417c4d54c0ab57133cf6dbff2c770c1ffc45
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58939333"
---
# <a name="commandplacement-element"></a>CommandPlacement 項目
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

CommandPlacement 元素可讓按鈕、 群組和包含在一個以上的群組或功能表的功能表。 藉由使用 CommandPlacement 元素，您不必完全重新定義這些項目，若要修改的使用者介面外觀。  
  
 如需詳細資訊，請參閱 <<c0> [ 建立可重複使用群組的按鈕](../extensibility/creating-reusable-groups-of-buttons.md)。  
  
## <a name="syntax"></a>語法  
  
```  
<CommandPlacement guid=guidMyCommandSet" id="MyCommand" priority="0x001" >  
  <Parent>... </Parent>  
</CommandPlacement>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|guid|必要項。 中所定義的命令集的 guid [Symbols 元素](../extensibility/symbols-element.md)。|  
|id|必要項。 功能表、 群組或放置時，如中所定義的命令識別碼`Symbols Element`。|  
|priority|必要項。 判斷項目在其父項目中的視覺位置。|  
|條件|選擇性。 請參閱[條件式屬性](../extensibility/vsct-xml-schema-conditional-attributes.md)。|  
  
### <a name="child-elements"></a>子元素  
  
|項目|描述|  
|-------------|-----------------|  
|父代|必要項。 功能表或裝載要放置的項目群組中。|  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[CommandPlacements 元素](../extensibility/commandplacements-element.md)|指定 CommandPlacements 和 CommandPlacement 元素的群組。|  
  
## <a name="example"></a>範例  
  
```  
<CommandPlacements>  
  <CommandPlacement guid="guidWidgetPackage" id="cmdidInsertOptions"  
    priority="0x0300">  
    <Parent guid="cmdGuidWidgetCommands" id="menuIDEditWidget"/>  
  </CommandPlacement>  
</CommandPlacements>  
```  
  
## <a name="see-also"></a>另請參閱  
 [CommandPlacements 元素](../extensibility/commandplacements-element.md)   
 [Visual Studio 命令表檔案 (.Vsct)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
