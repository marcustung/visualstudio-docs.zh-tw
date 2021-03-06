---
title: ParallelCustomBuild 工作 | Microsoft Docs
ms.date: 03/10/2019
ms.topic: reference
f1_keywords:
- vc.task.parallelcustombuild
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- MSBuild (Visual C++), ParallelCustomBuild task
- ParallelCustomBuild task (MSBuild (Visual C++))
author: mikeblome
ms.author: mblome
ms.workload:
- multiple
ms.openlocfilehash: 54623ab1c58d85de55c5b8a24384bf0be46f1a61
ms.sourcegitcommit: d78821f8c353e0102b1554719f549f32dffac71b
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2019
ms.locfileid: "58515122"
---
# <a name="parallelcustombuild-task"></a>ParallelCustomBuild 工作

執行 [CustomBuild 工作](../msbuild/custombuild-task.md)的平行執行個體。

## <a name="parameters"></a>參數

下表說明 **ParallelCustomBuild** 工作的參數。

|參數|說明|
|---------------|-----------------|
|**BreakOnFirstFailure**|選擇性的 **bool** 參數。|
|**MaxItemsInBatch**|選擇性的 **int** 參數。|
|**MaxProcesses**|選擇性的 **int** 參數。|
|**Sources**|必要的 **ITaskItem[]** 參數。|

## <a name="see-also"></a>另請參閱

[工作參考](../msbuild/msbuild-task-reference.md)