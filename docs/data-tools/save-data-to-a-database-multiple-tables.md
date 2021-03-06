---
title: 將資料儲存至資料庫 (多個資料表)
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- updating datasets, walkthroughs
- data [Visual Studio], saving
- saving data, walkthroughs
- data [Visual Studio], updating
ms.assetid: 7ebe03da-ce8c-4cbc-bac0-a2fde4ae4d07
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 9e4a30c3aa85969a4cbf712f2f4018c24169ff6d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60051410"
---
# <a name="save-data-to-a-database-multiple-tables"></a>將資料儲存至資料庫 (多個資料表)

在應用程式的開發過程中，最常見的一個情節是在 Windows 應用程式的表單上顯示資料並編輯資料，以及將更新的資料傳送回資料庫。 此逐步解說會建立表單，以顯示來自兩個關聯資料表的資料，並示範如何編輯記錄，以及將變更儲存回資料庫。 此範例使用 Northwind 範例資料庫的 `Customers` 和 `Orders` 資料表。

您可以透過呼叫 TableAdapter 的 `Update` 方法，將應用程式的資料存回資料庫。 當您將資料表從**Zdroje dat**視窗拖曳到表單時，必須先儲存資料的程式碼會自動加入。 加入至表單的任何其他資料表都需要手動加入此程式碼。 此逐步解說會示範如何加入程式碼，以儲存多個資料表的更新。

這個逐步解說中所述的工作包括：

- 建立及設定您的應用程式中的資料來源[資料來源組態精靈](../data-tools/media/data-source-configuration-wizard.png)。

