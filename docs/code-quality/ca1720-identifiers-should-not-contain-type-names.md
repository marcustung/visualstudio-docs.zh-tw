---
title: CA1720:識別項名稱不應該包含類型名稱
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1720
- IdentifiersShouldNotContainTypeNames
helpviewer_keywords:
- IdentifiersShouldNotContainTypeNames
- CA1720
ms.assetid: c95ee48f-f23a-45f0-ac9e-a3c1ecfabdea
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d0eb7cfeb2271b7ed01f59d4892987fb2ef72808
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/14/2019
ms.locfileid: "57867715"
---
# <a name="ca1720-identifiers-should-not-contain-type-names"></a>CA1720:識別項名稱不應該包含類型名稱

|||
|-|-|
|TypeName|IdentifiersShouldNotContainTypeNames|
|CheckId|CA1720|
|分類|Microsoft.Naming|
|中斷變更|中斷|

## <a name="cause"></a>原因

成員中的參數名稱包含的資料型別名稱。

-或-

成員的名稱包含語言特定資料型別名稱。

根據預設，此規則只會查看外部可見的成員，但這[可設定](#configurability)。

## <a name="rule-description"></a>規則描述

參數和成員的名稱最好用於傳達其意義說明其預期由開發工具所提供的類型。 名稱的成員，如果必須使用資料型別名稱，而不是特定語言使用的語言無關的名稱。 比方說，而不是C#型別名稱`int`，使用的語言無關的資料型別名稱，而`Int32`。

每個離散的權杖參數或成員的名稱已針對下列語言專屬的資料型別名稱不區分大小寫的方式：

- Bool
- WChar
- Int8
- UInt8
- Short
- UShort
- Int
- UInt
- 整數
- UInteger
- Long
- ULong
- 不帶正負號
- 簽署人
- 浮動
- Float32
- Float64

此外，參數的名稱也使核對下列的語言無關的資料型別名稱不區分大小寫的方式：

- Object
- Obj
- Boolean
- Char
- String
- SByte
- Byte
- UByte
- Int16
- UInt16
- Int32
- UInt32
- Int64
- UInt64
- IntPtr
- ptr
- Pointer
- UInptr
- UPtr
- UPointer
- Single
- Double
- Decimal
- Guid

## <a name="how-to-fix-violations"></a>如何修正違規

**如果針對參數引發：**

進一步描述其意義的詞彙或更泛型的詞彙如 'value' 取代參數名稱的資料類型識別項。

**如果成員針對引發：**

語言特定資料型別識別項，該成員的名稱取代為一個詞彙，進一步說明其意義、 語言獨立對等項目或更泛型的詞彙如 'value'。

## <a name="when-to-suppress-warnings"></a>隱藏警告的時機

偶爾使用的類型為基礎的參數和成員的名稱可能是適當的。 不過，對於新的開發，沒有已知您應該在其中隱藏此規則的警告發生的案例。 如先前所提供的程式庫，您可能必須隱藏此規則的警告。

## <a name="configurability"></a>設定功能

如果您執行這項規則，從[FxCop 分析器](install-fxcop-analyzers.md)（而不是透過靜態程式碼分析），您可以設定的哪些部分您程式碼基底上執行這項規則，根據其存取範圍。 比方說，若要指定執行規則時，應該只針對非公用 API 介面，將下列索引鍵 / 值組新增至專案中的.editorconfig 檔案：

```
dotnet_code_quality.ca1720.api_surface = private, internal
```

此類別 （命名） 中，您可以設定此選項，只是這項規則，所有規則，或所有的規則。 如需詳細資訊，請參閱 <<c0> [ 設定的 FxCop 分析器](configure-fxcop-analyzers.md)。

## <a name="related-rules"></a>相關的規則

- [CA1709:識別項應該使用正確的大小寫](../code-quality/ca1709-identifiers-should-be-cased-correctly.md)
- [CA1708:識別項應該不僅為大小寫不同](../code-quality/ca1708-identifiers-should-differ-by-more-than-case.md)
- [CA1707:識別項不應該包含底線](../code-quality/ca1707-identifiers-should-not-contain-underscores.md)
- [CA1719:參數名稱不應該和成員名稱相符](../code-quality/ca1719-parameter-names-should-not-match-member-names.md)