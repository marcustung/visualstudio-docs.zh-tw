---
title: SccCloseProject 函式 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- SccCloseProject
helpviewer_keywords:
- SccCloseProject function
ms.assetid: 259c2069-d349-4814-810f-1c3151b7fb84
caps.latest.revision: 16
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: aebc9d43ebf712d8add7e2aee4f7884ef2754da6
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47486342"
---
# <a name="scccloseproject-function"></a>SccCloseProject 函式
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主題的最新的版本可從[SccCloseProject 函式](https://docs.microsoft.com/visualstudio/extensibility/scccloseproject-function)。  
  
此函式會關閉專案時，標示特定的工作階段結束。  
  
## <a name="syntax"></a>語法  
  
```cpp#  
SCCRTN SccCloseProject (  
   LPVOID pvContext  
);  
```  
  
#### <a name="parameters"></a>參數  
 pvContext  
 原始檔控制外掛程式的內容結構。  
  
## <a name="return-value"></a>傳回值  
 此函式的原始檔控制外掛程式實作應該會傳回下列值之一：  
  
|值|描述|  
|-----------|-----------------|  
|SCC_OK|已成功關閉專案。|  
|SCC_E_PROJNOTOPEN|沒有任何專案目前開啟。|  
|SCC_E_NOTAUTHORIZED|若要執行這項作業不允許的使用者。|  
|SCC_E_NONSPECIFICERROR|不明確的失敗。|  
  
## <a name="remarks"></a>備註  
 [SccOpenProject](../extensibility/sccopenproject-function.md)一定會呼叫此函式前面。 呼叫此函式接下來是呼叫`SccOpenProject`函式或[SccUninitialize](../extensibility/sccuninitialize-function.md)，完全結束原始檔控制系統的連線。  
  
## <a name="see-also"></a>另請參閱  
 [原始檔控制外掛程式 API 函式](../extensibility/source-control-plug-in-api-functions.md)   
 [SccOpenProject](../extensibility/sccopenproject-function.md)   
 [SccInitialize](../extensibility/sccinitialize-function.md)
