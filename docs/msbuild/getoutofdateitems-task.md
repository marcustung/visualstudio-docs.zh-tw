---
title: GetOutOfDateItems 工作 | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.getoutofdateitems
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), GetOutOfDateItems task
- GetOutOfDateItems task (MSBuild (Visual C++))
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: e3393dd7e81fa98c49dd09a32457171286f88f18
ms.sourcegitcommit: d78821f8c353e0102b1554719f549f32dffac71b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2019
ms.locfileid: "58514965"
---
# <a name="getoutofdateitems-task"></a>GetOutOfDateItems 工作

協助程式工作，可讀取舊的 tlog、寫入新的 tlog，並傳回一組不是最新狀態的項目。

## <a name="parameters"></a>參數

下表說明 **GetOutOfDateItems** 工作的參數。

|參數|說明|
|---------------|-----------------|
|**CheckForInterdependencies**|選擇性的 **bool** 參數。|
|**CommandMetadataName**|選擇性的 **string** 參數。|
|**DependenciesMetadataName**|選擇性的 **string** 參數。|
|**HasInterdependencies**|選擇性的 **bool** 輸出參數。|
|**OutOfDateSources**|選擇性的 **ITaskItem[]** 輸出參數。|
|**OutputsMetadataName**|必要的 **string** 參數。|
|**Sources**|選擇性的 **ITaskItem[]** 參數。|
|**TLogDirectory**|必要的 **string** 參數。|
|**TLogNamePrefix**|必要的 **string** 參數。|

## <a name="see-also"></a>另請參閱

[工作參考](../msbuild/msbuild-task-reference.md)