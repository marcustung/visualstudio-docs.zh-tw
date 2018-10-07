---
title: 安全性頁面、專案設計工具 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-general
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vb.ProjectPropertiesSecurity
- vb.XBAPProjectPropertiesSecurity
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Project Designer, Security page
- Security page in Project Designer
ms.assetid: 641d9cd3-fa07-498a-8568-3c169bb4d3d5
caps.latest.revision: 40
author: gewarren
ms.author: gewarren
manager: ghogen
ms.openlocfilehash: fb9047f0fb3ebf3eb582220ec91d08612b8b9bca
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47499451"
---
# <a name="security-page-project-designer"></a>專案設計工具、安全性頁
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

本主題的最新的版本可從[安全性 Page，Project Designer](https://docs.microsoft.com/visualstudio/ide/reference/security-page-project-designer)。  
  
  
[專案設計工具] 的 [安全性] 頁面是用於設定使用 [!INCLUDE[ndptecclick](../../includes/ndptecclick-md.md)] 部署所部署之應用程式的程式碼存取安全性設定。 如需詳細資訊，請參閱 [ClickOnce 應用程式的程式碼存取安全性](../../deployment/code-access-security-for-clickonce-applications.md)。  
  
 若要存取 [安全性] 頁面，請選取方案總管中的專案節點，然後按一下 [專案] 功能表上的 [屬性]。 [專案設計工具] 出現時，請按一下 [安全性] 索引標籤。  
  
## <a name="security-settings"></a>安全性設定  
 **啟用 ClickOnce 安全性設定**  
 決定是否在設計階段啟用安全性設定。 清除這個選項後，就無法使用 [安全性] 頁面上的所有其他選項。  
  
> [!NOTE]
>  當您使用 [發行精靈] 發佈應用程式時，會自動啟用此選項。  
  
 選取此選項後，就可以選取兩個選項按鈕的其中之一：[這是完全信任的應用程式] 或 [這是部分信任的應用程式]。  
  
 WPF 網頁瀏覽器應用程式專案預設選取此選項。  
  
 所有其他專案類型則預設清除此選項。  
  
 **這是完全信任的應用程式**  
 如果選取此選項，在用戶端電腦上安裝或執行應用程式時，應用程式會要求完全信任權限。 可能的話，請避免使用完全信任，因為這會授權應用程式完全不受限制地存取資源，例如檔案系統和登錄。  
  
 根據預設，WPF 網頁瀏覽器應用程式專案的這個選項設為部分信任。  
  
 所有其他專案類型的這個選項則預設為完全信任。  
  
 **這是部分信任的應用程式**  
 如果選取此選項，在用戶端電腦上安裝或執行應用程式時，應用程式會要求部分信任權限。 「部分信任」表示只會執行要求程式碼存取安全性權限下允許的動作。 如需如何設定安全性權限的詳細資訊，請參閱 [ClickOnce 應用程式的程式碼存取安全性](../../deployment/code-access-security-for-clickonce-applications.md)。  
  
 您可以在 [ClickOnce 安全性權限] 區域中設定選項，指定部分信任的安全性設定。  
  
## <a name="clickonce-security-permissions"></a>ClickOnce 安全性權限  
 **安裝應用程式的區域**  
 指定預設的程式碼存取安全性權限集。 為受限的權限集選擇 [網際網路] 或 [近端內部網路]，或選擇[(自訂)] 設定自訂的權限集。 如果應用程式要求高於區域中授與的權限，即會顯示 ClickOnce 信任提示，提示使用者授與其他權限。 如需如何設定安全性權限的詳細資訊，請參閱 [ClickOnce 應用程式的程式碼存取安全性](../../deployment/code-access-security-for-clickonce-applications.md)。  
  
 根據預設，WPF 網頁瀏覽器應用程式專案的這個選項設為 [網際網路]。  
  
 **編輯權限 XML**  
 開啟應用程式資訊清單範本 (app.manifest) 設定 [(自訂)] 權限集的權限。  
  
 **進階**  
 開啟 [[進階安全性設定] 對話方塊](../../ide/reference/advanced-security-settings-dialog-box.md)，這是用來設定以限制權限偵錯應用程式的設定。 偵錯期間會檢查這些設定，權限例外狀況會指出應用程式可能需要比在區域中定義更高的權限。  
  
## <a name="see-also"></a>另請參閱  
 <xref:System.Security.Permissions.WebBrowserPermission>   
 <xref:System.Security.Permissions.MediaPermission>   
 [ClickOnce 應用程式的程式碼存取安全性](../../deployment/code-access-security-for-clickonce-applications.md)   
 [如何：啟用 ClickOnce 安全性設定](../../deployment/how-to-enable-clickonce-security-settings.md)   
 [如何：設定 ClickOnce 應用程式的安全性區域](../../deployment/how-to-set-a-security-zone-for-a-clickonce-application.md)   
 [如何：設定 ClickOnce 應用程式的自訂使用權限](../../deployment/how-to-set-custom-permissions-for-a-clickonce-application.md)   
 [如何：以限制權限偵錯 ClickOnce 應用程式](../../deployment/how-to-debug-a-clickonce-application-with-restricted-permissions.md)   
 [ClickOnce 安全性和部署](../../deployment/clickonce-security-and-deployment.md)   
 [專案屬性參考](../../ide/reference/project-properties-reference.md)   
 [進階安全性設定對話方塊](../../ide/reference/advanced-security-settings-dialog-box.md)


