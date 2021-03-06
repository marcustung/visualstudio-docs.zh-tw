---
title: CA1309:使用循序的 StringComparison |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- UseOrdinalStringComparison
- CA1309
helpviewer_keywords:
- UseOrdinalStringComparison
- CA1309
ms.assetid: 19be0854-cb6e-4efd-a4c8-a5c1fc6f7a71
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 7b491cf06528b67c96f90f314210e61800e0cab1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58939936"
---
# <a name="ca1309-use-ordinal-stringcomparison"></a>CA1309:使用循序的 StringComparison
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|UseOrdinalStringComparison|
|CheckId|CA1309|
|分類|Microsoft.Globalization|
|中斷變更|非重大|

## <a name="cause"></a>原因
 非語言的字串比較作業不會設定<xref:System.StringComparison>參數設為**序數**或是**OrdinalIgnoreCase**。

## <a name="rule-description"></a>規則描述
 許多字串作業，最重要<xref:System.String.Compare%2A?displayProperty=fullName>並<xref:System.String.Equals%2A?displayProperty=fullName>方法，現在提供的多載，接受<xref:System.StringComparison?displayProperty=fullName>做為參數的列舉值。

 當您指定**StringComparison.Ordinal**或是**StringComparison.OrdinalIgnoreCase**，將會用非語言字串比較。 也就是比較批覆後，會忽略自然語言專屬的功能。 這表示所做的決策根據簡單的位元組比較，並忽略大小寫或對等會因文化特性參數化的資料表。 如此一來，藉由明確地將參數設定為其中一個**StringComparison.Ordinal**或是**StringComparison.OrdinalIgnoreCase**，程式碼通常可以提升速度、 增加正確性，和會變成更可靠。

## <a name="how-to-fix-violations"></a>如何修正違規
 若要修正此規則的違規情形，請將字串比較方法變更為接受的多載<xref:System.StringComparison?displayProperty=fullName>列舉型別做為參數，並指定**序數**或是**OrdinalIgnoreCase**。 例如，將 `String.Compare(str1, str2)` 變更為 `String.Compare(str1, str2, StringComparison.Ordinal)`。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 它是安全的程式庫或應用程式適用於有限制的本機使用者，或應該使用目前文化特性的語意時，隱藏此規則的警告。

## <a name="see-also"></a>另請參閱
 [全球化警告](../code-quality/globalization-warnings.md) [CA1307:指定 StringComparison](../code-quality/ca1307-specify-stringcomparison.md)
