---
title: 程式行檢視 - 取樣資料 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Lines view
ms.assetid: 46497249-c797-42c5-a02c-3e4bb3b4ee60
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d0f527d6f12d841175afbaff0e653b817250cb4c
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/21/2019
ms.locfileid: "56625175"
---
# <a name="lines-view---sampling-data"></a>程式行檢視 - 取樣資料
取樣資料的 [程式行] 檢視會針對在執行分析期間收集樣本時執行的陳述式，列出效能資料。

> [!NOTE]
>  Windows 8 和 Windows Server 2012 增強式安全性功能需要的重大變更，會以 Visual Studio 分析工具在這些平台收集資料的方式表現。 UWP App 也需要新的收集技術。 請參閱 [Windows 8 和 Windows Server 2012 應用程式的效能工具](../profiling/performance-tools-on-windows-8-and-windows-server-2012-applications.md)。

 在原始程式檔中，陳述式在原始程式檔中可以長達多行，而單一行程式也可能包含一個以上的陳述式。 陳述式是由下列項目識別：

- 包含此函式陳述式的原始程式檔。

- 包含此陳述式的函式。

- 此陳述式在原始程式檔中開始的行位置。

- 此陳述式在原始程式檔中開始的字元。

- 此陳述式在原始程式檔中結束的行位置。

- 此陳述式在原始程式檔中結束的字元。

  [程式行名稱] 資料行提供識別項資料的可排序串連。

  根據定義，陳述式不會呼叫其他函式。 因此只會列出互斥值。

|資料行|說明|
|------------|-----------------|
|**處理序 ID**|分析執行的處理序 ID (PID)。|
|**處理序名稱**|處理序的名稱。|
|**模組名稱**|包含該函式行的模組名稱。|
|**模組路徑**|包含該函式行的模組路徑。|
|**原始程式檔**|包含此函式行的原始程式檔。|
|**函式名稱**|函式的名稱。|
|**函式行號**|原始程式檔中這個函式的開頭行號。|
|**函式位址**|函式的開始位址。|
|**原始程式碼開頭行**|收集這個樣本的原始程式檔中的起始行號。|
|**原始程式碼結尾行**|收集這個樣本的原始程式檔中的結尾行號。|
|**原始程式碼開頭字元**|收集這個樣本的原始程式檔行中，起始字元的位移。|
|**原始程式碼結尾字元**|收集這個樣本的原始程式檔行中，結尾字元的位移。|
|**程式行名稱**|分析工具產生的程式行識別項，該程式行使用下列語法：`Source File`**;[**`Line Number Start`**,**`Character Start`**]->;[**`Line Number End`**,**`Character End`**]**|
|**專有樣本**|當正在執行函式行時所收集的總樣本數。|
|**專有樣本 %**|執行分析期間，執行函式行時所收集的所有樣本的百分比。|

## <a name="see-also"></a>另請參閱
- [程式行檢視 - 取樣](../profiling/lines-view-dotnet-memory-sampling-data.md)