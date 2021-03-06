---
title: 升級的.mdf 檔案 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- SQL Server Express
- SQL Server LocalDB
- LocalDB
- SQLEXPRESS
- upgrading SQLExpress to SQLExpress
- upgrading to LocalDB
ms.assetid: 14ca6f76-f80e-4926-8020-3fee2d802b75
caps.latest.revision: 36
author: gewarren
ms.author: gewarren
manager: jillfra
robots: noindex,nofollow
ms.openlocfilehash: 395e2a6233c1b6187d9089459cb8f267c4c3c904
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60079904"
---
# <a name="upgrade-mdf-files"></a>升級 .mdf 檔案
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主題說明在您安裝新版的 Visual Studio 之後，升級您的資料庫檔案 (.mdf) 的選項。 它包含下列工作的指示：  
  
- 升級使用較新版的 SQL Server Express LocalDB 資料庫檔案  
  
- 升級使用較新版本的 SQL Server Express 資料庫檔案  
  
- 使用 Visual Studio 中的資料庫檔案，但會保留與較舊版本的 SQL Server Express 或 LocalDB 的相容性  
  
- 讓 SQL Server Express 的預設資料庫引擎  
  
  您可以使用 Visual Studio 中開啟專案，其中包含使用較舊版本的 SQL Server Express 或 LocalDB 所建立的資料庫檔案 (.mdf)。 不過，若要繼續開發您的專案在 Visual Studio 中，您必須擁有 SQL Server Express 或 LocalDB 與 Visual Studio 中，相同的電腦上安裝該版本，或您必須先升級資料庫檔案。 如果您升級資料庫檔案時，您將無法存取使用舊版的 SQL Server Express 或 LocalDB。  
  
  您可能也會提示您升級資料庫檔案，如果檔案的版本不相容的 SQL Server Express 或目前已安裝的 LocalDB 執行個體，透過 SQL Server Express 或 LocalDB 的較早版本所建立的。 若要解決此問題，Visual Studio 會提示您升級的檔案。  
  
> [!IMPORTANT]
>  我們建議您在升級之前先備份資料庫檔案。  
  
> [!WARNING]
>  如果您升級 LocalDB 2014 (V12) 至 LocalDB 2016 (V13) 的 32 位元中所建立的.mdf 檔案時，您無法在 32 位元版本的 LocalDB 中再次開啟該檔案。  在 Update 2 中，LocalDB V13 會是 64 位元。  
  
 您將資料庫升級之前，請考慮下列準則：  
  
- 如果您想要使用舊版和新版的 Visual Studio 中的專案，請不要升級。  
  
- 如果您的應用程式將用於在環境中使用 SQL Server Express 而非 LocalDB，請不要升級。  
  
- 請不要升級應用程式所使用的遠端連線，如果因為 LocalDB 不接受這些條款。  
  
- 如果您的應用程式都需要網際網路資訊服務 (IIS) 上，不要升級。  
  
- 如果您想要在沙箱環境中測試資料庫應用程式，但不想要管理資料庫，請考慮升級。  
  
### <a name="to-upgrade-a-database-file"></a>若要升級的資料庫檔案  
  
1. 在 [**伺服器總管**，選取**連接到資料庫**] 按鈕。  
  
2. 在 **加入連接**對話方塊方塊中，指定下列資訊：  
  
   - **資料來源**：`Microsoft SQL Server (SqlClient)`  
  
   - **伺服器名稱**：  
  
       - 若要使用的預設版本： `(localdb)\MSSQLLocalDB`。  這會指定 ProjectV12 或 ProjectV13，取決於已安裝的 Visual Studio 版本，並建立第一個的 LocalDB 執行個體時。 **MSSQLLocalDB**中的節點**SQL Server 物件總管**哪一個版本指向所示。  
  
       - 若要使用特定版本：`(localdb)\ProjectsV12`或`(localdb)\ProjectsV13`，其中 V12 是 LocalDB 2014 而 V13 是 LocalDB 2016。  
  
   - **附加資料庫檔案**:主要.mdf 檔案的實體路徑。  
  
   - **邏輯名稱**:您想要使用的檔案名稱。  
  
3. 選取 [確定] 按鈕。  
  
4. 當系統提示您時，選取**是**升級檔 按鈕。  
  
   資料庫會升級、 附加至 LocalDB 資料庫引擎，且不再與較舊的 LocalDB 版本相容。  
  
   您也可以修改 SQL Server Express 要使用的連線 LocalDB 開啟連接的捷徑功能表，然後選取**修改連接**。 在 **修改連接**對話方塊方塊中，變更伺服器名稱以`(LocalDB)\MSSQLLocalDB`。 在 **進階屬性**對話方塊方塊中，請確定**使用者執行個體**設定為**False**。  
  
### <a name="to-upgrade-to-a-newer-version-of-sql-server-express"></a>若要升級至較新版本的 SQL Server Express  
  
1. 在資料庫連接的捷徑功能表，選取**修改連接**。  
  
2. 在 [**修改連接**對話方塊中，選取**進階**] 按鈕。  
  
3. 在 **進階屬性**對話方塊中，選取**確定**按鈕不會變更伺服器名稱。  
  
   資料庫檔案會升級到符合目前的 SQL Server Express 版本。  
  
### <a name="to-work-with-the-database-in-visual-studio-but-retain-compatibility-with-sql-server-express"></a>若要使用 Visual Studio 中的資料庫，但保留與 SQL Server Express 的相容性  
  
- 在 Visual Studio 中，開啟專案，而不將它升級。  
  
    - 若要執行專案時，選取 F5 鍵。  
  
    - 若要編輯資料庫，開啟 .mdf 檔案的**方案總管 中**，並展開中的節點**伺服器總管**才能使用您的資料庫。  
  
### <a name="to-make-sql-server-express-the-default-database-engine"></a>若要讓 SQL Server Express 的預設資料庫引擎  
  
1. 在功能表列上選取**工具** > **選項**。  
  
2. 在 **選項**對話方塊方塊中，展開**Data Tools**選項，然後再選取**資料連接**節點。  
  
3. 在  **SQL Server 執行個體名稱**文字中，指定的 SQL Server Express 或您想要使用的 LocalDB 執行個體的名稱。 如果不名為執行個體，指定`.\SQLEXPRESS or (localdb)\MSSQLLocalDB`。  
  
4. 選取 [確定] 按鈕。  
  
   SQL Server Express，將會是您的應用程式的預設資料庫引擎。  