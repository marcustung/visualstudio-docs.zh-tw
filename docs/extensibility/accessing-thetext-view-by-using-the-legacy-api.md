---
title: 使用舊版 API 存取 theText 檢視 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - text view
ms.assetid: 8f751f72-c972-4be3-84ee-19c281e02e25
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bce39d8ae736d9f7dcda8b18198053f90933b811
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/18/2019
ms.locfileid: "56335491"
---
# <a name="access-the-text-view-by-using-the-legacy-api"></a>使用舊版的 API 來存取 [文字] 檢視
文字檢視是儲存在文字緩衝區中的文字呈現。 您可以存取 [文字] 檢視下一節中所示，使用舊版 API。

## <a name="text-view-object"></a>文字檢視物件
 每個檢視是它自己的文字緩衝區，相關聯，而檢視上的資料緩衝區中的視窗。 下圖顯示的文字檢視物件，因為它由索引鍵的介面<xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>。

 ![Visual Studio 文字檢視物件](../extensibility/media/vstextview.gif)

 檢視是一種呈現文字緩衝區中。 它包含功能，例如自動換行和製作大綱，以便在檢視中看到的內容不是確切的緩衝區中的文字。

 檢視可讓其他服務或攔截連入的命令，並檢視採取行動之前採取動作的程序。 若要這樣做最常見的服務是語言服務。 語言服務可能需要，比方說，攔截 ENTER 鍵來提供自訂的縮排的行為或工具提示的命令。

## <a name="add-functionality-to-the-text-view"></a>將功能加入至文字檢視
 您可以藉由處理特定的按鍵輸入自訂文字檢視行為。 若要攔截的按鍵輸入，您實作<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewFilter>物件，並提供命令目標 (<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>) 監視和截距命令。

 [文字] 檢視會用於命令篩選器中的循序的架構。 新的命令篩選器 (<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>物件) 的呼叫加入至序列<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextView.AddCommandFilter%2A>方法。

 文字檢視的事件通知使用來提供<xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextViewEvents>介面。 實作此介面上接收到 [文字] 檢視的變更通知用戶端物件。 使用公開這個介面來文字檢視<xref:Microsoft.VisualStudio.OLE.Interop.IConnectionPointContainer>上的文字檢視，以從檢視收到變更通知的介面。

## <a name="see-also"></a>另請參閱

- [使用舊版的 API 來變更檢視設定](../extensibility/changing-view-settings-by-using-the-legacy-api.md)
- [使用文字管理員監視全域設定](../extensibility/using-the-text-manager-to-monitor-global-settings.md)