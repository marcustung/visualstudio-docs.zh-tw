---
title: IDebugDocumentTextEvents2::onRemoveText | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugDocumentTextEvents2::OnRemoveText
helpviewer_keywords:
- IDebugDocumentTextEvents2::onRemoveText
ms.assetid: 1ebeabb2-52a1-4ccc-83cd-9ae7c3541783
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: df0504515d8ddacb4e21918cefffe76f8e96d6a1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56682631"
---
# <a name="idebugdocumenttextevents2onremovetext"></a>IDebugDocumentTextEvents2::onRemoveText
告知偵錯封裝文字具有從文件中移除。

## <a name="syntax"></a>語法

```cpp
HRESULT onRemoveText( 
   TEXT_POSITION pos,
   DWORD         dwNumToRemove
);
```

```csharp
int onRemoveText( 
   enum_TEXT_POSITION pos,
   uint               dwNumToRemove
);
```

#### <a name="parameters"></a>參數
 `pos`

 [in]A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)結構，表示已移除文字的位置。

 `dwNumToRemove`

 [in]指定文字的已移除的字元數目。

## <a name="return-value"></a>傳回值
 如果成功，則傳回`S_OK`; 否則傳回錯誤碼。

## <a name="see-also"></a>另請參閱
- [IDebugDocumentTextEvents2](../../../extensibility/debugger/reference/idebugdocumenttextevents2.md)
- [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)