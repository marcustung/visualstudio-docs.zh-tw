---
title: 多層式架構資料應用程式概觀
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- presentation tier
- middle tier
- data tier
- n-tier applications, about n-tier applications
ms.assetid: 1020581d-eaaa-41a2-aca4-bf4c212895f6
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 35b882914deacafae46f2470c49efe1d6ace00f6
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60109929"
---
# <a name="n-tier-data-applications-overview"></a>多層式架構 (N-Tier) 資料應用程式概觀
*多層式架構*資料應用程式是指分隔成多個資料應用程式*層*。 也稱為 「 分散式應用程式 」 和 「 多層式應用程式，多層式架構應用程式在個別分成離散層級的用戶端與伺服器之間分散處理。 當您開發應用程式以存取資料時，您應該有清楚的區隔，組成應用程式各層之間。

一般的 N-Tier 應用程式包含展示層、中介層和資料層。 分隔各層的多層式架構應用程式中的最簡單方式是建立針對您想要包含在您的應用程式中每一層的離散專案。 比方說，展示層可能是 Windows Forms 應用程式，而資料存取邏輯可能位於中介層的類別庫。 此外，展示層可能會與中介層服務，例如服務透過資料存取邏輯進行通訊。 將應用程式元件分隔成不同的層級會提升應用程式的可維護性和延展性 (Scalability)。 它會更輕鬆地採用新技術，可以套用至單一的層級，而不需要重新設計整個方案。 此外，多層式架構應用程式通常會儲存機密資訊在中介層，以維護從展示層的隔離。

Visual Studio 包含數個功能，可協助開發人員建立多層式架構應用程式：

- 資料集提供**資料集 Project**屬性，可讓您區隔資料集 （資料實體層） 和 Tableadapter （資料存取層） 分成離散專案。

- [在 Visual Studio 中的 LINQ to SQL 工具](../data-tools/linq-to-sql-tools-in-visual-studio2.md)提供用來產生不同的命名空間的 DataContext 和資料類別設定。 這可讓資料存取與資料實體層的邏輯分隔。

- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)提供<xref:System.Data.Linq.Table%601.Attach%2A>方法可讓您將應用程式中的不同層級的結合在一起的 DataContext。 如需詳細資訊，請參閱 <<c0> [ 多層式架構和遠端的應用程式使用 LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql)。

## <a name="presentation-tier"></a>展示層
*展示層*是使用者與應用程式的互動的層。 它通常會包含其他的應用程式邏輯也。 典型的展示層元件包括下列各項：

- 資料繫結的元件，例如<xref:System.Windows.Forms.BindingSource>和<xref:System.Windows.Forms.BindingNavigator>。

- 物件表示的資料，例如[LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)展示層中使用的實體類別。

展示層通常存取中介層使用的服務參考 (例如[Windows Communication Foundation 服務和 Visual Studio 中的 WCF Data Services](../data-tools/windows-communication-foundation-services-and-wcf-data-services-in-visual-studio.md)應用程式)。 展示層不會直接存取資料層。 展示層會與資料層透過中介層的資料存取元件通訊。

## <a name="middle-tier"></a>中介層
*中介層*用來彼此通訊的展示層和資料層的層。 典型的中介層元件包括下列各項：

- 商務邏輯，例如商務規則和資料驗證。

- 資料存取元件和邏輯，如下所示：

    - [TableAdapters](create-and-configure-tableadapters.md)並[Dataadapter 和 Datareader](/dotnet/framework/data/adonet/dataadapters-and-datareaders)。

    - 物件表示的資料，例如[LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)實體類別。

    - 一般應用程式服務，例如驗證、 授權和個人化。

下圖顯示功能和技術，可在 Visual Studio 中，和他們可能適用於什麼情況的多層式架構應用程式的中介層。

![中間層元件](../data-tools/media/ntiermid.png)中介層

中介層通常會連接到資料層使用的資料連接。 此資料連接通常會儲存在資料存取元件中。

## <a name="data-tier"></a>資料層
*資料層*基本上是儲存應用程式的資料 （例如，執行 SQL Server 的伺服器） 的伺服器。

下圖顯示功能和技術，可在 Visual Studio 中，和他們可能適用於什麼情況的多層式架構應用程式資料層。

![資料層元件](../data-tools/media/ntierdatatier.png)資料層

無法存取資料層，直接從展示層中的用戶端。 相反地中介層, 的資料存取元件用於展示層和資料層之間的通訊。

## <a name="help-for-n-tier-development"></a>適用於多層式架構開發的說明
下列主題提供有關使用多層式架構應用程式的資訊：

[將資料集和 TableAdapter 分成不同的專案](../data-tools/separate-datasets-and-tableadapters-into-different-projects.md)

[逐步解說：建立多層式架構 (N-Tier) 資料應用程式](../data-tools/walkthrough-creating-an-n-tier-data-application.md)

[使用 LINQ to SQL 的多層式架構 (N-Tier) 和遠端應用程式](/dotnet/framework/data/adonet/sql/linq/n-tier-and-remote-applications-with-linq-to-sql)

## <a name="see-also"></a>另請參閱

- [逐步解說：建立多層式架構 (N-Tier) 資料應用程式](../data-tools/walkthrough-creating-an-n-tier-data-application.md)
- [階層式更新](../data-tools/hierarchical-update.md)
- [Visual Studio 中的資料集工具](../data-tools/dataset-tools-in-visual-studio.md)
- [存取 Visual Studio 中的資料](../data-tools/accessing-data-in-visual-studio.md)