- 設定控制項中項目的[資料來源 視窗](add-new-data-sources.md#data-sources-window)。 如需詳細資訊，請參閱 <<c0> [ 設定要從資料來源視窗拖曳時要建立的控制項](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md)。

- 從 [資料來源] 視窗將項目拖曳至表單，以建立資料繫結控制項。

- 修改資料集中的每個資料表中的一些記錄。

- 修改程式碼，以將資料集中更新的資料傳送回資料庫。

## <a name="prerequisites"></a>必要條件

本逐步解說會使用 SQL Server Express LocalDB 和 Northwind 範例資料庫。

1. 如果您沒有 SQL Server Express LocalDB，請將它安裝從[SQL Server Express 下載頁面](https://www.microsoft.com/sql-server/sql-server-editions-express)，或透過**Visual Studio 安裝程式**。 在  **Visual Studio 安裝程式**，您可以安裝 SQL Server Express LocalDB 做為一部分**資料儲存和處理**工作負載，或作為個別的元件。

2. 安裝 Northwind 範例資料庫執行下列步驟：

    1. 在 Visual Studio 中開啟**SQL Server 物件總管**視窗。 (SQL Server 物件總管 中已安裝的一部分**資料儲存和處理**Visual Studio 安裝程式中的工作負載。)依序展開**SQL Server**節點。 以滑鼠右鍵按一下您的 LocalDB 執行個體，然後選取**新的查詢**。

       查詢編輯器視窗隨即開啟。

    2. 複製[Northwind 的 TRANSACT-SQL 指令碼](https://github.com/MicrosoftDocs/visualstudio-docs/blob/master/docs/data-tools/samples/northwind.sql?raw=true)到剪貼簿。 這個 T-SQL 指令碼會從頭建立 Northwind 資料庫，並填入資料。

    3. 將 T-SQL 指令碼貼到查詢編輯器，然後選擇**Execute**  按鈕。

       短時間之後，查詢完成執行，並建立 Northwind 資料庫。

## <a name="create-the-windows-forms-application"></a>建立 Windows Forms 應用程式

建立新**Windows Forms 應用程式**專案，或C#或 Visual Basic。 將專案命名為 **UpdateMultipleTablesWalkthrough**。

## <a name="create-the-data-source"></a>建立資料來源

此步驟會使用 [資料來源組態精靈] 從 Northwind 資料庫建立資料來源。 您必須具有 Northwind 範例資料庫的存取權，才能建立連接。 如需設定 Northwind 範例資料庫的詳細資訊，請參閱[How to:安裝範例資料庫](../data-tools/installing-database-systems-tools-and-samples.md)。

1. 在 **資料**功能表上，選取**顯示資料來源**。

   [資料來源] 視窗隨即開啟。

2. 在 [資料來源] 視窗中，選取 [新增新資料來源]，以啟動 [資料來源組態精靈]。

3. 在 [**選擇資料來源類型**畫面上，選取**資料庫**，然後選取**下一步]**。

4. 在 **選擇您的資料連接**畫面上，執行下列其中一項：

    - 如果下拉式清單中有提供 Northwind 範例資料庫的資料連接，請選取這個資料連接。

         -或-

    - 選取 [新增連線]，以開啟 [新增/修改連線] 對話方塊。

5. 如果您的資料庫需要密碼，請選取選項來加入敏感性資料，然後選取**下一步**。

6. 在 [**將連接字串儲存到應用程式組態檔**，選取**下一步]**。

7. 在 **選擇您的資料庫物件**畫面上，展開**資料表**節點。

8. 選取 **客戶**並**訂單**資料表，然後選取**完成**。

     **NorthwindDataSet** 會新增專案中，且資料表會出現在 [資料來源] 視窗中。

## <a name="set-the-controls-to-be-created"></a>設定要建立的控制項

在這個逐步解說中的資料`Customers`資料表存在於**詳細資料**其中資料會顯示在個別控制項的版面配置。 將資料從`Orders`資料表存在於**格線**版面配置中顯示<xref:System.Windows.Forms.DataGridView>控制項。

### <a name="to-set-the-drop-type-for-the-items-in-the-data-sources-window"></a>在資料來源視窗中設定項目的卸除類型

1. 在 [**資料來源**] 視窗中，展開**客戶**節點。

2. 在上**客戶**節點中，選取**詳細資料**若要變更的控制項的控制項清單**客戶**為個別控制項的資料表。 如需詳細資訊，請參閱 <<c0> [ 設定要從資料來源視窗拖曳時要建立的控制項](../data-tools/set-the-control-to-be-created-when-dragging-from-the-data-sources-window.md)。

## <a name="create-the-data-bound-form"></a>建立資料繫結表單

您可以從 [資料來源] 視窗將項目拖曳至表單，以建立資料繫結控制項。

1. 從 [資料來源] 視窗，將 [客戶] 主節點拖曳至 **Form1**。

     會在表單上顯示具有描述性的資料繫結控制項，以及巡覽記錄的工具區域 (<xref:System.Windows.Forms.BindingNavigator>)。 A [NorthwindDataSet](../data-tools/dataset-tools-in-visual-studio.md)， `CustomersTableAdapter`， <xref:System.Windows.Forms.BindingSource>，和<xref:System.Windows.Forms.BindingNavigator>會出現在元件匣。

2. 從 [資料來源] 視窗將關聯的 [Orders] 節點拖曳至 [Form1]。

    > [!NOTE]
    > 關聯的 [Orders] 節點位於 [Fax] 節點之下，而且是 [Customers] 節點的子節點。

     <xref:System.Windows.Forms.DataGridView> 控制項以及巡覽記錄的工具區域 (<xref:System.Windows.Forms.BindingNavigator>) 會出現在表單上。 `OrdersTableAdapter`和<xref:System.Windows.Forms.BindingSource>會出現在元件匣。

## <a name="add-code-to-update-the-database"></a>加入程式碼以更新資料庫

您可以藉由呼叫 [Customers] 和 [Orders] TableAdapters 的 `Update` 方法以更新資料庫。 根據預設，事件處理常式**儲存**按鈕<xref:System.Windows.Forms.BindingNavigator>新增至表單的程式碼，以將更新傳送至資料庫。 此程序修改程式碼，以將更新傳送正確的順序。這會排除參考完整性錯誤提高的可能性。 程式碼也會藉由將 try-catch 區塊中的更新呼叫換行，以實作錯誤處理。 您可以修改程式碼，使其符合應用程式的需求。

> [!NOTE]
> 為了清楚起見，本逐步解說中所使用的交易。 不過，如果您正在更新兩個或多個相關資料表，包含在交易內的所有更新邏輯。 交易是確保對資料庫的所有相關的變更都成功，認可任何變更之前的程序。 如需詳細資訊，請參閱 <<c0> [ 異動和並行存取](/dotnet/framework/data/adonet/transactions-and-concurrency)。

### <a name="to-add-update-logic-to-the-application"></a>將更新邏輯加入至應用程式

1. 選取 **儲存**按鈕<xref:System.Windows.Forms.BindingNavigator>。 這會開啟程式碼編輯器`bindingNavigatorSaveItem_Click`事件處理常式。

2. 替換事件處理常式中的程式碼，以呼叫相關 TableAdapters 的 `Update` 方法。 下列程式碼會先建立三個暫存資料表，以保留 <xref:System.Data.DataRowState> (<xref:System.Data.DataRowState.Deleted>、<xref:System.Data.DataRowState.Added> 及 <xref:System.Data.DataRowState.Modified>) 的更新資訊。 更新會以正確的順序執行。 程式碼看起來應該如下所示：

     [!code-vb[VbRaddataSaving#10](../data-tools/codesnippet/VisualBasic/save-data-to-a-database-multiple-tables_1.vb)]
     [!code-csharp[VbRaddataSaving#10](../data-tools/codesnippet/CSharp/save-data-to-a-database-multiple-tables_1.cs)]

## <a name="test-the-application"></a>測試應用程式

1. 請按 **F5**。

2. 在每個資料表中，變更一個或多個記錄的資料。

3. 選取 [儲存] 按鈕。

4. 檢查資料庫中的值，確認已儲存變更。

## <a name="see-also"></a>另請參閱

- [將資料儲存回資料庫](../data-tools/save-data-back-to-the-database.md)