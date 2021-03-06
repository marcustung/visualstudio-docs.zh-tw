---
title: 停用 Debugger for Windows Workflow Foundation （舊版） |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- workflows, disabling debugger
- debugging workflows, disabling debugger
- workflow debugger, disabling
ms.assetid: 9da96d0e-f941-4fa9-a1a5-6bab50adfec9
caps.latest.revision: 6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e5065de4ec0217123f76eb23d32bcb0facd25dcc
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58941328"
---
# <a name="disabling-the-visual-studio-debugger-for-windows-workflow-foundation-legacy"></a>停用 Visual Studio Debugger for Windows Workflow Foundation (舊版)
本主題描述在舊版 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 中建置 [!INCLUDE[wf](../includes/wf-md.md)] 應用程式時，如何透過組態檔停用 [!INCLUDE[wfd1](../includes/wfd1-md.md)] 偵錯工具。 當您需要以 [!INCLUDE[wfd2](../includes/wfd2-md.md)] 或 [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] 為目標時，請使用舊版 [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)]。

 根據預設，將會針對主機處理序啟用 [!INCLUDE[vs_current_long](../includes/vs-current-long-md.md)] Debugger for [!INCLUDE[wf](../includes/wf-md.md)]。 若要停用工作流程偵錯，您必須明確地將它關閉將"DisableWorkflowDebugging"項目新增**\<交換器 >** 中的項目 **\<system.diagnostics >** 主機組態檔區段。

 下列範例顯示如何修改主機組態檔來停用工作流程偵錯。

```
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
   <system.diagnostics>
      <switches>
         <add name="DisableWorkflowDebugging" value="true"/>
      </switches>
   </system.diagnostics>
</configuration>
```

## <a name="see-also"></a>另請參閱
 [叫用 Visual Studio Debugger for Windows Workflow Foundation （舊版）](../workflow-designer/invoking-the-visual-studio-debugger-for-windows-workflow-foundation-legacy.md) [偵錯舊版工作流程](../workflow-designer/debugging-legacy-workflows.md)