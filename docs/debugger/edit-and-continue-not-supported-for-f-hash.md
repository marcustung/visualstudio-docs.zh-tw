---
title: 編輯後繼續 不支援F#|Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [F#]
- Debugging [F#], Edit and Continue
ms.assetid: 40ec77bb-07e3-4b58-9254-ae015009441c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ceb0ca767b1ac6364e103925fb86ed639c3d321d
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56680915"
---
# <a name="edit-and-continue-not-supported-for-f"></a>F# 不支援編輯後繼續 #
當您偵錯 F# 程式碼時，不支援 [編輯後繼續]。 在偵錯工作階段期間編輯 F# 程式碼是可行的作法，但應該避免。 偵錯工作階段期間不會套用程式碼變更。 因此，您在偵錯時對 F# 程式碼所做的任何編輯都會導致原始程式碼與正在偵錯的程式碼變成不相符。
