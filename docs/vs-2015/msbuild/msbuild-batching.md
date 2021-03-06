---
title: MSBuild 批次處理 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
helpviewer_keywords:
- batching [MSBuild]
- MSBuild, batching
ms.assetid: d35c085b-27b8-49d7-b6f8-8f2f3a0eec38
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 823b853363e3044383da4673d7e88a96d9e5ea6a
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2019
ms.locfileid: "59664332"
---
# <a name="msbuild-batching"></a>MSBuild 批次處理
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] 能夠根據項目中繼資料，將項目清單分割成不同的類別或批次，然後針對每個批次一次執行一個目標或工作。  
  
## <a name="task-batching"></a>工作批次處理  
 工作批次處理可讓您將項目清單分割成不同的批次，並分別將各批次傳遞給工作，以簡化專案檔案。 這表示即使工作可能要執行若干次，專案檔也只需要宣告一次工作和其屬性。  
  
 您可以在其中一個工作屬性中使用 %(*ItemMetaDataName*) 標記法，以指定要讓 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] 執行工作的批次處理。 下列範例會根據 `Color` 項目中繼資料值，將 `Example` 項目清單分割成批次，並將每個批次個別傳遞給 `MyTask` 工作。  
  
> [!NOTE]
>  如果您不需參考工作屬性中其他位置的項目清單，或中繼資料名稱可能模稜兩可，您可以使用 %(*ItemCollection.ItemMetaDataName*) 標記法，來完整限定要用於批次處理的項目中繼資料值。  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <Example Include="Item1">  
            <Color>Blue</Color>  
        </Example>  
        <Example Include="Item2">  
            <Color>Red</Color>  
        </Example>  
    </ItemGroup>  
  
    <Target Name="RunMyTask">  
        <MyTask  
            Sources = "@(Example)"  
            Output = "%(Color)\MyFile.txt"/>  
    </Target>  
  
</Project>  
```  
  
 如需更具體的批次處理範例，請參閱[工作批次處理中的項目中繼資料](../msbuild/item-metadata-in-task-batching.md)。  
  
## <a name="target-batching"></a>目標批次處理  
 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] 會在執行目標之前檢查目標的輸入和輸出是否都為最新狀態。 如果輸入和輸出都是最新的，則會略過目標。 如果在目標內的工作會使用批次處理，[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] 需要判斷每個批次項目的輸入和輸出是否都為最新狀態。 否則，每次叫用目標時均會執行。  
  
 下列範例示範包含 `Outputs` 屬性與 %(*ItemMetaDataName*) 標記法的 `Target` 項目。 [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] 會根據 `Color` 項目中繼資料，將 `Example` 項目清單分割成批次，並分析每個批次的輸出檔時間戳記。 如果批次的輸出不是最新狀態，則會執行目標。 否則，會略過目標。  
  
```  
<Project  
    xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
  
    <ItemGroup>  
        <Example Include="Item1">  
            <Color>Blue</Color>  
        </Example>  
        <Example Include="Item2">  
            <Color>Red</Color>  
        </Example>  
    </ItemGroup>  
  
    <Target Name="RunMyTask"  
        Inputs="@(Example)"  
        Outputs="%(Color)\MyFile.txt">  
        <MyTask  
            Sources = "@(Example)"  
            Output = "%(Color)\MyFile.txt"/>  
    </Target>  
  
</Project>  
```  
  
 如需目標批次處理的其他範例，請參閱[目標批次處理中的項目中繼資料](../msbuild/item-metadata-in-target-batching.md)。  
  
## <a name="property-functions-using-metadata"></a>使用中繼資料的屬性函式  
 批次處理可由包含中繼資料的屬性函式來控制。 例如，套用至物件的  
  
 `$([System.IO.Path]::Combine($(RootPath),%(Compile.Identity)))`  
  
 會使用 <xref:System.IO.Path.Combine%2A> 來結合根資料夾路徑和編譯項目路徑。  
  
 屬性函式可能不會出現在中繼資料值內。  例如，套用至物件的  
  
 `%(Compile.FullPath.Substring(0,3))`  
  
 不允許。  
  
 如需屬性函式的詳細資訊，請參閱[屬性函式](../msbuild/property-functions.md)。  
  
## <a name="see-also"></a>請參閱  
 [ItemMetadata 元素 (MSBuild)](../msbuild/itemmetadata-element-msbuild.md)   
 [MSBuild 概念](../msbuild/msbuild-concepts.md)   
 [MSBuild 參考](../msbuild/msbuild-reference.md)   
 [進階概念](../msbuild/msbuild-advanced-concepts.md)
