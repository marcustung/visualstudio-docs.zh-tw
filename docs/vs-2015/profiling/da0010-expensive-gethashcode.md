---
title: DA0010：GetHashCode 高度耗費資源 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DAExpensiveGetHashCode
- vs.performance.DA0010
- vs.performance.rules.DA0010
- vs.performance.10
ms.assetid: 3987e21a-5b4f-45e4-8a33-6b3f0a472c08
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 1055136562d59412a6187524dc6023c55ef2dc3c
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2019
ms.locfileid: "59659029"
---
# <a name="da0010-expensive-gethashcode"></a>DA0010：GetHashCode 高度耗費資源
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

如需 Visual Studio 的最新文件，請參閱[DA0010:昂貴的 GetHashCode](https://docs.microsoft.com/visualstudio/profiling/da0010-expensive-gethashcode)。  

|||  
|-|-|  
|規則 ID|DA0010|  
|分類|.NET Framework 使用方式|  
|分析方法|取樣<br /><br /> .NET 記憶體|  
|訊息|GetHashCode 函式應該便宜，而且不會配置任何記憶體。 盡可能降低雜湊碼函式的複雜度。|  
|訊息類型|警告|  
  
## <a name="cause"></a>原因  
 類型的 GetHashCode 方法呼叫大部分是分析資料，或方法會配置記憶體。  
  
## <a name="rule-description"></a>規則描述  
 雜湊是一種技術，可快速尋找大型集合中的特定項目。 雜湊表可以很大，且必須支援高比率的存取，因為雜湊表應該非常有效率。 這項需求的含意在於 .NET Framework 中的 GetHashCode 方法不應該配置記憶體。 配置記憶體時會增加記憶體回收行程的負載，而且在因配置要求而需要執行記憶體回收時公開潛在延遲方法。  
  
## <a name="how-to-fix-violations"></a>如何修正違規  
 降低方法的複雜性。
