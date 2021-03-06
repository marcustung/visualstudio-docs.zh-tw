---
title: IActiveScriptParse | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptParse interface
ms.assetid: 8c967d70-f582-4f64-9e79-49f40c4dcb7c
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a987b4be3430f2ed8b0562f41b51a94797f96dc4
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "58152180"
---
# <a name="iactivescriptparse"></a>IActiveScriptParse
如果 Windows 指令碼引擎允許未經處理的文字加入指令碼的程式碼程式碼片段，或允許在執行階段評估的運算式文字，它會實作`IActiveScriptParse`介面。 解譯的指令碼語言具有無獨立的撰寫環境，例如 VBScript，這會提供替代機制 (而非`IPersist*`) 指令碼進入指令碼引擎，並將附加到各種不同的物件的指令碼片段事件。  
  
## <a name="methods-in-vtable-order"></a>依照 Vtable 順序的方法  
  
|方法|描述|  
|------------|-----------------|  
|[IActiveScriptParse::InitNew](../../winscript/reference/iactivescriptparse-initnew.md)|初始化指令碼引擎。|  
|[IActiveScriptParse::AddScriptlet](../../winscript/reference/iactivescriptparse-addscriptlet.md)|將指令碼中的程式碼的程式碼片段。|  
|[IActiveScriptParse::ParseScriptText](../../winscript/reference/iactivescriptparse-parsescripttext.md)|剖析指定的程式碼程式碼片段，加入宣告至命名空間，並評估為適當的程式碼。|  
  
## <a name="see-also"></a>另請參閱  
 [動態指令碼介面](../../winscript/reference/active-script-interfaces.md)