---
title: 如何： 使用 編輯後繼續 (C#) |Microsoft Docs
ms.date: 10/04/2018
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- Edit and Continue [C#], about Edit and Continue
ms.assetid: 40e136d8-a08c-43bd-b313-fb821c55eb3c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 515068f29045ef92ee7d2323f752ba2185f28cac
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56696346"
---
# <a name="how-to-use-edit-and-continue-c"></a>如何：使用編輯後繼續 (C#)
編輯後繼續，您可以進行，並將變更套用至您的程式碼在中斷模式中，偵錯時，而不需要停止並重新啟動偵錯工作階段。

編輯後繼續C#會在自動發生，當您在中斷模式中進行程式碼變更，然後繼續使用偵錯**繼續**，**步驟**，或**設定下一個陳述式**，或評估在偵錯工具視窗中的函式。

如需詳細資訊，請參閱 <<c0> [ 編輯後繼續 (Visual C#)](../debugger/edit-and-continue-visual-csharp.md)。</c0>

>[!NOTE]
>編輯後繼續的最佳化，不支援混用，或 SQL Server common language runtime (CLR) 整合程式碼。 如需其他不支援的案例，請參閱[支援的程式碼變更 (C#和 Visual Basic)](../debugger/supported-code-changes-csharp.md)。 如果您嘗試編輯後繼續使用這些案例的其中一個時，出現訊息方塊，指出不支援 編輯後繼續。

**若要啟用或停用編輯後繼續：**

1. 如果您是在偵錯工作階段中，停止偵錯 (**偵錯** > **停止偵錯**或是**Shift**+**F5**).

1. 在 **工具** > **選項**(或**偵錯** > **選項**) >**偵錯** > **一般**，選取或清除**啟用編輯後繼續**核取方塊。

當您啟動或重新啟動偵錯工作階段時，這個設定會生效。

**若要使用 編輯後繼續：**

1. 偵錯時，在中斷模式，請對原始程式碼進行變更。

1. 從**偵錯**功能表上，按一下**繼續**，**步驟**，或**設定下一個陳述式**，或評估在偵錯工具視窗中的函式。

   使用新的已編譯程式碼會繼續偵錯。

編輯後繼續不支援某些類型的程式碼變更。 如需詳細資訊，請參閱 <<c0> [ 支援的程式碼變更 (C#和 Visual Basic)](../debugger/supported-code-changes-csharp.md)。</c0>
