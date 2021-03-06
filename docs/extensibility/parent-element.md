---
title: 父項目 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT XML schema elements, Parent
- Parent element (VSCT XML schema)
ms.assetid: e4624ac8-1b9a-4940-910a-528a661cefad
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7220e435090cc688d32a2d6d26917a8c05510d4f
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687909"
---
# <a name="parent-element"></a>父項目
按鈕或下拉式方塊的父代可能只是群組。 功能表或群組的父系可能是功能表或群組。 在  [CommandPlacement 元素](../extensibility/commandplacement-element.md)，則需要這個元素; 所有其他執行個體中是選擇性的。 如果省略這個項目，則父代`Group_Undefined:0`會隱含。

## <a name="syntax"></a>語法

```xml
<Parent guid="guidMyCommandSet" id="MyParentGroupOrMenu" />
```

## <a name="attributes-and-elements"></a>屬性和元素
 下列章節說明屬性、子元素和父元素。

### <a name="attributes"></a>屬性

|屬性|描述|
|---------------|-----------------|
|guid|必要項。 GUID/識別碼 GUID 命令識別項。|
|id|必要項。 識別碼的 GUID/識別碼命令識別項。|

### <a name="child-elements"></a>子元素
 無

### <a name="parent-elements"></a>父元素

|元素|描述|
|-------------|-----------------|
|[CommandTable 元素](../extensibility/commandtable-element.md)|定義代表命令的 VSPackage 提供整合式的開發環境 (IDE) 的所有項目。 例如，功能表項目、 功能表、 工具列和下拉式方塊。|
|[Buttons 元素](../extensibility/buttons-element.md)|群組[Button 元素](../extensibility/button-element.md)項目。|
|[功能表項目](../extensibility/menus-element.md)|定義實作 VSPackage 的所有功能表。|
|[Groups 元素](../extensibility/groups-element.md)|包含定義 VSPackage 的命令群組的項目。|

## <a name="see-also"></a>另請參閱
- [Visual Studio 命令表檔案 (.vsct)](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)