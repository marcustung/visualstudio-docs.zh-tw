---
title: CA1815:覆寫 equals 和實值型別上等號比較運算子 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1815
- OverrideEqualsAndOperatorEqualsOnValueTypes
helpviewer_keywords:
- OverrideEqualsAndOperatorEqualsOnValueTypes
- CA1815
ms.assetid: 0a8ab3a3-ee8e-46f7-985d-dcf00c89363b
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e21585a7a56fde2fb46ea86adde92eecfd1a4565
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58943411"
---
# <a name="ca1815-override-equals-and-operator-equals-on-value-types"></a>CA1815:必須覆寫實值類型上的 Equals 方法和等號比較運算子
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|OverrideEqualsAndOperatorEqualsOnValueTypes|
|CheckId|CA1815|
|分類|Microsoft.Performance|
|中斷變更|非重大|

## <a name="cause"></a>原因
 公用實值類型不覆寫<xref:System.Object.Equals%2A?displayProperty=fullName>，或是未實作等號比較運算子 （= =）。 此規則不會檢查列舉型別。

## <a name="rule-description"></a>規則描述
 實值型別，繼承實作<xref:System.Object.Equals%2A>使用 Reflection 程式庫，並比較所有欄位的內容。 但是 Reflection 相當耗費運算資源，而且可能不需要比較每個欄位是否相等。 如果您希望使用者比較或排序執行個體，或使用它們作為雜湊表索引鍵時，您的實值型別應該實作<xref:System.Object.Equals%2A>。 如果您的程式設計語言支援運算子多載，則也應該提供相等和不等運算子的實作。

## <a name="how-to-fix-violations"></a>如何修正違規
 若要修正此規則的違規情形，提供實作<xref:System.Object.Equals%2A>。 如果可以，您可以實作等號比較運算子。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 它可安全地隱藏此規則的警告，如果實值型別的執行個體不會互相比較。

## <a name="example-of-a-violation"></a>發生違規的範例

### <a name="description"></a>描述
 下列範例顯示違反此規則的結構 （數值型別）。

### <a name="code"></a>程式碼
 [!code-csharp[FxCop.Performance.OverrideEqualsViolation#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.OverrideEqualsViolation/cs/FxCop.Performance.OverrideEqualsViolation.cs#1)]

## <a name="example-of-how-to-fix"></a>範例，示範如何修正

### <a name="description"></a>描述
 下列範例會藉由覆寫修正上述違規<xref:System.ValueType.Equals%2A?displayProperty=fullName>和實作等號比較運算子 (= =、 ！ =)。

### <a name="code"></a>程式碼
 [!code-csharp[FxCop.Performance.OverrideEqualsFixed#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Performance.OverrideEqualsFixed/cs/FxCop.Performance.OverrideEqualsFixed.cs#1)]

## <a name="related-rules"></a>相關的規則
 [CA2224:覆寫等於多載等號比較運算子](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)

 [CA2231：在覆寫 ValueType.Equals 上多載等號運算子](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)

 [CA2226:運算子應該有對稱的多載](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)

## <a name="see-also"></a>另請參閱
 <xref:System.Object.Equals%2A?displayProperty=fullName>
