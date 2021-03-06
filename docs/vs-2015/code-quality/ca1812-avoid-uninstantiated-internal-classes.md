---
title: CA1812:避免使用未執行個體化的內部類別 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1812
- AvoidUninstantiatedInternalClasses
helpviewer_keywords:
- AvoidUninstantiatedInternalClasses
- CA1812
ms.assetid: 1bb92a42-322a-44cc-98a8-8858212c1e1f
caps.latest.revision: 28
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f44dcb010dd9c62d130913efd590a4c1b651de50
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60081993"
---
# <a name="ca1812-avoid-uninstantiated-internal-classes"></a>CA1812:避免使用未執行個體化的內部類別
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|AvoidUninstantiatedInternalClasses|
|CheckId|CA1812|
|分類|Microsoft.Performance|
|中斷變更|非重大|

## <a name="cause"></a>原因
 組件層級類型的執行個體不是由組件中的程式碼所建立。

## <a name="rule-description"></a>規則描述
 此規則會嘗試找出其中的型別，建構函式的呼叫，並報告違規情形，如果不找到任何呼叫。

 此規則就不會檢查下列類型：

- 值類型

- 抽象類型

- 列舉

- 委派

- 編譯器發出的陣列類型

- 類型，無法具現化，並定義`static`(`Shared` Visual Basic 中) 只方法。

  如果您套用<xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?displayProperty=fullName>正在分析之組件，此規則不會發生在標示為任何建構函式`internal`因為您不知道欄位是否正由另一個`friend`組件。

  即使您無法解決這項限制中[!INCLUDE[vsprvs](../includes/vsprvs-md.md)]程式碼分析，外部的獨立 FxCop 會發生內部建構函式上每個`friend`組件會出現在分析中。

## <a name="how-to-fix-violations"></a>如何修正違規
 若要修正此規則的違規情形，移除類型，或加入程式碼使用它。 如果型別只包含靜態方法，請加入下列其中一種類型，以避免編譯器發出的預設公用執行個體建構函式：

- 私用建構函式的類型為目標[!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]1.0 和 1.1 版。

- `static` (`Shared` Visual Basic 中) 修飾詞的類型為目標[!INCLUDE[dnprdnlong](../includes/dnprdnlong-md.md)]。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機
 它可安全地隱藏此規則的警告。 我們建議您隱藏這個警告，在下列情況：

- 這類的類別建立透過晚期繫結反映方法<xref:System.Activator.CreateInstance%2A?displayProperty=fullName>。

- 執行階段所自動建立類別或[!INCLUDE[vstecasp](../includes/vstecasp-md.md)]。 例如，類別實作<xref:System.Configuration.IConfigurationSectionHandler?displayProperty=fullName>或<xref:System.Web.IHttpHandler?displayProperty=fullName>。

- 類別會當做有新的條件約束的泛型類型參數傳遞。 例如，下列範例將會引發此規則。

  ```csharp
  internal class MyClass
  {
      public DoSomething()
      {
      }
  }
  public class MyGeneric<T> where T : new()
  {
      public T Create()
      {
          return new T();
      }
  }
  // [...]
  MyGeneric<MyClass> mc = new MyGeneric<MyClass>();
  mc.Create();
  ```

  在這些情況下，我們建議您隱藏這個警告。

## <a name="related-rules"></a>相關的規則
 [CA1811:避免使用未呼叫的私用程式碼](../code-quality/ca1811-avoid-uncalled-private-code.md)

 [CA1801： 必須檢閱未使用的參數](../code-quality/ca1801-review-unused-parameters.md)

 [CA1804： 必須移除未使用的區域變數](../code-quality/ca1804-remove-unused-locals.md)
