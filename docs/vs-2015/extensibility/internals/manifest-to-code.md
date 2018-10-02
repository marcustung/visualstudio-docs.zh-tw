---
title: 程式碼資訊清單 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 17ecacea-397d-4a97-b003-01bd5d56e936
caps.latest.revision: 5
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: f0809d44afb6777f26ea6b863ede765d93b5d24f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/22/2018
ms.locfileid: "47485512"
---
# <a name="manifest-to-code"></a>資訊清單至程式碼
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

本主題的最新的版本可從[程式碼資訊清單](https://docs.microsoft.com/visualstudio/extensibility/internals/manifest-to-code)。  
  
資訊清單以程式碼工具是 Visual Studio 映像服務採用.imagemanifest 檔案，並產生包裝函式的檔案或檔案參考 c + +、 C#、 VB 或 Visual Studio 擴充功能的.vsct 檔案中的映像資訊清單的值的主控台應用程式。 此工具會產生可用於從 Visual Studio 映像服務直接提出要求的映像或傳遞到 Api 的資訊清單的值，如果程式碼不會處理任何自己的 UI 和轉譯的包裝函式檔案。  
  
## <a name="how-to-use-the-tool"></a>如何使用工具  
 **語法**  
  
 ManifestToCode /manifest:\<映像資訊清單檔案 > /language:\<程式碼語言 >\<選擇性引數 >  
  
 **引數**  
  
||||  
|-|-|-|  
|**交換器名稱**|**備註**|**必要或選用**|  
|/manifest|若要建立或更新的程式碼包裝函式使用映像資訊清單的路徑。|必要|  
|/language|要在其中產生的程式碼包裝函式語言。<br /><br /> 有效值： CPP、 c + +、 CS、 CSharp、 C#、 VB 或 VSCT 值不區分大小寫。<br /><br /> VSCT 語言則會忽略選項、 /monikerClass、 /classAccess 和 /namespace 選項。|必要|  
|/imageIdClass|ImageIdClass 和相關聯的工具所建立的檔案名稱。 C + + 語言選項時，會產生只有.h 檔案。<br /><br /> 預設值：\<資訊清單路徑 > \MyImageIds。\<L a n g e >|Optional|  
|/monikerClass|MonikerClass 和相關聯的工具所建立的檔案名稱。 C + + 語言選項時，會產生只有.h 檔案。 這會忽略 VSCT 語言。<br /><br /> 預設值：\<資訊清單路徑 > \MyMonikers。\<L a n g e >|Optional|  
|/classAccess|ImageIdClass 和 monikerClass 存取修飾詞。 請確定所指定語言的存取修飾詞無效。 這會忽略 VSCT 語言選項。<br /><br /> 預設： 公用|Optional|  
|/namespace|在程式碼包裝函式中定義的命名空間。 這會忽略 VSCT 語言選項。 可能是 '。 ' 或 ':: ' 是有效的命名空間的分隔符號，不論所選擇的語言選項。<br /><br /> 預設： Images|Optional|  
|/noLogo|設定這個旗標，就會停止列印的產品和著作權資訊。|Optional|  
|/?|列印出說明資訊。|Optional|  
|/help|列印出說明資訊。|Optional|  
  
 **範例**  
  
-   ManifestToCode /manifest:D:\MyManifest.imagemanifest /language: csharp  
  
-   ManifestToCode /manifest:D:\MyManifest.imagemanifest /language:C++ /namespace： 我:: 命名空間 /imageIdClass:MyImageIds /monikerClass:MyMonikers /classAccess:friend  
  
-   ManifestToCode /manifest:D:\MyManifest.imagemanifest /language:VSCT /imageIdClass:MyImageIds  
  
## <a name="notes"></a>注意  
  
-   我們建議您使用這項工具與資源 工具的資訊清單所產生的映像資訊清單。  
  
-   此工具只會查看符號項目，以產生程式碼包裝函式。 如果映像資訊清單包含沒有符號，產生的程式碼包裝函式會是空的。 如果沒有映像或映像資訊清單中不會使用符號的映像，他們將會排除從程式碼包裝函式。  
  
## <a name="sample-output"></a>範例輸出  
 **C# 包裝函式**  
  
 一對簡單的映像識別碼和影像 moniker 類別的 C# 會類似下列程式碼：  
  
```csharp  
//-----------------------------------------------------------------------------  
// <auto-generated>  
//     This code was generated by the ManifestToCode tool.  
//     Tool Version: 14.0.15198  
// </auto-generated>  
//-----------------------------------------------------------------------------  
  
using System;  
  
namespace MyImages  
{  
    public static class MyImageIds  
    {  
        public static readonly Guid AssetsGuid = new Guid("{442d8739-efde-46a4-8f29-e3a1e5e7f8b4}");  
  
        public const int MyImage1 = 0;  
        public const int MyImage2 = 1;  
    }  
}  
//-----------------------------------------------------------------------------  
// <auto-generated>  
//     This code was generated by the ManifestToCode tool.  
//     Tool Version: 14.0.15198  
// </auto-generated>  
//-----------------------------------------------------------------------------  
  
using Microsoft.VisualStudio.Imaging.Interop;  
  
namespace MyImages  
{  
    public static class MyMonikers  
    {  
        public static ImageMoniker MyImage1 { get { return new ImageMoniker { Guid = MyImageIds.AssetsGuid, Id = MyImageIds.MyImage1 }; } }  
        public static ImageMoniker MyImage2 { get { return new ImageMoniker { Guid = MyImageIds.AssetsGuid, Id = MyImageIds.MyImage2 }; } }  
    }  
}  
```  
  
 **C + + 包裝函式**  
  
 一對簡單的映像識別碼和影像 moniker 類別的 c + + 會類似下列程式碼：  
  
```cpp  
//-----------------------------------------------------------------------------  
// <auto-generated>  
//     This code was generated by the ManifestToCode tool.  
//     Tool Version: 14.0.15198  
// </auto-generated>  
//-----------------------------------------------------------------------------  
  
#pragma once  
  
#include <guiddef.h>  
  
namespace MyImages {  
  
class MyImageIds {  
public:  
  
    static const GUID AssetsGuid;  
  
    static const int MyImage1 = 0;  
    static const int MyImage2 = 1;  
  
};  
  
__declspec(selectany) const GUID MyImageIds::AssetsGuid = {0x442d8739,0xefde,0x46a4,{0x8f,0x29,0xe3,0xa1,0xe5,0xe7,0xf8,0xb4}};  
  
}  
//-----------------------------------------------------------------------------  
// <auto-generated>  
//     This code was generated by the ManifestToCode tool.  
//     Tool Version: 14.0.15198  
// </auto-generated>  
//-----------------------------------------------------------------------------  
  
#pragma once  
  
#include "ImageParameters140.h"  
#include "MyImageIds.h"  
  
namespace MyImages {  
  
class MyMonikers {  
public:  
  
    static const ImageMoniker MyImage1;  
    static const ImageMoniker MyImage2;  
  
};  
  
__declspec(selectany) const ImageMoniker MyMonikers::MyImage1 = { MyImageIds::AssetsGuid, MyImageIds::MyImage1 };  
__declspec(selectany) const ImageMoniker MyMonikers::MyImage2 = { MyImageIds::AssetsGuid, MyImageIds::MyImage2 };  
  
}  
```  
  
 **Visual Basic 包裝函式**  
  
 一對簡單的映像識別碼和影像 moniker 類別的 Visual Basic 會類似下列程式碼：  
  
```vb  
' -----------------------------------------------------------------------------  
'  <auto-generated>  
'      This code was generated by the ManifestToCode tool.  
'      Tool Version: 14.0.15198  
'  </auto-generated>  
' -----------------------------------------------------------------------------  
  
Imports System  
  
Namespace MyImages  
  
    Public Module MyImageIds  
  
        Public Shared ReadOnly AssetsGuid As Guid = New Guid("{442d8739-efde-46a4-8f29-e3a1e5e7f8b4}")  
  
        Public Const MyImage1 As Integer = 0  
        Public Const MyImage2 As Integer = 1  
  
    End Module  
  
End Namespace  
' -----------------------------------------------------------------------------  
'  <auto-generated>  
'      This code was generated by the ManifestToCode tool.  
'      Tool Version: 14.0.15198  
'  </auto-generated>  
' -----------------------------------------------------------------------------  
  
Imports Microsoft.VisualStudio.Imaging.Interop  
  
Namespace MyImages  
  
    Public Module MyMonikers  
  
        Public Readonly Property MyImage1  
            Get  
                Return New ImageMoniker With {.Guid = MyImageIds.AssetsGuid, .Id = MyImageIds.MyImage1}  
            End Get  
        End Property  
  
        Public Readonly Property MyImage2  
            Get  
                Return New ImageMoniker With {.Guid = MyImageIds.AssetsGuid, .Id = MyImageIds.MyImage2}  
            End Get  
        End Property  
  
    End Module  
  
End Namespace  
```  
  
 **VSCT 包裝函式**  
  
 .Vsct 檔案的映像識別碼的一組會如下所示：  
  
```xml  
<?xml version='1.0' encoding='utf-8'?>  
<!--  
 [auto-generated]  
     This code was generated by the ManifestToCode tool.  
     Tool Version: 14.0.15198  
 [/auto-generated]  
-->  
<CommandTable xmlns="http://schemas.microsoft.com/VisualStudio/2005-10-18/CommandTable">  
  <Symbols>  
    <GuidSymbol name="AssetsGuid" value="{442d8739-efde-46a4-8f29-e3a1e5e7f8b4}">  
      <IDSymbol name="MyImage1" value="0" />  
      <IDSymbol name="MyImage2" value="1" />  
    </GuidSymbol>  
  </Symbols>  
</CommandTable>  
```
