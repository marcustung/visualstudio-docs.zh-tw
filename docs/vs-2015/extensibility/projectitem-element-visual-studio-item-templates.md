---
title: ProjectItem 項目 （Visual Studio 項目範本） |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#ProjectItem
helpviewer_keywords:
- <ProjectItem> element [Visual Studio item templates]
- ProjectItem element [Visual Studio item templates]
ms.assetid: 9ed94112-0c38-49df-b728-0dd2d0d1eb47
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 29b65f5cff9e2ffbed3c66c29c61f0a7e9e50f20
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58945347"
---
# <a name="projectitem-element-visual-studio-item-templates"></a>ProjectItem 項目 (Visual Studio 項目範本)
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

指定項目範本中所包含的檔案。  
  
> [!NOTE]
>  `ProjectItem`元素接受不同的屬性，根據該範本是否為專案或項目。 本主題說明`ProjectItem`項目的項目。 如需說明`ProjectItem`項目專案範本，請參閱[ProjectItem 項目 （Visual Studio 專案範本）](../extensibility/projectitem-element-visual-studio-project-templates.md)。  
  
 \<VSTemplate>  
 \<TemplateContent>  
 \<ProjectItem>  
  
## <a name="syntax"></a>語法  
  
```  
<ProjectItem  
    SubType="Form/Component/CustomControl/UserControl"  
    CustomTool="string"  
    ItemType="string"  
    ReplaceParameters="true/false"  
    TargetFileName="TargetFileName.ext">  
        FileName.ext  
</ProjectItem>  
```  
  
## <a name="attributes-and-elements"></a>屬性和項目  
 下列章節將說明屬性、子項目和父項目。  
  
### <a name="attributes"></a>屬性  
  
|屬性|描述|  
|---------------|-----------------|  
|`SubType`|選擇性屬性。<br /><br /> 多檔案項目範本中指定項目子的類型。 這個值用來判斷編輯器，[!INCLUDE[vsprvs](../includes/vsprvs-md.md)]將用以開啟項目。|  
|`CustomTool`|選擇性屬性。<br /><br /> 專案檔中設定項目的自訂工具。|  
|`ItemType`|選擇性屬性。<br /><br /> 專案檔中設定項目的 ItemType。|  
|`ReplaceParameters`|選擇性屬性。<br /><br /> 布林值，指定的項目是否有從範本建立專案時，必須被取代的參數值。 預設值為 `false`。|  
|`TargetFileName`|選擇性屬性。<br /><br /> 指定從範本建立的項目名稱。 這個屬性可用於建立項目名稱使用參數取代。|  
  
### <a name="child-elements"></a>子元素  
 無。  
  
### <a name="parent-elements"></a>父項目  
  
|項目|描述|  
|-------------|-----------------|  
|[TemplateContent](../extensibility/templatecontent-element-visual-studio-templates.md)|指定範本的內容。|  
  
## <a name="text-value"></a>文字值  
 需要文字值。  
  
 A`string`表示範本的.zip 檔中的檔案名稱。  
  
## <a name="remarks"></a>備註  
 `ProjectItem` 是選擇性的子系的`TemplateContent`。  
  
 `TargetFileName`屬性可用來重新命名具有參數檔案。 比方說，如果檔案`MyFile.vb`存在於範本.zip 檔案，但您的根目錄中的使用者所提供的檔案名稱的檔案命名為基礎的想**加入新項目** 對話方塊中，您可以使用下列 XML:  
  
```  
<ProjectItem TargetFileName="$fileinputname$.vb">MyFile.vb</ProjectItem>  
```  
  
 檔案名稱從這個範本建立項目時，會根據使用者輸入的名稱**加入新項目** 對話方塊。 建立多檔案項目範本時，這非常有用。 如需詳細資訊，請參閱[如何：建立多檔案項目範本](../ide/how-to-create-multi-file-item-templates.md)並[範本參數](../ide/template-parameters.md)。  
  
## <a name="example"></a>範例  
 下列範例說明的標準項目範本的中繼資料[!INCLUDE[csprcs](../includes/csprcs-md.md)]類別。  
  
```  
<VSTemplate Type="Item" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyClass</Name>  
        <Description>My custom C# class.</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <DefaultName>MyClass.cs</DefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem ReplaceParameters="true">MyClass.cs</ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>另請參閱  
 [Visual Studio 範本結構描述參考](../extensibility/visual-studio-template-schema-reference.md)   
 [建立專案和項目範本](../ide/creating-project-and-item-templates.md)   
 [如何：建立多檔案項目範本](../ide/how-to-create-multi-file-item-templates.md)   
 [範本參數](../ide/template-parameters.md)
