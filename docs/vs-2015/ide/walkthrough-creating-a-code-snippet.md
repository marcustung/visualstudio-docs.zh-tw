---
title: 逐步解說：建立程式碼片段 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- code snippets, creating
- code snippets, shortcut
- code snippets, template
- code snippets, replacements
- code snippets, references
- code snippets, imports
ms.assetid: 0dcaae11-39cf-4463-9c90-2494321251c2
caps.latest.revision: 25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ee4e0c6fd686398ae89b5c079d6efc1297a19f5d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60109800"
---
# <a name="walkthrough-creating-a-code-snippet"></a>逐步解說：建立程式碼片段
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

只需要幾個步驟就能建立程式碼片段。 您只需要建立 XML 檔案、填入適當的項目，並在其中新增您的程式碼。 您也可以將參考和取代參數新增至程式碼。 您可以使用 [程式碼片段管理員] ([工具]/[程式碼片段管理員]) 上的 [匯入] 按鈕，將程式碼片段新增至 Visual Studio 安裝。  
  
> [!TIP]
>  如需如何更輕鬆地撰寫程式碼片段，在 CodePlex 網站搜尋社群工具這類[程式碼片段編輯器](http://go.microsoft.com/fwlink/?LinkId=251033)。  
  
## <a name="snippet-template"></a>程式碼片段範本  
 以下是基本程式碼片段範本：  
  
```  
<?xml version="1.0" encoding="utf-8"?>  
<CodeSnippets  
    xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">  
    <CodeSnippet Format="1.0.0">  
        <Header>  
            <Title></Title>  
        </Header>  
        <Snippet>  
            <Code Language="">  
                <![CDATA[]]>  
            </Code>  
        </Snippet>  
    </CodeSnippet>  
</CodeSnippets>  
  
```  
  
### <a name="to-create-a-code-snippet"></a>建立程式碼片段  
  
1. 在 Visual Studio 中建立新的 XML 檔案，並新增上面所示的範本。  
  
2. 在 Title 項目中，填入程式碼片段標題，例如 "Hello World VB"。  
  
3. 在 [程式碼] 項目的 [語言] 屬性中，填入程式碼片段的語言。 在此範例中，使用 "VB"。  
  
4. 例如，在 Code 項目的 CDATA 區段中新增一些程式碼：  
  
    ```  
    <Code Language="VB">  
        <![CDATA[Console.WriteLine("Hello, World!")]]>  
    </Code>  
  
    ```  
  
5. 將程式碼片段儲存為 VBCodeSnippet.snippet。  
  
### <a name="to-add-a-code-snippet-to-visual-studio"></a>將程式碼片段新增至 Visual Studio  
  
1. 您可以使用 [程式碼片段管理員]，將自己的程式碼片段新增至 Visual Studio 安裝。 開啟 [程式碼片段管理員] ([工具]/[程式碼片段管理員])。  
  
2. 按一下 [匯出] 按鈕。  
  
3. 移至您在先前程序中儲存程式碼片段的位置，並選取它，然後按一下 [開啟]。  
  
4. [匯入程式碼片段] 對話方塊隨即開啟，要求您從右窗格的選項中選擇要新增程式碼片段的位置。 其中一個選項應該是 [我的程式碼片段]。 選取它，然後依序按一下 [完成] 和 [確定]。  
  
5. 程式碼片段會複製至下列位置：  
  
     `%USERPROFILE%\Documents\Visual Studio 2013\Code Snippets\Visual Basic\My Code Snippets`  
  
6. 開啟 Visual Basic 專案，並開啟程式碼檔，來測試程式碼片段。 在檔案中按一下**插入程式碼片段**操作功能表上，然後**My Code Snippets**。 您應該會看到名為 **My Visual Basic Code Snippet** 的程式碼片段。 對它按兩下。  
  
7. 您應該會看到`Console.WriteLine("Hello, World!")`插入程式碼中。  
  
### <a name="adding-description-and-shortcut-fields"></a>新增描述和捷徑欄位  
  
1. 描述欄位會提供您的程式碼片段在 [程式碼片段管理員] 中檢視時的詳細資訊。 捷徑是使用者可鍵入以插入程式碼片段的標記。 編輯您已開啟檔案的程式碼片段`%USERPROFILE%\Documents\Visual Studio 2013\Code Snippets\Visual Basic\My Code Snippet\VBCodeSnippet.snippet`。  
  
2. 將 Author 和 Description 項目新增至 Header 項目，並填入其資料。  
  
3. Header 項目看起來應該類似這樣：  
  
    ```  
    <Header>  
        <Title>Hello World VB</Title>  
        <Author>Myself</Author>  
        <Description>Says Hello to the world.</Description>  
    </Header>  
  
    ```  
  
4. 開啟 [程式碼片段管理員]，然後選取程式碼片段。 在右窗格中，您應該會看到現在已填入 [描述] 和 [作者] 欄位。  
  
5. 若要新增捷徑，請新增 Shortcut 項目以及 Author 和 Description 項目：  
  
    ```  
    <Header>  
        <Title>Hello World VB</Title>  
        <Author>Myself</Author>  
        <Description>Says Hello to the world.</Description>  
        <Shortcut>hello</Shortcut>  
    </Header>  
  
    ```  
  
6. 重新儲存程式碼片段檔案。  
  
7. 若要測試捷徑，請開啟 Visual Basic 專案，並開啟程式碼檔。 型別`hello`中的檔案及按下 TAB 鍵。 應該插入程式碼片段。  
  
### <a name="to-add-references-and-imports"></a>新增 References 和 Imports  
  
1. 使用 Visual Basic 程式碼片段，您可以使用 References 項目新增至專案的參考，並使用 Imports 項目新增 Imports 宣告。 （其他語言中的程式碼片段沒有這項功能。）例如，如果您將程式碼範例中的 `Console.WriteLine` 變更為 `MessageBox.Show`，則可能需要將 System.Windows.Forms.dll 組件新增至專案。  
  
2. 開啟程式碼片段。  
  
3. 在 Snippet 項目下新增 References 項目：  
  
    ```  
    <References>  
        <Reference>  
            <Assembly>System.Windows.Forms.dll</Assembly>  
        </Reference>  
    </References>  
  
    ```  
  
4. 在 Snippet 項目下新增 Imports 項目：  
  
    ```  
    <Imports>  
        <Import>  
           <Namespace>System.Windows.Forms</Namespace>  
        </Import>  
    </Imports>  
  
    ```  
  
5. 將 CDATA 區段變更如下：  
  
    ```  
    <![CDATA[MessageBox.Show("Hello, World!")]]>  
    ```  
  
6. 儲存程式碼片段。  
  
7. 開啟 Visual Basic 專案，並新增程式碼片段。  
  
8. 您會在程式碼檔頂端看到 Imports 陳述式：  
  
    ```  
    Imports System.Windows.Forms  
  
    ```  
  
9. 查看專案的屬性。 [參考] 索引標籤會包含 System.Windows.Forms.dll 的參考。  
  
### <a name="adding-replacements"></a>新增取代  
  
1. 您可能想要讓使用者取代程式碼片段的各部分；例如，如果您新增變數，而且想要使用者將變數取代為目前專案中的變數。 您可以提供兩種類型的取代：常值和物件。 常值是某種類型的字串 (字串常值、變數名稱或數值的字串表示法)。 物件是字串以外的某種類型的執行個體。 在此程序中，您會宣告常值取代和物件取代，並變更程式碼以參考這些取代。  
  
2. 開啟程式碼片段。  
  
3. 此範例使用 SQL 連接字串，因此您需要變更 Imports 和 References 項目來新增適當的參考：  
  
    ```  
    <References>  
        <Reference>  
            <Assembly>System.Data.dll</Assembly>  
        </Reference>  
        <Reference>  
            <Assembly>System.Xml.dll</Assembly>  
        </Reference>  
    </References>  
    <Imports>  
        <Import>  
            <Namespace>System.Data</Namespace>  
        </Import>  
        <Import>  
            <Namespace>System.Data.SqlClient</Namespace>  
        </Import>  
    </Imports>  
  
    ```  
  
4. 若要宣告 SQL 連接字串的常值取代，請在 Snippet 項目下新增 Declarations 項目，並在其中新增具有取代識別碼、工具提示和預設值之子項目的 Literal 項目：  
  
    ```  
    <Declarations>  
        <Literal>  
            <ID>SqlConnString</ID>  
            <ToolTip>Replace with a SQL connection string.</ToolTip>  
            <Default>"SQL connection string"</Default>  
        </Literal>  
    </Declarations>  
  
    ```  
  
5. 若要宣告 SQL 連線的物件取代，請新增 Declarations 項目內的 Object 項目，並新增識別碼、物件類型、工具提示和預設值的子項目。 產生的 Declarations 項目看起來應該像這樣：  
  
    ```  
    <Declarations>  
        <Literal>  
            <ID>SqlConnString</ID>  
            <ToolTip>Replace with a SQL connection string.</ToolTip>  
            <Default>"SQL connection string"</Default>  
        </Literal>  
        <Object>  
            <ID>SqlConnection</ID>  
            <Type>System.Data.SqlClient.SqlConnection</Type>  
            <ToolTip>Replace with a connection object in your application.</ToolTip>  
            <Default>dcConnection</Default>  
        </Object>  
    </Declarations>  
    ```  
  
6. 在程式碼區段中，您可以參考使用 $ 符號括住的取代 (例如 `$replacement$`)：  
  
    ```  
    <Code Language="VB" Kind="method body">  
        <![CDATA[Dim daCustomers As SqlDataAdapter  
            Dim selectCommand As SqlCommand  
  
            daCustomers = New SqlClient.SqlDataAdapter()  
            selectCommand = new SqlClient.SqlCommand($SqlConnString$)  
            daCustomers.SelectCommand = selectCommand  
            daCustomers.SelectCommand.Connection = $SqlConnection$]]>  
    </Code>  
    ```  
  
7. 儲存程式碼片段。  
  
8. 開啟 Visual Basic 專案，並新增程式碼片段。  
  
9. 程式碼應該如下，其中會以淺橙色反白顯示 `SQL connection string` 和 `dcConnection` 取代。 按下索引標籤，以從兩個不同的瀏覽。  
  
    ```  
    Dim daCustomers As SqlDataAdapter  
    Dim selectCommand As SqlCommand  
  
    daCustomers = New SqlClient.SqlDataAdapter()  
    selectCommand = New SqlClient.SqlCommand("SQL connection string")  
    daCustomers.SelectCommand = selectCommand  
    daCustomers.SelectCommand.Connection = dcConnection  
  
    ```  
  
## <a name="see-also"></a>另請參閱  
 [程式碼片段結構描述參考](../ide/code-snippets-schema-reference.md)
