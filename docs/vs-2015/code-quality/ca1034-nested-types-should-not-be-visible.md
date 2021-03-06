---
title: CA1034:巢狀的類型不應該為可見 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- NestedTypesShouldNotBeVisible
- CA1034
helpviewer_keywords:
- NestedTypesShouldNotBeVisible
- CA1034
ms.assetid: e9789a2c-2540-42a1-8705-ae7104011194
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 915b5807f7b14269acf4b7509ffceaecfb13af47
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58942641"
---
# <a name="ca1034-nested-types-should-not-be-visible"></a>CA1034:巢狀類型不應該為可見的
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|NestedTypesShouldNotBeVisible|
|CheckId|CA1034|
|分類|Microsoft.Design|
|中斷變更|中斷|

## <a name="cause"></a>原因
 外部可見的型別包含為外部可見的型別宣告。 巢狀的列舉與受保護的類型是 免套用此規則。

## <a name="rule-description"></a>規則描述
 巢狀型別是另一種類型的範圍內宣告的類型。 巢狀型別可用於封裝為包含類型的私用實作詳細資料。 因為有這樣的用途，所以巢狀類型不應為外部可見的。

 邏輯群組，或避免發生名稱衝突，請不要使用外部可見的巢狀的類型相反地，使用命名空間。

 巢狀型別包含成員存取範圍，某些程式設計人員不清楚地了解的概念。

 受保護的類型可以用於子類別以及進階的自訂案例中的巢狀型別。

## <a name="how-to-fix-violations"></a>如何修正違規
 如果您不想要為外部可見的巢狀型別，變更型別的存取範圍。 否則，從其父代移除巢狀型別。 如果巢狀的目的是要分類的巢狀的類型，請改為建立階層中使用的命名空間。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 請勿隱藏此規則的警告。

## <a name="example"></a>範例
 下列範例顯示違反規則的型別。

 [!code-cpp[FxCop.Design.NestedTypes#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.NestedTypes/cpp/FxCop.Design.NestedTypes.cpp#1)]
 [!code-csharp[FxCop.Design.NestedTypes#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.NestedTypes/cs/FxCop.Design.NestedTypes.cs#1)]
 [!code-vb[FxCop.Design.NestedTypes#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.NestedTypes/vb/FxCop.Design.NestedTypes.vb#1)]
