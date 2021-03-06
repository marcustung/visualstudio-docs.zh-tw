---
title: Combo 元素 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
helpviewer_keywords:
- Combos element (VSCT XML schema)
- VSCT XML schema elements, Combos
ms.assetid: 392e3063-f0a0-4130-9583-23bd2aa3fa36
caps.latest.revision: 12
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: daa89266d653743a743f42e5f0b8e11c954adc1a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944589"
---
# <a name="combo-element"></a>Combo 項目
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

定義會出現在下拉式方塊中的命令。 有四種下拉式方塊，如下所示：下拉式組合、 DynamicCombo、 IndexCombo 和 MRUCombo。  
  
## <a name="syntax"></a>語法  
  
```  
<combo guid="guidMyCommandSet" id="MyCommand" defaultWidth="20" idCommandList="MyCommandListID" priority="0x102" type="DropDownCombo">  
  <Parent>... </Parent  
  <CommandFlag>... </CommandFlag>  
  <Strings>... </Strings>  
</combo>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列各節描述屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|guid|必要項。 GUID/識別碼命令識別碼的 GUID。|  
|id|必要項。 GUID/識別碼的命令識別項的識別碼。|  
|defaultWidth|必要項。 指定下拉式方塊的像素寬度的整數。|  
|idCommandList|必要項。 擷取要顯示在下拉式方塊中的項目清單傳送至作用中的命令目標識別碼。 識別碼會在相同的 GUID 範圍內，做為控制項。|  
|priority|選擇性。 數值，指定的優先權。|  
|類型|選擇性。 列舉的值，指定的按鈕類型。<br /><br /> 如果未指定，會使用按鈕。<br /><br /> DropDownCombo<br /> VSPackage 是負責填入這個下拉式方塊的內容。 使用者無法將任何項目在這個下拉式表單的文字方塊中輸入。<br /><br /> DynamicCombo<br /> VSPackage 是負責填入這個下拉式方塊的內容。 使用者可以編輯此組合，並也在其中選取項目。<br /><br /> IndexCombo<br /> 只是它的 DynamicCombo 相同引發項目，而不是它的文字的索引。<br /><br /> MRUCombo<br /> 填入代表 VSPackage 的整合式的開發環境 (IDE)。  使用者可以編輯此下拉式方塊中。 IDE 會記住最多每下拉式方塊的最後 16 個項目。<br /><br /> 當使用者在下拉式方塊中，選取的項目，或輸入新的項目時，則 IDE 會通知適當的 VSPackage。|  
|條件|選擇性。 請參閱[條件式屬性](../extensibility/vsct-xml-schema-conditional-attributes.md)。|  
  
### <a name="child-elements"></a>子元素  
  
|項目|描述|  
|-------------|-----------------|  
|父代|選擇性。 按鈕的父項目。|  
|CommandFlag|必要項。 請參閱[命令旗標項目](../extensibility/command-flag-element.md)。 CommandFlag 按鈕有效值，如下所示。<br /><br /> -CaseSensitive<br /><br /> -CommandWellOnly<br /><br /> -DefaultDisabled<br /><br /> -DefaultInvisible<br /><br /> -DynamicVisibility<br /><br /> -篩選鍵<br /><br /> - IconAndText<br /><br /> -NoAutoComplete<br /><br /> -NoButtonCustomize<br /><br /> -NoCustomize<br /><br /> -NoKeyCustomize<br /><br /> -StretchHorizontally|  
|字串|必要項。 請參閱[字串項目](../extensibility/strings-element.md)。 必須定義子 ButtonText 元素。|  
|註釋|選擇性註解。|  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[Commands 元素](../extensibility/commands-element.md)|表示 [VSPackage] 工具列上的命令的集合。|  
  
## <a name="example"></a>範例  
  
```  
<Combo guid="guidWidgetPackage" id="cmdidInsertOptions"  
  defaultWidth="100" idCommandList="cmdidGetInsertOptionsList">  
  <CommandFlag>DynamicVisibility</CommandFlag>  
  <Strings>  
    <ButtonText>Select Insert Options</ButtonText>  
  </Strings>  
</Combo>  
  
<Combo guid="guidWidgetPackage" id="cmdidInsertOptions"  
  priority="0x0500" type="DropDownCombo" defaultWidth="100"  
  idCommandList="cmdidGetInsertOptionsList">  
  <Parent guid="cmdSetGuidWidgetCommands" id="groupIDFileEdit">  
  <CommandFlag>DynamicVisibility</CommandFlag>  
  <Strings>  
    <ButtonText>Select Insert Options</ButtonText>  
  </Strings>  
</Combo>  
```  
  
## <a name="see-also"></a>另請參閱  
 [Visual Studio 命令表檔案 (.Vsct)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)
