---
title: 錯誤：Web 伺服器找不到要求的資源 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- debugger, Web application errors
ms.assetid: 1ceeaf30-918c-42bb-ace1-96944530fef3
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 656ebd6f8b1e720afd129bca3d53712526fc914f
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "59000626"
---
# <a name="error-the-web-server-could-not-find-the-requested-resource"></a>錯誤：Web 伺服器找不到要求的資源
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

基於安全性考量，IIS 已傳回泛型錯誤。  
  
 原因可能是伺服器的安全性組態。 IIS 6.0 (含) 以前版本中使用了一個稱為 URLScan 的附加元件程式，用於篩選出可疑和格式錯誤的要求。 IIS 7.0 內建了要求篩選功能，可達到相同的目的。 在這兩種情況下，太過嚴格的要求篩選可能會阻止 Visual Studio 對伺服器進行偵錯。  
  
 造成這個錯誤的原因可能有很多種。 其中幾個最常見的原因包括 IIS 的安裝或組態、網站組態或檔案系統的權限發生問題。 您可以嘗試使用瀏覽器存取資源。 根據 IIS 的設定方式，您可能需要在伺服器上使用本機瀏覽器或檢查 IIS 錯誤記錄檔，以取得詳細的錯誤訊息。  
  
 如需針對 IIS 進行疑難排解的詳細資訊，請參閱 [IIS 管理與系統管理](http://go.microsoft.com/fwlink/?LinkId=255872)。  
  
## <a name="see-also"></a>另請參閱  
 [UrlScan 安全性工具](https://www.iis.net/downloads/microsoft/urlscan)   
 [錯誤：Web 伺服器已經鎖定，並會封鎖 DEBUG 動詞命令](../debugger/error-the-web-server-has-been-locked-down-and-is-blocking-the-debug-verb.md)
