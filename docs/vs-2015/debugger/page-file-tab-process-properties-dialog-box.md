---
title: 分頁檔索引標籤、 處理序屬性對話方塊 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- Process properties for Windows NT
ms.assetid: daf41a06-8a55-48f6-95f5-49a8416bd308
caps.latest.revision: 7
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 24fdba37be2373623d94f03e45dc5e8a41a74b84
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58942377"
---
# <a name="page-file-tab-process-properties-dialog-box"></a>處理序屬性對話方塊、分頁檔索引標籤
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

使用**分頁檔**檢查分頁檔的處理程序 索引標籤。 若要顯示[處理序屬性對話方塊](../debugger/process-properties-dialog-box.md)，焦點移至[處理序檢視](../debugger/processes-view.md)視窗。 在樹狀目錄中，選取任何處理序節點，然後選擇**屬性**從**檢視**功能表。  
  
 下列設定位於**分頁檔** 索引標籤：  
  
|進入|描述|  
|-----------|-----------------|  
|**分頁檔位元組**|目前的分頁檔中使用此程序的頁面數目。 分頁檔會儲存資料的處理序使用，但不是包含其他檔案中的頁面。 分頁檔由所有處理程序，並在分頁檔的空間不足可能會導致錯誤，而其他處理序正在執行。|  
|**尖峰分頁檔位元組**|頁面的分頁檔中使用此程序的數目上限。|  
|**分頁錯誤**|在此程序中執行的執行緒的分頁錯誤數目。 當執行緒參考不是在它的工作集主記憶體中的虛擬記憶體分頁時，就會發生分頁錯誤。 因此，頁面將不會擷取從磁碟如果它在待命清單上，因此已經在主記憶體，或如果它正由另一個處理與共用的頁面。|
