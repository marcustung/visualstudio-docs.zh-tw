---
title: CA1058:類型不應該擴充特定基底類型 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- TypesShouldNotExtendCertainBaseTypes
- CA1058
helpviewer_keywords:
- CA1058
- TypesShouldNotExtendCertainBaseTypes
ms.assetid: 8446ee40-beb1-49fa-8733-4d8e813471c0
caps.latest.revision: 26
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1ce67a70b6cbe955ef13bf6475a672bcbb687d95
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60046535"
---
# <a name="ca1058-types-should-not-extend-certain-base-types"></a>CA1058:類型不應該擴充特定基底類型
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|TypesShouldNotExtendCertainBaseTypes|
|CheckId|CA1058|
|分類|Microsoft.Design|
|中斷變更|中斷|

## <a name="cause"></a>原因
 外部可見的類型會延伸某些基底類型 (Base Type)。 目前，此規則會回報衍生自下列類型的類型：

- <xref:System.ApplicationException?displayProperty=fullName>

- <xref:System.Xml.XmlDocument?displayProperty=fullName>

- <xref:System.Collections.CollectionBase?displayProperty=fullName>

- <xref:System.Collections.DictionaryBase?displayProperty=fullName>

- <xref:System.Collections.Queue?displayProperty=fullName>

- <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>

- <xref:System.Collections.SortedList?displayProperty=fullName>

- <xref:System.Collections.Stack?displayProperty=fullName>

## <a name="rule-description"></a>規則描述
 針對[!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]第 1 版中，會建議衍生新的例外狀況，從<xref:System.ApplicationException>。 建議變更和新的例外狀況應該衍生自<xref:System.Exception?displayProperty=fullName>或其中一個子類別中<xref:System>命名空間。

 請勿建立的子類別<xref:System.Xml.XmlDocument>如果您想要建立基礎物件模型或資料來源的 XML 檢視。

### <a name="non-generic-collections"></a>非泛型集合
 使用及/或擴充盡可能的泛型集合。 除非您先前隨附未延伸您的程式碼中的非泛型集合。

 **不正確的使用方式的範例**

```csharp
public class MyCollection : CollectionBase
{
}

public class MyReadOnlyCollection : ReadOnlyCollectionBase
{
}
```

 **正確使用方式的範例**

```csharp
public class MyCollection : Collection<T>
{
}

public class MyReadOnlyCollection : ReadOnlyCollection<T>
{
}
```

## <a name="how-to-fix-violations"></a>如何修正違規
 若要修正此規則的違規情形，請從不同的基底類型或泛型集合衍生型別。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 請勿隱藏這項規則違規警告有關<xref:System.ApplicationException>。 安全地隱藏這項規則違規警告有關<xref:System.Xml.XmlDocument>。 它可安全地隱藏非泛型集合有關的警告，如果先前發行的程式碼。
