---
title: HOW TO：設定電腦以開發 Office 方案
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- prerequisites [Office development in Visual Studio]
- Office development in Visual Studio, installing tools
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b1f87b9548aceab58e1a8e1c6178a1dca759c312
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60052841"
---
# <a name="how-to-configure-a-computer-to-develop-office-solutions"></a>HOW TO：設定電腦以開發 Office 方案
  若要設定開發電腦，讓您可以使用 Visual Studio 中的 Microsoft Office Developer Tools，請遵循本主題中的指示。 您必須擁有開發電腦上的系統管理權限，才能執行這些步驟。

### <a name="to-configure-the-development-computer"></a>設定開發電腦

1. 安裝包含 Office Developer Tools 的 Visual Studio 版本。 預設會安裝 Office Developer Tools。 如果您可以選取要安裝的功能，以自訂 Visual Studio 安裝，請確定**Microsoft Office Developer Tools**在安裝期間選取。 如需包含 Office developer tools 的 Visual Studio 版本的詳細資訊，請參閱[設定電腦以開發 Office 方案](../vsto/configuring-a-computer-to-develop-office-solutions.md)。

2. 安裝由 Visual Studio 中 Office Developer Tools 支援的 Office 版本。 如需詳細資訊，請參閱 <<c0> [ 設定電腦以開發 Office 方案](../vsto/configuring-a-computer-to-develop-office-solutions.md)。

     請確定您也針對所安裝的 Office 版本安裝 PIA。 PIA 預設會與 Office 一起安裝。 如果您修改了 Office 安裝，請確定 **.NET 程式設計支援**選取您想要為目標的應用程式的功能。

3. 如果您有 Visual Studio 的英文版，但使用非英文設定的 Windows，您可以安裝[!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]語言套件，查看[!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]中與 Windows 相同語言的訊息。 非英文版的 Visual Studio 會自動安裝語言套件。 語言套件是可從[Microsoft 下載中心](http://go.microsoft.com/fwlink/?LinkId=140386)。

## <a name="see-also"></a>另請參閱

- [開始使用&#40;在 Visual Studio 中的 Office 程式開發&#41;](../vsto/getting-started-office-development-in-visual-studio.md)
- [如何：安裝 Visual Studio Tools for Office runtime 可轉散發套件](../vsto/how-to-install-the-visual-studio-tools-for-office-runtime-redistributable.md)
- [如何：安裝 Office 主要 interop 組件](../vsto/how-to-install-office-primary-interop-assemblies.md)
