---
title: 要編碼的 URI 包含無效的字元 |Microsoft Docs
ms.date: 01/18/2017
ms.prod: visual-studio-windows
ms.technology: vs-javascript
ms.topic: reference
f1_keywords:
- VS.WebClient.Help.SCRIPT5024
dev_langs:
- JavaScript
- TypeScript
- DHTML
ms.assetid: a3f0fdbb-8d4b-41ae-a396-43dfc9483760
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f2f9111acf656bf882a3d506fe95b8361f3693ff
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053390"
---
# <a name="the-uri-to-be-encoded-contains-an-invalid-character"></a>要編碼的 URI 包含無效的字元
您嘗試將字串編碼為 URI （統一資源識別項），但它包含無效的字元。 雖然大部分字元字串轉換成 Uri 內有效，但是某些 Unicode 字元序列是不合法的。  
  
### <a name="to-correct-this-error"></a>更正這個錯誤  
  
- 確定要編碼的字串，包含只有有效的 Unicode 順序。 完整的 URI 被組成一連串的元件和分隔符號。 角括弧括住的名稱代表的元件，而":"，"/"，";"和"？"是用來做為分隔符號的保留的字元。 一般格式如下：  
  
    ```JavaScript  
    <Scheme>:<first>/<second>;<third>?<fourth>  
    ```  
  
## <a name="see-also"></a>另請參閱  
 [encodeURI 函式](../../javascript/reference/encodeuri-function-javascript.md)   
 [encodeURIComponent 函式](../../javascript/reference/encodeuricomponent-function-javascript.md)