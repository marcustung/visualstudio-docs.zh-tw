---
title: 建置事件對話方塊 (Visual Basic)
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vb.ProjectPropertiesBuildEvents
helpviewer_keywords:
- build events
- build events, specifying
- pre-build events
- Build Events dialog box
- post-build events
ms.assetid: 3a81a7c7-39f9-47a8-ba5a-b351227f380e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d1fb6c532016ce37c33766af05fac19eac252c99
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55952420"
---
# <a name="build-events-dialog-box-visual-basic"></a>建置事件對話方塊 (Visual Basic)

使用 [建置事件] 對話方塊來指定組建設定指令。 您也可以指定執行任何建置前或建置後事件的條件。 如需詳細資訊，請參閱[＜How to：指定建置事件 (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md)。

**建置前事件命令列**

指定要在建置開始前執行的任何命令。 若要鍵入很長的命令，請按一下 [建置前進行編輯] 顯示[建置前事件/建置後事件命令列對話方塊](../../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)。

> [!NOTE]
> 如果專案是最新狀態，而且未觸發任何建置，則建置前事件不會執行。

**建置後事件命令列**

指定要在建置結束後執行的任何命令。 若要鍵入長命令，請按一下 [建置後進行編輯] 以顯示 [建置前事件/建置後事件命令列] 對話方塊。

> [!NOTE]
> 在執行 .bat 檔案的所有建置命令前方，加入 `call` 陳述式。 例如，`call C:\MyFile.bat` 或 `call C:\MyFile.bat call C:\MyFile2.bat`。

**執行建置後事件**

指定要執行建置後事件的條件，如下表所示。

|選項|結果|
|------------|------------|
|**永遠**|不論建置是否成功都會執行建置後事件。|
|**建置成功時**|如果建置成功，則會執行建置後事件。 即使專案是最新狀態，只要建置成功都會執行事件。 這是預設設定。|
|**當組建更新專案輸出時**|只有在編譯器的輸出檔 (.exe 或 .dll) 不同於先前的編譯器輸出檔時，才會執行建置後事件。 如果專案是最新狀態，便不會執行建置後事件。|

## <a name="see-also"></a>請參閱

- [專案設計工具、編譯頁面 (Visual Basic)](../../ide/reference/compile-page-project-designer-visual-basic.md)
- [如何：指定建置事件 (Visual Basic)](../../ide/how-to-specify-build-events-visual-basic.md)
- [建置前事件/建置後事件命令列對話方塊](../../ide/reference/pre-build-event-post-build-event-command-line-dialog-box.md)