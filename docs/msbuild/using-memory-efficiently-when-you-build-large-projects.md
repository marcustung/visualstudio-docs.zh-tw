---
title: 在建置大型專案時有效使用記憶體 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- memory use (MSBuild)
- msbuild, efficient memory use building large trees
- caching (MSBuild)
ms.assetid: 853a21ed-69f7-4817-af00-57f73e2c74b5
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab3be342f31e5df018c14f84d30febd38c31c401
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56631649"
---
# <a name="use-memory-efficiently-when-you-build-large-projects"></a>在建置大型專案時有效使用記憶體
大型專案通常會包含許多子專案和其他相依性，這可能會在建置時耗用大量系統記憶體。 可用系統記憶體減少時，系統效能也可能會降低。 舊版 [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 專案會保留在記憶體中。 3.5 版中移除了舊版專案，但在快取中保留了建置結果以供日後擷取之用。

 4.0 版會自動處理此記憶體管理，並儲存專案；而不需要使用 `UnloadProjectsOnCompletion` 和 `UseResultsCache` 這類屬性。

### <a name="see-also"></a>另請參閱
- [平行建置多個專案](../msbuild/building-multiple-projects-in-parallel-with-msbuild.md)