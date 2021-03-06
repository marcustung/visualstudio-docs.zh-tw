---
title: CA1821:必須移除空的完成項
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- RemoveEmptyFinalizers
- CA1821
helpviewer_keywords:
- CA1821
ms.assetid: 3f4855a0-e4a0-46e6-923c-4c3b7074048d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 16bb2786c4c7b0ca94fe60a9577e4b462d663bfc
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55957844"
---
# <a name="ca1821-remove-empty-finalizers"></a>CA1821:必須移除空的完成項

|||
|-|-|
|TypeName|RemoveEmptyFinalizers|
|CheckId|CA1821|
|分類|Microsoft.Performance|
|中斷變更|非重大|

## <a name="cause"></a>原因
 型別實作完成項是空的、 呼叫只有基底類型完成項，或僅有條件地發出方法呼叫。

## <a name="rule-description"></a>規則描述
 請盡可能避免使用完成項，因為追蹤物件存留期 (Lifetime) 時將會產生額外的效能負荷。 它會收集物件之前，記憶體回收行程會執行完成項。 這表示兩個集合都需要回收物件。 空的完成項會產生此額外負荷，而沒有任何好處。

## <a name="how-to-fix-violations"></a>如何修正違規
 移除空的完成項。 如果需要進行偵錯完成項，括住整個的完成項中`#if DEBUG / #endif`指示詞。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 請勿隱藏這項規則的訊息。 若要隱藏最終處理失敗會降低效能，並不提供任何好處。

## <a name="example"></a>範例
 下列範例顯示空的完成項，應該移除、 完成項，應該括住`#if DEBUG / #endif`指示詞，並使用完成項`#if DEBUG / #endif`指示詞正確。

 [!code-csharp[FxCop.Performance.RemoveEmptyFinalizers#1](../code-quality/codesnippet/CSharp/ca1821-remove-empty-finalizers_1.cs)]