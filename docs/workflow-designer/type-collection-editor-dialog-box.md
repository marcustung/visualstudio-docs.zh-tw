---
title: 工作流程設計工具-型別集合編輯器對話方塊
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- TypeCollectionEditor.UI
ms.assetid: 63cdea6b-bca2-4c06-b8b4-c8faabd40726
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 191635364c445bc3959ee2f5f63c7c72c71f171d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60093120"
---
# <a name="type-collection-editor-dialog-box"></a>型別集合編輯器對話方塊

**型別集合編輯器** 對話方塊用來新增至已知型別的**傳送**並**接收**活動。 此對話方塊也會用來加入泛用型別引數**InvokeMethod**活動。 當用於**傳送**並**接收**活動，以加入已知型別，**型別集合編輯器**對話方塊需要是唯一的型別新增項目。 如果加入重複的型別，並認可變更，即可**確定**，會傳回錯誤訊息。 當用於**InvokeMethod**活動，將泛型型別引數**型別集合編輯器**對話方塊允許重複的型別。

如需詳細資訊，請參閱 <<c0> [ 資料合約已知型別](/dotnet/framework/wcf/feature-details/data-contract-known-types)。

下表描述的使用者介面 (UI) 項目**型別集合** 對話方塊。

|UI 項目|描述|
|-|-----------------|
|**類型清單**|已加入或已移除之型別的清單。|

## <a name="to-bring-up-the-type-collection-editor-for-the-send-and-receive-activities"></a>若要顯示 Send  與 Receive 活動的型別集合編輯器

1. 選取 **傳送**或是**接收**設計 檢視中的活動。

2. 按下**F4**即可啟動**屬性**視窗。

3. 在 **屬性**視窗中，按一下 下的一步 的省略符號按鈕**KnownTypes**屬性。

## <a name="to-bring-up-the-type-collection-editor-for-the-invokemethod-activity"></a>若要顯示 InvokeMethod 活動的型別集合編輯器

1. 選取  **InvokeMethod** 設計 檢視中的活動。

2. 按下**F4**即可啟動**屬性**視窗。

3. 在 **屬性**視窗中，按一下 下的一步 的省略符號按鈕**GenericTypeArguments**屬性。