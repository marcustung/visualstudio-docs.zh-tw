---
title: CA1721:屬性名稱不應該相符的 get 方法 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
helpviewer_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
ms.assetid: 45a0e853-1f06-4688-af1b-cc634409e295
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c9a3dcf6566267cebdfeecb91f57bf139be46de2
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/24/2019
ms.locfileid: "59000406"
---
# <a name="ca1721-property-names-should-not-match-get-methods"></a>CA1721:屬性名稱不應該和其中有 get 的方法名稱相符
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|PropertyNamesShouldNotMatchGetMethods|
|CheckId|CA1721|
|分類|Microsoft.Naming|
|中斷變更|中斷|

## <a name="cause"></a>原因
 公用或受保護的成員名稱開頭為 'Get'，否則需符合公用或受保護的屬性名稱。 比方說，此型別包含名為 'GetColor' 和名為 'Color' 屬性的方法違反此規則。

## <a name="rule-description"></a>規則描述
 Get 方法和屬性應該清楚區別其功能的名稱。

 命名慣例提供了通用程式庫 common language runtime 為目標。 這可減少的時間，才能了解新的軟體程式庫，並增加程式庫，開發人員專業開發的 managed 程式碼中的其他人的客戶信心。

## <a name="how-to-fix-violations"></a>如何修正違規
 變更名稱，使它不符合加上 'Get' 方法的名稱。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 請勿隱藏此規則的警告。

> [!NOTE]
>  如果因為實作 IExtenderProvider 介面的 Get 方法，可能會排除這個警告。

## <a name="example"></a>範例
 下列範例包含方法和違反此規則的屬性。

 [!code-csharp[FxCop.Naming.GetMethod#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod/cs/FxCop.Naming.GetMethod.cs#1)]
 [!code-vb[FxCop.Naming.GetMethod#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod/vb/FxCop.Naming.GetMethod.vb#1)]

## <a name="related-rules"></a>相關的規則
 [CA1024:在適當時使用屬性](../code-quality/ca1024-use-properties-where-appropriate.md)
