---
title: '&lt;customHostSpecified&gt;元素 （在 Visual Studio 中的 Office 程式開發）'
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application manifests [Office development in Visual Studio], <customHostSpecified> element
- <customHostSpecified> element
- customHostSpecified element
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 26597796c99d3ab8740812819cf3aa5568e2985b
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874376"
---
# <a name="ltcustomhostspecifiedgt-element-office-development-in-visual-studio"></a>&lt;customHostSpecified&gt;元素 （在 Visual Studio 中的 Office 程式開發）
  `customHostSpecified`項目會指出此解決方案不是獨立的應用程式。 Office 方案包含裝載在 Microsoft Office 應用程式的元件。

## <a name="syntax"></a>語法

```xml
<customHostSpecified />
```

## <a name="elements-and-attributes"></a>元素和屬性
 `customHostSpecified` ，則需要 Office 方案的元素。 此元素為`co.v1`命名空間及指定此部署包含將自訂主機，內部部署的元件，並不是獨立的應用程式。

 這個項目是第一個子系`<entrypoint>`應用程式資訊清單中的項目。 可以是任何其他子項目中，`<entrypoint>`項目或[!INCLUDE[ndptecclick](../vsto/includes/ndptecclick-md.md)]將會在安裝期間引發驗證錯誤。

 這個項目具有屬性和任何子項目。

## <a name="example"></a>範例
 下列程式碼範例說明`customHostSpecified`Office 方案的應用程式資訊清單中的項目。 此程式碼範例是中提供之較大範例的一部分[Application manifests for Office 方案](../vsto/application-manifests-for-office-solutions.md)。

```xml
<entryPoint>
    <co.v1:customHostSpecified />
</entryPoint>
```

## <a name="see-also"></a>另請參閱

- [Office 方案的應用程式資訊清單](../vsto/application-manifests-for-office-solutions.md)
- [Office 方案的部署資訊清單](../vsto/deployment-manifests-for-office-solutions.md)
- [ClickOnce 應用程式資訊清單](../deployment/clickonce-application-manifest.md)