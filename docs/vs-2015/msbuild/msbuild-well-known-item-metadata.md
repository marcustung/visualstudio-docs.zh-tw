---
title: MSBuild 已知的項目中繼資料 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, item metadata
- MSBuild, well-known item metadata
ms.assetid: b5e791b5-c68f-4978-ad8a-9247d03bb6c0
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 02464cd6c7116da988903d8a8f19f36c900595f1
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47499455"
---
# <a name="msbuild-well-known-item-metadata"></a>MSBuild 已知的項目中繼資料
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主題的最新的版本可從[MSBuild 已知的項目中繼資料](https://docs.microsoft.com/visualstudio/msbuild/msbuild-well-known-item-metadata)。  
  
  
下表說明在建立期間指派給每個項目的中繼資料。 每個範例都使用了下列項目宣告，以在專案中包含 `C:\MyProject\Source\Program.cs` 檔案。  
  
```  
<ItemGroup>  
    <MyItem Include="Source\Program.cs" />  
</ItemGroup>  
```  
  
|項目中繼資料|描述|  
|-------------------|-----------------|  
|%(FullPath)|包含項目的完整路徑。 例如: <br /><br /> `C:\MyProject\Source\Program.cs`|  
|%(RootDir)|包含項目的根目錄。 例如: <br /><br /> `C:\`|  
|%(Filename)|包含項目的檔案名稱 (不含副檔名)。 例如: <br /><br /> `Program`|  
|%(Extension)|包含項目的副檔名。 例如: <br /><br /> `.cs`|  
|%(RelativeDir)|包含 `Include` 屬性中指定的路徑，直到最後一個反斜線 (\\) 為止。 例如: <br /><br /> `Source\`|  
|%(Directory)|包含項目的目錄 (不含根目錄)。 例如: <br /><br /> `MyProject\Source\`|  
|%(RecursiveDir)|如果 `Include` 屬性包含萬用字元 \*\*，此中繼資料會指定取代萬用字元的部分路徑。 如需萬用字元的詳細資訊，請參閱[如何：選取要建置的檔案](../msbuild/how-to-select-the-files-to-build.md)。<br /><br /> 如果資料夾 *C:\MySolution\MyProject\Source\\* 包含 Program.cs 檔案，而且專案檔包含此項目：<br /><br /> `<ItemGroup>`<br /><br /> `<MyItem Include="C:\**\Program.cs" />`<br /><br /> `</ItemGroup>`<br /><br /> 則 `%(MyItem.RecursiveDir)` 的值會是 *MySolution\MyProject\Source\\*。|  
|%(Identity)|`Include` 屬性中指定的項目。 例如: <br /><br /> `Source\Program.cs`|  
|%(ModifiedTime)|包含上次修改項目時間的時間戳記。 例如: <br /><br /> `2004-07-01 00:21:31.5073316`|  
|%(CreatedTime)|包含項目建立時間的時間戳記。 例如: <br /><br /> `2004-06-25 09:26:45.8237425`|  
|%(AccessedTime)|包含上次存取項目時間的時間戳記。<br /><br /> `2004-08-14 16:52:36.3168743`|  
  
## <a name="see-also"></a>另請參閱  
 [項目](../msbuild/msbuild-items.md)   
 [批次處理](../msbuild/msbuild-batching.md)   
 [MSBuild 參考](../msbuild/msbuild-reference.md)


