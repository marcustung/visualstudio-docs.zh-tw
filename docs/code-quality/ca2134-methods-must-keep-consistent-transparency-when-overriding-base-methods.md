---
title: CA2134:覆寫基底方法時，方法必須保持一致的透明度
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2134
ms.assetid: 3b17e487-0326-442e-90e1-dc0ba9cdd3f2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 67114c20a7fcf5e8ff01773d8777b23d3caf3d91
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954656"
---
# <a name="ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods"></a>CA2134:覆寫基底方法時，方法必須保持一致的透明度

|||
|-|-|
|TypeName|MethodsMustOverrideWithConsistentTransparency|
|CheckId|CA2134|
|分類|Microsoft.Security|
|中斷變更|中斷|

## <a name="cause"></a>原因
 以標記方法時，就會引發此規則<xref:System.Security.SecurityCriticalAttribute>覆寫的方法為透明或使用<xref:System.Security.SecuritySafeCriticalAttribute>。 當透明或使用的方法時，也會引發此規則<xref:System.Security.SecuritySafeCriticalAttribute>覆寫的方法標記著<xref:System.Security.SecurityCriticalAttribute>。

 覆寫虛擬方法或實作介面時會套用此規則。

## <a name="rule-description"></a>規則描述
 若要變更的方法進一步繼承鏈結上的安全性存取嘗試都會引發此規則。 比方說，如果透明或安全關鍵性的基底類別中的虛擬方法，然後在衍生的類別必須覆寫它使用透明或安全關鍵性的方法。 相反地，如果虛擬是安全性關鍵，衍生的類別必須覆寫它使用安全性關鍵方法。 實作介面方法適用於相同的規則。

 程式碼是 JIT 編譯而不是在執行階段，讓透明度計算沒有動態型別資訊時，會強制執行透明度規則。 因此，透明度計算的結果必須能夠判斷完全從進行 JIT 編譯，不論動態類型的靜態類型。

## <a name="how-to-fix-violations"></a>如何修正違規
 若要修正此規則的違規情形，變更方法覆寫虛擬方法或實作介面，以比對透明度的虛擬或介面方法的透明度。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 請勿隱藏這項規則的警告。 違反此規則會導致執行階段<xref:System.TypeLoadException>使用層級 2 透明度的組件。

## <a name="examples"></a>範例

### <a name="code"></a>程式碼
 [!code-csharp[FxCop.Security.CA2134.MethodsMustOverrideWithConsistentTransparency#1](../code-quality/codesnippet/CSharp/ca2134-methods-must-keep-consistent-transparency-when-overriding-base-methods_1.cs)]

## <a name="see-also"></a>另請參閱
 [安全性透明程式碼，層級 2](/dotnet/framework/misc/security-transparent-code-level-2)