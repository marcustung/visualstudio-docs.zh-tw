---
title: 與 XML 編輯器整合 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 43d7a8e6-bd94-4407-a800-15a145c74223
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 350b97385ab03daca80cc86d4f672dfec07222aa
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/17/2019
ms.locfileid: "59654018"
---
# <a name="integration-with-xml-editor"></a>與 XML 編輯器整合
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XML 結構描述設計工具會與 XML 編輯器整合。 如果您修改 XSD 檔案在 XML 編輯器 中，變更將會反映在[XML 結構描述總管](../xml-tools/xml-schema-explorer.md)。 如果您有[圖表檢視](../xml-tools/graph-view.md)或[內容模型檢視](../xml-tools/content-model-view.md)開啟時，變更也會反映那里。 您可以利用下列方式，在 XML 結構描述設計工具和 XML 編輯器之間巡覽：  
  
- 在 XML 編輯器中，以滑鼠右鍵按一下節點，然後選取**在 XML 結構描述總管中顯示**。  
  
- 在 [圖表] 檢視和 XML 結構描述總管中，按兩下 [] 節點，或以滑鼠右鍵按一下節點並選取**檢視程式碼**。 在內容模型檢視中，以滑鼠右鍵按一下節點，然後選取**檢視程式碼**。  
  
  下列螢幕擷取畫面會顯示在 XML 結構描述總管中開啟的 XML 結構描述。 XML 結構描述總管會在樹狀檢閱中顯示結構描述設定。 XML 編輯器會顯示目前在 XML 結構描述總管中使用之節點的文字檢視。  
  
  ![XSDDesignerWithXMLEditor](../xml-tools/media/xsddesignerwithxmleditor.gif "XSDDesignerWithXMLEditor")  
  
  有時候，在並排顯示的 XML 編輯器和圖形設計工具中查看程式碼相當有用。 若要檢視這兩個檔案，在相同的時間，以滑鼠右鍵按一下 XML 編輯器中，然後選取**檢視表設計工具**。 在 Visual Studio Windows 功能表中，選取**新增水平 （或垂直） 索引標籤群組**。  
  
  ![XSDDesignerWithXMLEditorAndCMV](../xml-tools/media/xsddesignerwithxmleditorandcmv.gif "XSDDesignerWithXMLEditorAndCMV")  
  
## <a name="see-also"></a>另請參閱  
 [XML 結構描述總管](../xml-tools/xml-schema-explorer.md)
