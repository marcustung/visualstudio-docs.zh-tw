---
title: HOW TO：設定 ClickOnce 發行版本 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- ClickOnce deployment, setting publish version
- publishing, ClickOnce
- Publish Version property
ms.assetid: 06f15504-6385-40a6-b01d-cd90ca36dc73
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: bca76d104550a8607de82c9092f57d43c027e63c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60104471"
---
# <a name="how-to-set-the-clickonce-publish-version"></a>HOW TO：設定 ClickOnce 發行版本
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] `Publish Version`屬性會決定是否要發行的應用程式將會被視為更新。 每個階段的版本會遞增，將更新的形式發行應用程式。  
  
 `Publish Version`上設定屬性**發佈**頁面**專案設計工具**。  
  
> [!NOTE]
>  沒有專案 選項，將會自動遞增`Publish Version`屬性每次發行應用程式時，預設會啟用此選項。 如需詳細資訊，請參閱[如何：自動累加 ClickOnce 的發佈版本](../deployment/how-to-automatically-increment-the-clickonce-publish-version.md)。  
  
### <a name="to-change-the-publish-version"></a>若要變更的發行版本  
  
1. 選取方案總管 中的專案，然後按一下 [專案]  功能表中的 [屬性] 。  
  
2. 按一下 [發佈] 索引標籤。  
  
3. 在 **發行版本**欄位中，遞增**主要**，**次要**，**建置**，或**修訂**版本數字。  
  
    > [!NOTE]
    >  您應該永遠不會遞減版本號碼;因此，這麼做可能會造成無法預期的更新行為。  
  
## <a name="see-also"></a>另請參閱  
 [選擇 ClickOnce 更新策略](../deployment/choosing-a-clickonce-update-strategy.md)   
 [如何：自動累加 ClickOnce 的發行版本](../deployment/how-to-automatically-increment-the-clickonce-publish-version.md)   
 [發佈 ClickOnce 應用程式](../deployment/publishing-clickonce-applications.md)   
 [如何：使用 [發佈精靈] 發佈 ClickOnce 應用程式](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
