---
title: 錯誤： SQL 可以&#39;t 找不到 SSDEBUGPS |Microsoft Docs
ms.date: 11/04/2016
ms.topic: troubleshooting
f1_keywords:
- vs.debug.error.sqlde_cant_find_ssdebugps
dev_langs:
- CSharp
- VB
- FSharp
- C++
- SQL
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 854105ea5d94f6d3b09ce73a23ec45ccab9e797c
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56694162"
---
# <a name="error-sql-can39t-find-ssdebugps"></a>錯誤： SQL 可以&#39;t 找不到 SSDEBUGPS

SSDEBUGPS.dll 是 SQL Server 偵錯主機元件。

當您嘗試啟動偵錯時會發生這個錯誤，並表示指定的檔案不在 [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] 電腦上。 可能的原因是從未執行遠端偵錯 (Remote Debugging) 安裝程式，或者已刪除這個檔案。

有兩個方法可以解決這個錯誤：一是重新執行遠端偵錯安裝程式，二是將該檔案複製到 [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] 電腦。

若要重新執行遠端偵錯安裝程式，請遵循指示[遠端偵錯](../debugger/remote-debugging.md)。

如果找得到 ssdebugps.dll 的複本，就可以將該複本複製到 [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] 電腦。 如果有這個檔案，會在 \Program Files\ Common Files\Microsoft Shared\SQL Debugging 目錄中。 您可能會發現它在另一個[!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)]機器，或已安裝 Visual Studio 2005 的電腦上。

將 SSDEBUGPS.dll 複製到 SQL Server 2005 電腦：

1. 將該檔案複製到 [!INCLUDE[sqprsqlong](../debugger/includes/sqprsqlong_md.md)] 電腦上具有相同名稱和路徑的目錄。

2. 開啟 [命令提示字元] 並執行下列命令，即可登錄該檔案：

    ```cmd
    regsvr32 ssdebugps.dll
    ```
