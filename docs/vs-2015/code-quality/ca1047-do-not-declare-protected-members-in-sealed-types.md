---
title: CA1047:不要宣告在密封類型中的受保護的成員 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotDeclareProtectedMembersInSealedTypes
- CA1047
helpviewer_keywords:
- CA1047
- DoNotDeclareProtectedMembersInSealedTypes
ms.assetid: 829033b5-a9d8-4f26-a719-45494c9dd035
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 6d949a756dfe3ff22ba43d172078d35bfe706e14
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944561"
---
# <a name="ca1047-do-not-declare-protected-members-in-sealed-types"></a>CA1047:不要在密封類型中宣告 protected 成員
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotDeclareProtectedMembersInSealedTypes|
|CheckId|CA1047|
|分類|Microsoft.Design|
|中斷變更|非重大|

## <a name="cause"></a>原因
 公用類型是`sealed`(`NotInheritable` Visual Basic 中)，並宣告受保護的成員或受保護的巢狀型別。 此規則不會報告的違規<xref:System.Object.Finalize%2A>必須遵循這個模式的方法。

## <a name="rule-description"></a>規則描述
 類型會宣告 protected 成員，如此繼承的類型即可存取或覆寫成員。 根據定義，您無法繼承自密封型別，也就是說，受保護的方法，密封類型上的無法呼叫。

 C# 編譯器會發出這項錯誤的警告。

## <a name="how-to-fix-violations"></a>如何修正違規
 若要修正此規則的違規情形，變更成員的存取層級設為私用，或讓類型成為可繼承。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 請勿隱藏此規則的警告。 類型在目前的狀態可能會造成維護問題並不提供任何好處。

## <a name="example"></a>範例
 下列範例顯示違反此規則的型別。

 [!code-csharp[FxCop.Design.SealedNoProtected#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.SealedNoProtected/cs/FxCop.Design.SealedNoProtected.cs#1)]
 [!code-vb[FxCop.Design.SealedNoProtected#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.SealedNoProtected/vb/FxCop.Design.SealedNoProtected.vb#1)]
