---
title: 指定套用註釋的時機和位置
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _Group_
- _At_
- _When_
- _At_buffer_
ms.assetid: 8e4f4f9c-5dfa-4835-87df-ecd1698fc650
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 1b94bd5dc40102bce073e42302e92b737b4e8b0d
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55942020"
---
# <a name="specifying-when-and-where-an-annotation-applies"></a>指定套用註釋的時機和位置
條件式註解時，它可能需要指定分析器的其他註解。  例如，如果函式的變數，可以同步或非同步，函式的行為，如下所示：在同步的情況下它一定最終會成功，但在非同步的情況下則會回報錯誤如果無法立即成功。 以同步方式呼叫此函式時，檢查結果值提供以程式碼分析工具的任何值，因為它將不會有傳回。  不過，當以非同步方式呼叫此函式，並不會檢查函式的結果，就可能發生嚴重的錯誤。 此範例說明您可以使用的情況下`_When_`註釋，本文稍後所述，啟用檢查。

## <a name="structural-annotations"></a>結構化註解
 若要控制註釋套用的時機和位置，請使用下列的結構化註解。

|註釋|描述|
|----------------|-----------------|
|`_At_(expr, anno-list)`|`expr` 這會產生左值運算式。 中的註釋`anno-list`套用至物件命名`expr`。 在每個註釋`anno-list`，`expr`如果註解解譯在預先條件，並在後置條件如果註解解譯後置條件中，會將前置條件中解譯。|
|`_At_buffer_(expr, iter, elem-count, anno-list)`|`expr` 這會產生左值運算式。 中的註釋`anno-list`套用至物件命名`expr`。 在每個註釋`anno-list`，`expr`如果註解解譯在前置條件下，並在後置條件如果註解解譯後置條件中，會將前置條件中解譯。<br /><br /> `iter` 是以註解為範圍變數的名稱 (在內`anno-list`)。 `iter` 具有隱含類型`long`。 從評估版，在任何封閉範圍中同名的變數會隱藏起來。<br /><br /> `elem-count` 這是判斷值為整數的運算式。|
|`_Group_(anno-list)`|中的註解`anno-list`全部都視為具有群組註釋套用至每個註釋適用於任何限定詞。|
|`_When_(expr, anno-list)`|`expr` 是可以轉換成運算式`bool`。 當它為非零 (`true`)，括住的註釋`anno-list`會被視為適用於。<br /><br /> 根據預設，在每個註釋`anno-list`，`expr`會解譯為使用輸入的值，如果註解是前置條件，而且如果使用的輸出值註釋是後置條件。 若要覆寫預設值，您可以使用`_Old_`如果內建函式，當您評估以指出應該使用輸入的值後置條件。 **注意：** 可能由於使用啟用不同的註釋`_When_`如果可變動的值 — 比方說， `*pLength`— 因為牽涉到評估的結果的`expr`在前置條件下可能不同於後置條件的評估結果。|

## <a name="see-also"></a>另請參閱

- [使用 SAL 註釋減少 C/C++ 程式碼的缺失](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [了解 SAL](../code-quality/understanding-sal.md)
- [註釋函式參數和傳回值](../code-quality/annotating-function-parameters-and-return-values.md)
- [註釋函式行為](../code-quality/annotating-function-behavior.md)
- [註釋結構和類別](../code-quality/annotating-structs-and-classes.md)
- [註釋鎖定行為](../code-quality/annotating-locking-behavior.md)
- [內建函式](../code-quality/intrinsic-functions.md)
- [最佳做法和範例](../code-quality/best-practices-and-examples-sal.md)