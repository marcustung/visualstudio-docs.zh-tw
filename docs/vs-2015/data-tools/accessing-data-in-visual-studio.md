---
title: 存取資料
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-data-tools
ms.topic: conceptual
f1_keywords:
- "80025080"
dev_langs:
- VB
- CSharp
- C++
- aspx
helpviewer_keywords:
- data [Visual Studio]
- data access [Visual Studio]
- data [C#]
- ADO.NET, data access
ms.assetid: 9812a6d5-23d2-4427-8b98-70a2abfec3bc
caps.latest.revision: 103
author: gewarren
ms.author: gewarren
manager: jillfra
robots: noindex,nofollow
ms.openlocfilehash: 02d40062b1202a261aa7be4ae306329a6a93b37a
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2019
ms.locfileid: "59669454"
---
# <a name="accessing-data-in-visual-studio"></a>在 Visual Studio 中存取資料
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

在 Visual Studio 中，您可以建立連接至幾乎任何的資料庫產品或服務的任何格式、 任何位置中資料的應用程式，在本機電腦上，在區域網路上，或是在公用、 私人或混合式雲端。

 JavaScript、 Python、 PHP、 Ruby 中的應用程式或C++，在取得程式庫，然後撰寫程式碼，執行任何動作，例如連接到資料。 .NET 應用程式，Visual Studio 會提供您可用來瀏覽資料來源，請建立來儲存和管理記憶體中的資料和資料繫結至使用者介面的物件模型的工具。     Microsoft Azure 會提供 Sdk for.NET、 Java、 Node.js、 PHP、 Python、 Ruby 和行動應用程式和在 Visual Studio 中的工具連線至 Azure 儲存體。

 下列清單會顯示幾個可用的許多資料庫和儲存體系統，從 Visual Studio。 [Microsoft Azure](https://azure.microsoft.com/)供應項目是資料服務，其中包含所有的佈建和管理的基礎資料存放區。  [Azure Tools for Visual Studio](https://www.visualstudio.com/features/azure-tools-vs.aspx)是選擇性元件，可讓您能夠直接從 Visual Studio 的 Azure 資料存放區使用。 大部分的其他 SQL 和 NoSQL 資料庫產品，此處會列出可裝載於本機電腦、 區域網路上或在 Microsoft Azure 中的虛擬機器上。 在此案例中，您負責管理資料庫本身。

 **Microsoft Azure**

||||
|-|-|-|
|SQL Database|DocumentDB|儲存體 （blob、 資料表、 佇列、 檔案）|
|SQL 資料倉儲|SQL Server Stretch Database|StorSimple|

 等等...

 **SQL**

||||
|-|-|-|
|SQL Server 2005 – 2016，包括 Express 和 LocalDB|Firebird|MariaDB|
|MySQL|Oracle|PostgreSQL|
|SQLite|||

 等等...

 **NoSQL**

||||
|-|-|-|
|Apache Cassandra|CouchDB|MongoDB|
|NDatabase|OrientDB|RavenDB|
|VelocityDB|||

 等等...

 許多資料庫供應商，以及第三方支援 Visual Studio 整合的 NuGet 套件。 在 nuget.org 上或透過 NuGet 套件管理員在 Visual Studio 中，您可以瀏覽供應項目 (**工具** > **NuGet 套件管理員** > **管理 nuget 封裝方案套件**)。 與 Visual Studio 整合擴充功能為其他資料庫產品。   您可以瀏覽至連線，瀏覽 Visual Studio 組件庫中的這些供應項目**工具** > **擴充功能和更新**，然後選取**線上**方對話方塊的窗格。  如需詳細資訊，請參閱 <<c0> [ 安裝資料庫系統、 工具和範例](../data-tools/installing-database-systems-tools-and-samples.md)。

> [!NOTE]
>  SQL Server 2005 的延長的支援已於 2016 年 4 月 12 日結束。   沒有 data tools 在 Visual Studio 2015 和更新版本會繼續使用 SQL Server 2005，此日期之後無法保證。 如需詳細資訊，請參閱 <<c0> [ 適用於 SQL Server 2005 的結束支援公告](https://www.microsoft.com/sql-server/sql-server-2005)。

### <a name="net-languages"></a>.NET 語言
 所有的.NET 資料存取，包括在.NET Core 中，根據 ADO.NET，一組類別，定義介面來存取任何種類的資料來源、 關聯式和非關聯性。 Visual Studio 有數個工具和設計工具，可以使用 ADO.NET 來協助您連接到資料庫，操作資料，並將資料呈現給使用者。 在本節中的文件說明如何使用這些工具。 您也可以直接用於 ADO.NET 命令物件執行程式。 如需有關直接呼叫 ADO.NET Api 的詳細資訊，請參閱[ADO.NET](https://msdn.microsoft.com/library/e80y5yhx\(v=vs.110\).aspx) MSDN Library 中。

 特別是關於 ASP.NET 資料存取的文件，請參閱 <<c0> [ 使用資料](http://www.asp.net/web-forms/overview/presenting-and-managing-data)ASP.NET 網站上。 如需使用 Entity Framework 搭配 ASP.NET MVC 教學課程，請參閱 < [Getting Started with Entity Framework 6 Code First 使用 MVC 5](http://www.asp.net/mvc/overview/getting-started/getting-started-with-ef-using-mvc/creating-an-entity-framework-data-model-for-an-asp-net-mvc-application)。

 在 C# 或 Visual Basic 中的通用 Windows 平台 (UWP) 應用程式可以使用 Microsoft Azure SDK for.NET 存取 Azure 儲存體和其他 Azure 服務。 Windows.Web.HttpClient 類別可讓您與任何 RESTful 服務的通訊。 如需詳細資訊，請參閱 <<c0> [ 如何連接至 HTTP 伺服器使用 windows.web.http 應用程式開發](https://msdn.microsoft.com/library/windows/apps/dn469430.aspx)。

 在本機電腦上的資料儲存體，建議的方法是使用 SQLite，會在應用程式相同的程序中執行。 如果需要物件關聯式對應 (ORM) 層，您可以使用 Entity Framework。 如需詳細資訊，請參閱 <<c0> [ 資料存取](https://msdn.microsoft.com/windows/uwp/data-access/index)Windows 開發人員中心。

 如果您要連接到 Azure 服務，請務必下載最新[Azure SDK 工具](https://azure.microsoft.com/downloads/)。

#### <a name="data-providers"></a>資料提供者
 要在 ADO.NET 中的資料庫，它必須能夠自訂*ADO.NET 資料提供者*或其他必須公開 （expose） 的 ODBC 或 OLE DB 介面。 Microsoft 提供[ADO.NET 資料提供者清單](https://msdn.microsoft.com/data/dd363565)SQL Server 產品，以及 ODBC 和 OLE DB 提供者。

#### <a name="data-modeling"></a>資料模型化
 在.NET 中，您會有三個選項用於模型化，以及管理記憶體中的資料之後擷取從資料來源,：

 Entity Framework 的慣用的 Microsoft ORM 技術。 您可以針對關聯式資料進行程式設計使用它做為第一級的.NET 物件。 對於新的應用程式，它應該是預設第一個選項，當模型是必要。 它需要從基礎的 ADO.NET 提供者的自訂支援。

 LINQ to SQL 先前產生的物件關聯式對應程式。 它適用於較不複雜的案例，但已不再進行開發。

 資料集最舊的三種模型化技術。 它是主要用於快速開發 「 資料表單 」 應用程式中不是處理大量資料或執行複雜的查詢或轉換。 資料集物件是由以邏輯方式類似於 SQL database 物件更多.NET 物件的 DataTable 和 DataRow 物件所組成。 SQL 資料來源為基礎的應用程式相當簡單，如資料集仍可能是不錯的選擇。

 沒有使用任何這些技術的需求。 在某些情況下，尤其是效能非常重要，您可以只使用 DataReader 物件從資料庫讀取，並將您所需要的值複製到集合物件，例如清單\<T >。

### <a name="native-c"></a>原生 C++
 C++連接到 SQL Server 的應用程式應使用[SQL Server Native Client](https://msdn.microsoft.com/sqlserver/aa937733.aspx)。 您可以使用來存取其他資料庫[ODBC](https://msdn.microsoft.com/library/ms710252\(v=vs.85\).aspx)或直接 OLE DB 驅動程式。 ODBC 是目前的標準資料庫介面，但大部分資料庫系統提供無法透過 ODBC 介面存取的自訂功能。  OLE DB 是舊的 COM 資料存取技術，仍然受到支援，但不是建議用於新的應用程式。  如需詳細資訊，請參閱 <<c0> [ 資料存取](http://msdn.microsoft.com/library/a9455752-39c4-4457-b14e-197772d3df0b)。

 C++使用 REST 服務的程式可以使用[ C++ REST SDK](https://github.com/Microsoft/cpprestsdk)。

 C++使用 Microsoft Azure 儲存體的程式可以使用[Microsoft Azure 儲存體用戶端](http://www.nuget.org/packages/wastorage)。

#### <a name="data-modeling"></a>資料模型化
 Visual Studio 不提供的 ORM 層C++。  [ODB](http://www.codesynthesis.com/products/odb/)是熱門的開放原始碼 ORM，如C++。

 如需有關舊版視覺效果C++資料存取技術，請參閱[資料存取](http://msdn.microsoft.com/library/a9455752-39c4-4457-b14e-197772d3df0b)

### <a name="javascript"></a>JavaScript
 [Visual Studio 中的 JavaScript](https://msdn.microsoft.com/library/hh334522.aspx)是第一級語言建置跨平台應用程式、 UWP 應用程式、 雲端服務、 網站及 web 應用程式。 您可以使用 Bower、 Grunt、 Gulp、 npm 及 Visual Studio 中的從 NuGet 安裝您最愛的 JavaScript 程式庫和資料庫產品。 下載 Sdk 從連線到 Azure 儲存體和服務[Azure 網站](https://azure.microsoft.com/)。  Edge.js 是連接至 ADO.NET 資料來源的伺服器端 JavaScript (Node.js) 程式庫。

### <a name="python"></a>Python
 安裝[Python Tools for Visual Studio](http://microsoft.github.io/PTVS/)以及您最愛的 Python 架構建立 CPython 或 IronPython (.NET) 的應用程式。  Python Tools for Visual Studio 網站已在連接到資料，包括數個教學課程[Django 和在 Azure 上的 SQL Database](https://github.com/Microsoft/PTVS/wiki/Django-and-SQL-Database-on-Azure)， [Django 和在 Azure 上的 MySQL](https://github.com/Microsoft/PTVS/wiki/Django-and-MySQL-on-Azure)和[Bottle 和 MongoDB 上Azure](https://github.com/Microsoft/PTVS/wiki/Bottle-and-MongoDB-on-Azure)。

## <a name="in-this-section"></a>本節內容
 [安裝資料庫系統、 工具和範例](../data-tools/installing-database-systems-tools-and-samples.md)討論濆爧髍孮資料庫產品和 Visual Studio 擴充功能或驅動程式支援，以及何處尋找範例資料庫的實驗和學習之用。

 [適用於.NET 的 visual Studio 資料工具](http://msdn.microsoft.com/6b145922-2f00-47db-befc-bf351b4809a1)描述如何使用 Visual Studio 工具視窗來連接到資料來源、 建立資料集或 Entity Framework 模型，以及將資料繫結至使用者介面控制項。

## <a name="related-topics"></a>相關主題
 [資料、 裝置和分析](https://msdn.microsoft.com/data-and-devices)介紹 Microsoft 的智慧型雲端，包括 Cortana Analytics Suite 和物聯網的支援。

 [Microsoft Azure 儲存體](/azure/storage/)描述的 Azure 儲存體，以及如何使用 Azure blob、 資料表、 佇列和檔案建立應用程式。

 [Azure SQL Database](https://azure.microsoft.com/documentation/services/sql-database/)描述如何連接到 Azure SQL Database，關聯式資料庫即服務。

 [SQL Server Data Tools](https://msdn.microsoft.com/library/hh272686\(v=vs.103\).aspx)說明的工具，可簡化設計中，瀏覽、 測試及部署的資料連接的應用程式和資料庫。

 [ADO.NET](http://msdn.microsoft.com/library/5b96ed06-9759-4966-a797-a1d5f6ee50ca)描述 ADO.NET 架構以及如何使用 ADO.NET 類別來管理應用程式資料並與其互動的資料來源和 XML。

 [ADO.NET Entity Framework](https://msdn.microsoft.com/data/ef)說明如何建立資料應用程式可讓開發人員針對概念模型而不是直接針對關聯式資料庫設計程式。

 [WCF Data Services 4.5](http://msdn.microsoft.com/library/73d2bec3-7c92-4110-b905-11bb0462357a)描述如何使用[!INCLUDE[ssAstoria](../includes/ssastoria-md.md)]部署在 web 或內部網路上的資料服務可實作[開放式資料通訊協定 (OData)](http://go.microsoft.com/fwlink/?LinkID=182204)。

 [在 Office 方案中的資料](http://msdn.microsoft.com/library/8478c095-864b-4ed3-8a70-1fc19b411c6a)包含說明資料在 Office 方案中的運作方式的主題連結。 這包括有關結構描述導向程式設計、 資料快取，以及伺服器端資料存取的資訊。

 [LINQ (Language-Integrated Query)](http://msdn.microsoft.com/library/a73c4aec-5d15-4e98-b962-1274021ea93d)告訴您，內建的查詢功能C#和 Visual Basic 和查詢關聯式資料庫、 XML 文件、 資料集和記憶體中集合的一般模型。

 [Visual Studio 中的 XML 工具](../xml-tools/xml-tools-in-visual-studio.md)討論使用 XML 資料、 偵錯 XSLT，.NET Framework 的 XML 功能，以及 XML 查詢的架構。

 [XML 文件和資料](http://msdn.microsoft.com/library/e695047f-3c0f-4045-8708-5baea91cc380)提供一組完整且整合式的類別處理 XML 文件和.NET Framework 中的資料的概觀。
