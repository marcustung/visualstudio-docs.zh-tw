---
title: HOW TO：變更發行 ClickOnce 應用程式的語言 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- Publish language property
- ClickOnce deployment, changing publish language
- publishing, ClickOnce
ms.assetid: ef5024c4-cda1-4970-bc75-32a2a10c92c3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7e5bf51fd416fd9ccbb2343c17412984858429da
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60115285"
---
# <a name="how-to-change-the-publish-language-for-a-clickonce-application"></a>HOW TO：變更 ClickOnce 應用程式的發佈語言

發佈時[!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)]應用程式，在安裝語言與您的開發電腦的文化特性的預設值時顯示的使用者介面。 如果您要發行當地語系化的應用程式，您必須指定語言和文化特性，以符合當地語系化的版本。 這取決於`Publish language`專案的屬性。

`Publish language`屬性可以在中設定**發行選項**對話方塊中，從可存取**發行**頁面**專案設計工具**。

> [!NOTE]
>  根據您目前使用的設定或版本，您所看到的對話方塊與功能表命令可能會與 [說明] 中描述的不同。 若要變更設定，請從 [ **工具** ] 功能表中選取 [ **匯入和匯出設定** ]。 如需詳細資訊，請參閱[重設設定](../ide/environment-settings.md#reset-settings)。

## <a name="to-change-the-publish-language"></a>若要變更的發行語言

1. 在方案總管 中選取專案之後，按一下 [專案]  功能表中 [屬性] 。

2. 按一下 [發佈] 索引標籤。

3. 按一下 **選項** 按鈕以開啟**發行選項** 對話方塊。

4. 按一下 **描述**。

5. 在 **發行選項**對話方塊方塊、 選取語言和文化特性，從**發行語言**下拉式清單中，然後再按一下**確定**。

## <a name="see-also"></a>另請參閱

- [發佈 ClickOnce 應用程式](../deployment/publishing-clickonce-applications.md)
- [如何：使用 [發佈精靈] 發佈 ClickOnce 應用程式](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)