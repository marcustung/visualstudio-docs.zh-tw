---
title: IDebugSymbolProviderDirect | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugSymbolProviderDirect interface
ms.assetid: 872b04a8-70de-4ab5-aceb-684c81828545
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: d546cae810d40a850bb3dd2758f2f659eecdd18e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/22/2019
ms.locfileid: "56697421"
---
# <a name="idebugsymbolproviderdirect"></a>IDebugSymbolProviderDirect
表示符號提供者可直接存取中繼資料和核心符號的介面。

## <a name="syntax"></a>語法

```
IDebugSymbolProviderDirect: IUnknown
```

## <a name="methods"></a>方法
 這個介面會實作下列方法：

|方法|描述|
|------------|-----------------|
|[GetAppIDFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getappidfromaddress.md)|擷取指定的偵錯位址的應用程式網域識別碼。|
|[GetCurrentModulesInfo](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesinfo.md)|擷取符號群組中的模組的相關資訊。|
|[GetCurrentModulesState](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getcurrentmodulesstate.md)|擷取符號提供者為成員的符號群組的相關資訊。|
|[GetMetaDataImport](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmetadataimport.md)|擷取中繼資料匯入資訊。|
|[GetMethodFromAddress](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getmethodfromaddress.md)|擷取在指定的偵錯位址之方法的相關資訊。|
|[GetSymUnmanagedReader](../../../extensibility/debugger/reference/idebugsymbolproviderdirect-getsymunmanagedreader.md)|擷取未受管理的程式碼的符號讀取器。|

## <a name="remarks"></a>備註
 使用這個介面時，來取代大部分的其他符號提供者介面。 它提供直接存取中繼資料和`CorSym`介面。

## <a name="requirements"></a>需求
 標頭：Sh.h

 命名空間：Microsoft.VisualStudio.Debugger.Interop

 組件︰Microsoft.VisualStudio.Debugger.Interop.dll