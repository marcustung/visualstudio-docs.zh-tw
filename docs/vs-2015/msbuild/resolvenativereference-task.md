---
title: ResolveNativeReference 工作 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#ResolveNativeReference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, ResolveNativeReference task
- ResolveNativeReference task [MSBuild]
ms.assetid: 56acd101-de77-4eec-92c6-f5c6d2187579
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 137ab6c54176c7c95c13c4b3e4defb3924937bc7
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2019
ms.locfileid: "59650313"
---
# <a name="resolvenativereference-task"></a>ResolveNativeReference 工作
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

解析原生參考。 實作 <xref:Microsoft.Build.Tasks.ResolveNativeReference> 類別。 此類別支援的 .NET Framework 結構不適合直接從程式碼使用。  
  
## <a name="task-parameters"></a>工作參數  
 下表說明 `ResolveNativeReference` 工作的參數。  
  
|參數|描述|  
|---------------|-----------------|  
|`AdditionalSearchPaths`|需要 [String] (<!-- TODO: review code entity reference <xref:assetId:///String?qualifyHint=False&amp;autoUpgrade=True>  -->)`[]`參數。<br /><br /> 取得或設定搜尋路徑，以解析原生參考的組件識別碼。|  
|`ContainedComComponents`|選擇性的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 輸出參數。<br /><br /> 取得或設定原生組譯碼的 COM 元件。|  
|`ContainedLooseEtcFiles`|選擇性的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 輸出參數。<br /><br /> 取得或設定原生資訊清單中列出的鬆散 Etc 檔案。|  
|`ContainedLooseTlbFiles`|選擇性的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 輸出參數。<br /><br /> 取得或設定原生組譯碼的鬆散 .tlb 檔案。|  
|`ContainedPrerequisiteAssemblies`|選擇性的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 輸出參數。<br /><br /> 取得或設定必須存在才能使用資訊清單的組件。|  
|`ContainedTypeLibraries`|選擇性的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 輸出參數。<br /><br /> 取得或設定原生組譯碼的類型程式庫。|  
|`ContainingReferenceFiles`|選擇性的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 輸出參數。<br /><br /> 取得或設定參考檔。|  
|`NativeReferences`|必要的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 參數。<br /><br /> 取得或設定 Win32 原生組件參考。|  
  
## <a name="remarks"></a>備註  
 除了上述所列的參數，此項工作還會繼承 <xref:Microsoft.Build.Tasks.TaskExtension> 類別中的參數，而該類別本身又繼承 <xref:Microsoft.Build.Utilities.Task> 類別。 如需這些其他參數的清單及其說明，請參閱 [TaskExtension Base Class](../msbuild/taskextension-base-class.md)。  
  
## <a name="see-also"></a>另請參閱  
 [工作](../msbuild/msbuild-tasks.md)   
 [工作參考](../msbuild/msbuild-task-reference.md)
