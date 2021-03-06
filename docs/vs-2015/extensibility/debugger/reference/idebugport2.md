---
title: IDebugPort2 | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugPort2
helpviewer_keywords:
- IDebugPort2 interface
ms.assetid: 8fd87f05-a950-4d14-b925-98be29d4facc
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c9227e2e05499feac628a5b90fc6e3d2a4399992
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58939532"
---
# <a name="idebugport2"></a>IDebugPort2
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

這個介面表示在電腦上的偵錯連接埠。  
  
## <a name="syntax"></a>語法  
  
```  
IDebugPort2 : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>實作者的附註  
 自訂的連接埠提供者會實作這個介面來代表電腦上的偵錯連接埠。  
  
 如果連接埠支援事件的傳送埠，它也必須實作<xref:System.Runtime.InteropServices.ComTypes.IConnectionPointContainer>介面，以支援<xref:System.Runtime.InteropServices.ComTypes.IConnectionPoint>介面，進而提供[IDebugPortEvents2](../../../extensibility/debugger/reference/idebugportevents2.md)介面。  
  
## <a name="notes-for-callers"></a>呼叫端資訊  
 若要呼叫[GetPort](../../../extensibility/debugger/reference/idebugportsupplier2-getport.md)或是[下列](../../../extensibility/debugger/reference/idebugportsupplier2-addport.md)傳回此介面，表示要求的通訊埠。  
  
## <a name="methods-in-vtable-order"></a>依照 Vtable 順序的方法  
 下表顯示的方法`IDebugPort2`。  
  
|方法|描述|  
|------------|-----------------|  
|[GetPortName](../../../extensibility/debugger/reference/idebugport2-getportname.md)|傳回的連接埠名稱。|  
|[GetPortId](../../../extensibility/debugger/reference/idebugport2-getportid.md)|傳回的連接埠識別碼。|  
|[GetPortRequest](../../../extensibility/debugger/reference/idebugport2-getportrequest.md)|傳回用來建立連接埠 （如果有的話） 的要求。|  
|[GetPortSupplier](../../../extensibility/debugger/reference/idebugport2-getportsupplier.md)|傳回此連接埠的連接埠供應商。|  
|[GetProcess](../../../extensibility/debugger/reference/idebugport2-getprocess.md)|傳回指定處理程序的識別項的處理序的介面。|  
|[EnumProcesses](../../../extensibility/debugger/reference/idebugport2-enumprocesses.md)|列舉連接埠上執行的所有處理程序。|  
  
## <a name="remarks"></a>備註  
 本機連接埠可存取所有的處理程序和本機電腦上執行的程式。 Windows CE 架構裝置的序列纜線連接或非 DCOM 電腦的網路連線，可能代表其他連接埠。 `IDebugPort2`介面用來尋找的名稱和識別碼的連接埠，列舉所有連接埠上執行的處理程序，並提供工具，啟動和終止的連接埠上的處理序。  
  
## <a name="requirements"></a>需求  
 標頭： msdbg.h  
  
 命名空間：Microsoft.VisualStudio.Debugger.Interop  
  
 組件︰Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>另請參閱  
 [核心介面](../../../extensibility/debugger/reference/core-interfaces.md)   
 [IDebugPortSupplier2](../../../extensibility/debugger/reference/idebugportsupplier2.md)   
 [IDebugCoreServer2](../../../extensibility/debugger/reference/idebugcoreserver2.md)
