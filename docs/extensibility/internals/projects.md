---
title: 專案 |Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- solutions [Visual Studio]
- custom tools [Visual Studio SDK]
- project subtypes [Visual Studio SDK]
- projects [Visual Studio SDK]
- project types [Visual Studio SDK]
ms.assetid: 237742e4-a638-4d5b-a9b3-6a69d627763c
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 853a131ce522da156f0e59aaea99bc289cd2a452
ms.sourcegitcommit: 23feea519c47e77b5685fec86c4bbd00d22054e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/26/2019
ms.locfileid: "56840900"
---
# <a name="projects"></a>專案
在 Visual Studio 中，專案是容器，開發人員用來組織原始程式碼檔和其他資源，會出現在**方案總管 中**。 一般而言，專案會儲存原始程式檔和資源，例如點陣圖檔案的參考的檔案 （例如，C# 專案的.csproj 檔案）。 可讓您組織、 建置、 偵錯及部署來源的程式碼的專案，請參考 Web 服務、 資料庫和其他資源。 Vspackage 可以擴充 Visual Studio 專案系統，三種主要方式：*專案類型*，*專案子類型*，並*自訂工具*。

## <a name="in-this-section"></a>本節內容
- [專案類型](../../extensibility/internals/project-types.md)

 *專案類型*加入新種類的專案，例如程式設計語言的支援。 比方說，Visual Studio 支援每種語言有它自己的專案類型，以及 IronPython 整合範例包括 IronPython 語言的專案類型。 您必須建立 C# 或 Visual Basic 自訂如何項目會建置、 偵錯、 部署，並顯示在以外的語言的專案類型**方案總管 中**。 如需詳細資訊，請參閱 <<c0> [ 專案類型](../../extensibility/internals/project-types.md)。

- [專案子類型](../../extensibility/internals/project-subtypes.md)

 *專案子類型*專案類型為基礎，而且可用以自訂建置、 偵錯和部署專案的方式。 Visual Studio 會使用智慧型裝置專案; 中的專案子類型他們藉由將新建立的程式從開發電腦複製到目標裝置自訂部署。 C# 和 Visual Basic 專案類型可以作為基礎專案子類型;C + + 專案類型不能。 您自己的專案類型也可用為基礎的專案子類型。 如需詳細資訊，請參閱 <<c0> [ 專案子類型](../../extensibility/internals/project-subtypes.md)。

- [Web 專案](../../extensibility/internals/web-projects.md)

 說明 Web 專案，進而建立 Web 應用程式。

- [新的專案產生：在幕後，第一部](../../extensibility/internals/new-project-generation-under-the-hood-part-one.md)和[產生新專案：在幕後，第二部分](../../extensibility/internals/new-project-generation-under-the-hood-part-two.md)

 說明實際發生的狀況時建立新的專案。

- [VSSDK 範例](https://aka.ms/vs2015sdksamples)包含 VSSDK 處理專案和方案的範例。

## <a name="related-sections"></a>相關章節
- [深入探索 Visual Studio SDK](../../extensibility/internals/inside-the-visual-studio-sdk.md)

 說明 Visual Studio 擴充性的不同層面。