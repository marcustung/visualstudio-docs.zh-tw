---
title: HOW TO：指定 Visual Studio 2015 複製的檔案位置 |Microsoft Docs
titleSuffix: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- publishing, specifying location
- Publish Location property
ms.assetid: 6c552700-dda3-49fe-af98-4717344fda07
caps.latest.revision: 14
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 6b9f44f3d4f1a9d1b110501d0178e0e2e8dc4e47
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58945341"
---
# <a name="how-to-specify-where-visual-studio-copies-the-files"></a>HOW TO：指定 Visual Studio 複製檔案的位置
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

當您使用 ClickOnce 發行應用程式時，`Publish Location`屬性會指定放置應用程式檔案和資訊清單的位置。 這可以是檔案路徑或 FTP 伺服器的路徑。

 您可以在 [專案設計工具] 的 [發佈] 頁面上，或使用 [發佈精靈] 來指定 `Publish Location` 屬性。 如需詳細資訊，請參閱[如何：使用發佈精靈發佈 ClickOnce 應用程式](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)。

> [!NOTE]
>  當您使用 ClickOnce 安裝多個版本的應用程式時，安裝會將舊版應用程式移至您指定之發行位置中名為 Archive 的資料夾。 以這種方式封存先前的版本可將安裝目錄與舊版的資料夾分開。

### <a name="to-specify-a-publishing-location"></a>指定發行位置

1. 在方案總管 中選取專案之後，按一下 [專案]  功能表中 [屬性] 。

2. 按一下 [發佈] 索引標籤。

3. 在 [發佈位置] 欄位中，使用下列其中一種格式輸入發佈位置：

   - 若要發行至檔案共用或磁碟路徑，請使用 UNC 路徑中輸入的路徑 (\\\Server\ApplicationName) 或檔案路徑 (C:\Deploy\ApplicationName)。

   - 若要發行至 FTP 伺服器，請使用 ftp://ftp.microsoft.com/ApplicationName 格式來輸入路徑。

     請注意，文字必須出現在 [發佈位置] 方塊中才能讓 [瀏覽] (**...**) 按鈕運作。

## <a name="see-also"></a>另請參閱
 [發行 ClickOnce 應用程式](../deployment/publishing-clickonce-applications.md) [How to:使用 [發佈精靈] 發佈 ClickOnce 應用程式](../deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard.md)
