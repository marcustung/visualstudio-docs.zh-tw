---
title: 程式節點 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- program nodes, debugging context
- debugging [Debugging SDK], program nodes
- program nodes, adding
- program nodes, superceding
ms.assetid: 1c5a5c13-c14d-42c3-af11-4c63f1032c8d
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3a06be4ef0a69ec173f171ba202f1f479448b1ca
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58941925"
---
# <a name="program-nodes"></a>程式節點
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

偵錯工具就架構而言，**計劃節點**:  
  
- 是輕量型程式的描述。  
  
- 可以識別本身和它正在執行中，並可以附加至要卸離，並說明如果有的話，請建立它，偵錯引擎 (DE) 的程序。  
  
- 由[IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md)介面，通常由 DE 或連接埠。 藉由呼叫程式的節點加入至連接埠[AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)。 當程式節點加入至連接埠時，它會加入包含此程式節點所表示的程式處理序。  
  
  啟動偵錯工作階段的一段時間，可根據的偵錯封裝，實作後程式節點用來建立對應的程式。 當查詢其程式的處理程序，就會列舉程式，一個用於每個程式節點。  
  
  程式附加到之前，IDE 會要求程式的輕量級描述。 從 [程式] 節點，就可以取得此資訊。 在程式附加至時，IDE 就必須顯示更詳細的資訊，例如執行程式中的所有執行緒的清單。 這項資訊被取自程式本身。  
  
## <a name="see-also"></a>另請參閱  
 [程式](../../extensibility/debugger/programs.md)   
 [處理程序](../../extensibility/debugger/processes.md)   
 [偵錯引擎](../../extensibility/debugger/debug-engine.md)   
 [偵錯工具概念](../../extensibility/debugger/debugger-concepts.md)   
 [IDebugProgramNode2](../../extensibility/debugger/reference/idebugprogramnode2.md)   
 [AddProgramNode](../../extensibility/debugger/reference/idebugportnotify2-addprogramnode.md)
