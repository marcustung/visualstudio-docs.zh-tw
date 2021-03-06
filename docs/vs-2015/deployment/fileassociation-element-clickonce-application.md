---
title: '&lt;fileAssociation&gt;項目 （ClickOnce 應用程式） |Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-deployment
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <fileAssociation> element [ClickOnce application manifest]
- manifests [ClickOnce], fileAssociation element
ms.assetid: 8f951b4f-54f9-412e-a9e5-af4e379fcf08
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4b31ac34627b244cb61b6fdb5c6ca214675ec045
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58941792"
---
# <a name="ltfileassociationgt-element-clickonce-application"></a>&lt;fileAssociation&gt;項目 （ClickOnce 應用程式）
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

識別要與應用程式相關聯的副檔名。  
  
## <a name="syntax"></a>語法  
  
```  
<fileAssociation  
    xmlns="urn:schemas-microsoft-com:clickonce.v1"  
    extension  
    description  
    progid  
    defaultIcon  
/>  
```  
  
## <a name="elements-and-attributes"></a>項目和屬性  
 `fileAssociation` 項目是選擇性的。 此元素具有下列屬性。  
  
|屬性|描述|  
|---------------|-----------------|  
|`extension`|必要項。 要與應用程式相關聯的副檔名。|  
|`description`|必要項。 Shell 所使用的檔案類型的描述。|  
|`progid`|必要項。 可唯一識別檔案類型的名稱。|  
|`defaultIcon`|必要項。 指定要用於與此延伸模組檔案的圖示。 必須使用指定的圖示檔[\<檔案 > 項目](../deployment/file-element-clickonce-application.md)內[\<組件 > 項目](../deployment/assembly-element-clickonce-application.md)，包含這個項目。|  
  
## <a name="remarks"></a>備註  
 此元素必須包含的 XML 命名空間參考"urn: schemas-microsoft-microsoft-com:clickonce.v1"。 如果`<fileAssociation>`項目時，它必須緊跟在後`<application>`項目在其父代[\<組件 > 項目](../deployment/assembly-element-clickonce-application.md)。  
  
 [!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)] 不會覆寫現有的檔案關聯。 不過，ClickOnce 應用程式可以覆寫目前使用者的檔案副檔名。 ClickOnce 應用程式解除安裝後，ClickOnce 會刪除使用者的檔案關聯和每台電腦關聯為使用一次。  
  
## <a name="example"></a>範例  
 下列程式碼範例說明`fileAssociation`的文字編輯器的應用程式，使用部署資訊清單的應用程式中的項目[!INCLUDE[ndptecclick](../includes/ndptecclick-md.md)]。 此程式碼範例也包含[\<檔案 > 項目](../deployment/file-element-clickonce-application.md)所`defaultIcon`屬性。  
  
```  
<file name="text.ico" size="4286">  
  <hash>  
    <dsig:Transforms>  
      <dsig:Transform Algorithm="urn:schemas-microsoft-com:HashTransforms.Identity" />  
    </dsig:Transforms>  
    <dsig:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
    <dsig:DigestValue>0joAqhmfeBb93ZneZv/oTMP2brY=</dsig:DigestValue>  
  </hash>  
</file>  
<file name="writing.ico" size="9662">  
  <hash>  
    <dsig:Transforms>  
      <dsig:Transform Algorithm="urn:schemas-microsoft-com:HashTransforms.Identity" />  
    </dsig:Transforms>  
    <dsig:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1" />  
    <dsig:DigestValue>2cL2U7cm13nG40v9MQdxYKazIwI=</dsig:DigestValue>  
  </hash>  
</file>  
<fileAssociation xmlns="urn:schemas-microsoft-com:clickonce.v1" extension=".text" description="Text  Document (ClickOnce)" progid="Text.Document" defaultIcon="text.ico" />  
<fileAssociation xmlns="urn:schemas-microsoft-com:clickonce.v1" extension=".writing" description="Writings (ClickOnce)" progid="Writing.Document" defaultIcon="writing.ico" />  
```  
  
## <a name="see-also"></a>另請參閱  
 [ndptecclick](../deployment/clickonce-application-manifest.md)
