---
title: PreviewImage 元素 （Visual Studio 範本） |Microsoft Docs
ms.date: 11/04/2016
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- <PreviewImage> Element (Visual Studio Templates)
- PreviewImage Element (Visual Studio Templates)
ms.assetid: d1796f20-523b-4e0d-8ac3-ca87f3b5a9b6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 15e09d7837c04c276e955f88e8b1afd670d6e948
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56687766"
---
# <a name="previewimage-element-visual-studio-templates"></a>PreviewImage 元素 （Visual Studio 範本）
指定的預覽影像，做為檔案名稱，會出現在 [預覽映像**新的專案**或是**加入新項目**] 對話方塊。

 \<VSTemplate> \<TemplateData> \<PreviewImage>

## <a name="syntax"></a>語法

```
<PreviewImage>"filename"</PreviewImage>
```

## <a name="attributes-and-elements"></a>屬性和元素
 下列章節說明屬性、子元素和父元素。

### <a name="attributes"></a>屬性
 無。

### <a name="child-elements"></a>子元素
 無。

### <a name="parent-elements"></a>父元素

|元素|描述|
|-------------|-----------------|
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|必要項目。<br /><br /> 將範本分類，以及定義如何顯示在**新的專案**或**加入新項目** 對話方塊。|

## <a name="text-value"></a>文字值
 需要文字值。

 文字必須是字串，表示檔案名稱。

## <a name="remarks"></a>備註
 `PreviewImage` 是選擇性項目。

## <a name="see-also"></a>另請參閱
- [Visual Studio 範本結構描述參考](../extensibility/visual-studio-template-schema-reference.md)
- [建立專案和項目範本](../ide/creating-project-and-item-templates.md)