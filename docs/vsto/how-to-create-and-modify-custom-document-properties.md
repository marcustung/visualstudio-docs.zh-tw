---
title: HOW TO：建立和修改自訂文件屬性
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- custom document properties
- documents [Office development in Visual Studio], properties
- document properties [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7d6ef8332a5adc21e25f2a414c5b359e48cf1ba7
ms.sourcegitcommit: 4d9c54f689416bf1dc4ace058919592482d02e36
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2019
ms.locfileid: "58194586"
---
# <a name="how-to-create-and-modify-custom-document-properties"></a>HOW TO：建立和修改自訂文件屬性
  上列 Microsoft Office 應用程式提供與文件一起儲存的內建屬性。 此外，如果您有想要與文件一起儲存的其他資訊，則可以建立和修改自訂文件屬性。

 [!INCLUDE[appliesto_docprops](../vsto/includes/appliesto-docprops-md.md)]

 若要使用自訂屬性中使用的文件的 CustomDocumentProperties 屬性。 例如，在 Microsoft Office Excel 的文件層級專案中，請使用 <xref:Microsoft.Office.Tools.Excel.Workbook.CustomDocumentProperties%2A> 類別的 `ThisWorkbook` 屬性。 在 Excel 的 VSTO 增益集專案中，則請使用 <xref:Microsoft.Office.Interop.Excel._Workbook.CustomDocumentProperties%2A> 物件的 <xref:Microsoft.Office.Interop.Excel.Workbook> 屬性。 這些屬性會傳回 <xref:Microsoft.Office.Core.DocumentProperties> 物件，它是 <xref:Microsoft.Office.Core.DocumentProperty> 物件的集合。 您可以按照名稱或集合內的索引，使用該集合的 `Item` 屬性擷取特定的屬性。

 下列範例示範如何在 Excel 的文件層級自訂中加入自訂屬性，並指派該屬性的值。

## <a name="example"></a>範例
 [!code-vb[Trin_VstcoreProgramming#6](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/ThisWorkbook.vb#6)]
 [!code-csharp[Trin_VstcoreProgramming#6](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/ThisWorkbook.cs#6)]

## <a name="robust-programming"></a>穩固程式設計
 嘗試存取未定義之屬性的 `Value` 屬性將會引發例外狀況。

## <a name="see-also"></a>另請參閱
- [程式 VSTO 增益集](../vsto/programming-vsto-add-ins.md)
- [程式文件層級自訂](../vsto/programming-document-level-customizations.md)
- [如何：讀取和寫入文件屬性](../vsto/how-to-read-from-and-write-to-document-properties.md)
