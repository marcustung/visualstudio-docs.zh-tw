---
title: 密碼編譯警告
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: d96723ea-a293-488d-b9db-adb437e50cdd
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 669b7806e01772e6a871b6c6a9bf47907cf9a5a4
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55916852"
---
# <a name="cryptography-warnings"></a>密碼編譯警告
密碼編譯警告透過正確使用加密來支援更安全的程式庫與應用程式。 這些警告有助於防止在程式中出現安全性問題。 如果停用這些警告中的任一個，則您應該清楚地在程式碼中標示理由，同時也要通知指定的安全主管有關您的開發專案。

|規則|描述|
|----------|-----------------|
|[CA5350:請勿使用弱式密碼編譯演算法](../code-quality/ca5350-do-not-use-weak-cryptographic-algorithms.md)|現今，弱式加密演算法和雜湊函式用於多種原因，但它們不應該用來保證所保護資料的機密性或完整性。        此規則會在它在程式碼中發現 TripleDES、SHA1 或 RIPEMD160 演算法時觸發。|
|[CA5351 不要使用中斷的密碼編譯演算法](../code-quality/ca5351-do-not-use-broken-cryptographic-algorithms.md)|中斷的密碼編譯演算法較不安全，強烈建議您不要使用它們。 此規則會在它在程式碼中發現 MD5 雜湊演算法或 DES 或 RC2 加密演算法時觸發。|