---
title: 將資料集儲存為 XML |Microsoft Docs
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
- XML [Visual Basic], datasets
- data [Visual Studio], saving as XML
- datasets [Visual Basic], saving as XML
- saving data
ms.assetid: 68b8327c-ae05-49ff-b9ba-99183e70b52c
caps.latest.revision: 14
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 2e4331b59c532e681c7e10ab8e43b953e9f72b18
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60059691"
---
# <a name="save-a-dataset-as-xml"></a>將資料集儲存為 XML
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

資料集內的 XML 資料可以存取的資料集上呼叫可用的 XML 方法。 若要以 XML 格式儲存資料，您可以呼叫<xref:System.Data.DataSet.GetXml%2A>方法或<xref:System.Data.DataSet.WriteXml%2A>方法<xref:System.Data.DataSet>。  
  
 呼叫<xref:System.Data.DataSet.GetXml%2A>方法會傳回字串，包含所有資料表的資料會格式化為 XML 資料集裡的資料。  
  
 呼叫<xref:System.Data.DataSet.WriteXml%2A>方法會以 XML 格式的資料傳送至您指定的檔案。  
  
### <a name="to-save-the-data-in-a-dataset-as-xml-to-a-variable"></a>若要將資料集中的資料為 XML 儲存至變數  
  
- <xref:System.Data.DataSet.GetXml%2A>方法會傳回<xref:System.String>。這表示您宣告類型的變數<xref:System.String>並將其指派的結果<xref:System.Data.DataSet.GetXml%2A>方法。  
  
     [!code-csharp[VbRaddataSaving#12](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#12)]
     [!code-vb[VbRaddataSaving#12](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#12)]  
  
### <a name="to-save-the-data-in-a-dataset-as-xml-to-a-file"></a>若要將資料集中的資料為 XML 儲存至檔案  
  
- <xref:System.Data.DataSet.WriteXml%2A>方法有數個多載。 下列程式碼示範如何將資料儲存至檔案。宣告變數，並將它指派有效的路徑來儲存檔案。  
  
     [!code-csharp[VbRaddataSaving#13](../snippets/csharp/VS_Snippets_VBCSharp/VbRaddataSaving/CS/Class1.cs#13)]
     [!code-vb[VbRaddataSaving#13](../snippets/visualbasic/VS_Snippets_VBCSharp/VbRaddataSaving/VB/Class1.vb#13)]  
  
## <a name="see-also"></a>另請參閱  
 [將資料儲存回資料庫](../data-tools/save-data-back-to-the-database.md)
