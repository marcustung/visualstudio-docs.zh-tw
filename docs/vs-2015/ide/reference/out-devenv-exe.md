---
title: -Out (devenv.exe) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
- errors [Visual Studio], builds
- Devenv, /out switch
- builds [Visual Studio], logs
- error logs [Visual Studio], command-line build errors
- error logs [Visual Studio]
- /out Devenv switch
- out Devenv switch
- builds [Visual Studio], errors
- output files, build errors
ms.assetid: 9002d8c2-36d4-451c-b489-8f01932f31f7
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e1f20b446d355ea0cbc6700de5f2e6f79de51d09
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MTE95
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2019
ms.locfileid: "59647057"
---
# <a name="out-devenvexe"></a>/Out (devenv.exe)
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

指定檔案以在您執行、建置、重建或部署解決方案時儲存及顯示錯誤。  
  
## <a name="syntax"></a>語法  
  
```  
devenv /out FileName  
```  
  
## <a name="arguments"></a>引數  
 `FileName`  
 必要項。 當您建置可執行檔時要接收錯誤的檔案路徑和名稱。  
  
## <a name="remarks"></a>備註  
 如果指定不存在的檔名，會自動建立該檔案。 如果檔案已經存在，則結果會附加至檔案的現有內容。  
  
 命令列建置錯誤顯示在 [命令] 視窗與 [輸出] 視窗的 [解決方案產生器] 檢視。 如果您正在執行自動建置，而且需要查看結果，這個選項非常有用。  
  
## <a name="example"></a>範例  
 這個範例會執行 `MySolution` 並將錯誤寫入至檔案 `MyErrorLog.txt`。  
  
```  
devenv /run "C:\Documents and Settings\someuser\My Documents\Visual Studio\Projects\MySolution\MySolution.sln" /out "C:\MyErrorLog.txt"  
```  
  
## <a name="see-also"></a>請參閱  
 [Devenv 命令列參數](../../ide/reference/devenv-command-line-switches.md)   
 [/Run (devenv.exe)](../../ide/reference/run-devenv-exe.md)   
 [/Build (devenv.exe)](../../ide/reference/build-devenv-exe.md)   
 [/Rebuild (devenv.exe)](../../ide/reference/rebuild-devenv-exe.md)   
 [/Deploy (devenv.exe)](../../ide/reference/deploy-devenv-exe.md)
