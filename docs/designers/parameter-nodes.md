---
title: 參數節點
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: da54db0b-3a3d-48dc-858c-7ac43aa04b13
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c99986b65e1b396a92e667ceb4eeff2b92a58dc6
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/08/2019
ms.locfileid: "55944503"
---
# <a name="parameter-nodes"></a>參數節點

在著色器設計工具中，參數節點代表每次繪製時都受應用程式控制的著色器輸入，例如材質屬性、定向光線、觀景窗位置及時間。 因為您可以透過每次的繪製呼叫，變更這些參數，所以能夠使用相同的著色器提供物件不同的外觀。

## <a name="parameter-node-reference"></a>參數節點參考

|節點|Details|屬性|
|----------|-------------|----------------|
|**觀景窗世界空間位置**|觀景窗在世界空間中的位置。<br /><br /> **輸出：**<br /><br /> `Output`: `float4`<br /> 相機的位置。|無|
|**光方向**|定義世界空間中光源投射方向的向量。<br /><br /> 您可以用這個向量來計算世界空間中的光線和反射比重。<br /><br /> **輸出：**<br /><br /> `Output`: `float3`<br /> 從目前像素到光源的向量。|無|
|**材質環境**|目前像素的擴散色彩比重屬於間接光源。<br /><br /> 像素的擴散色彩會模擬光源和粗糙表面如何相互影響。 您可以用材質環境參數約略估計間接光源在實際物件外觀上的比重。<br /><br /> **輸出：**<br /><br /> `Output`: `float4`<br /> 目前像素的擴散色彩，由間接 (也就是環境) 光源造成。|**存取權**<br /> [公用] 允許從模型編輯器設定此屬性，否則為 [私用]。<br /><br /> **值**<br /> 目前像素的擴散色彩，由間接 (也就是環境) 光源造成。|
|**材質擴散**|色彩，描述目前像素如何使直接光源擴散。<br /><br /> 像素的擴散色彩會模擬光源和粗糙表面如何相互影響。 您可以使用材質擴散參數來變更目前像素使直接光源 (也就是定向、點及聚光光線) 擴散的方式。<br /><br /> **輸出：**<br /><br /> `Output`: `float4`<br /> 色彩，描述目前像素如何使直接光源擴散。|**存取權**<br /> [公用] 允許從模型編輯器設定此屬性，否則為 [私用]。<br /><br /> **值**<br /> 色彩，描述目前像素如何使直接光源擴散。|
|**材質放射**|目前像素的色彩比重屬於自身提供的光源。<br /><br /> 您可以用此來模擬發光物件，也就是提供自身光線的物件。 此光線並不會影響其他物件。<br /><br /> **輸出：**<br /><br /> `Output`: `float4`<br /> 目前像素的色彩比重，由自行提供的光源造成。|**存取權**<br /> [公用] 允許從模型編輯器設定此屬性，否則為 [私用]。<br /><br /> **值**<br /> 目前像素的色彩比重，由自行提供的光源造成。|
|**材質反射**|色彩，描述目前像素如何使直接光源反射。<br /><br /> 像素的反射色彩會模擬光源和平滑、鏡面般的表面如何相互影響。 您可以使用材質反射參數來變更目前像素使直接光源 (也就是定向、點及聚光光線) 反射的方式。<br /><br /> **輸出：**<br /><br /> `Output`: `float4`<br /> 色彩，描述目前像素如何使直接光源反射。|**存取權**<br /> [公用] 允許從模型編輯器設定此屬性，否則為 [私用]。<br /><br /> **值**<br /> 色彩，描述目前像素如何使直接光源反射。|
|**材質光澤度**|描述反射反白顯示項目之濃度的純量值。<br /><br /> 光澤度越大，反射亮部會變得越強烈和深遠。<br /><br /> **輸出：**<br /><br /> `Output`: `float`<br /> 一個指數項，描述目前像素上的反射亮部濃度。|**存取權**<br /> [公用] 允許從模型編輯器設定此屬性，否則為 [私用]。<br /><br /> **值**<br /> 指數，定義目前像素上反射亮部的濃度。|
|**標準化時間**|秒數，標準化為範圍 [0, 1]，如此，當時間達到 1 時，就會重設為 0。<br /><br /> 您可以將這個當做著色器計算中的參數，如此，舉例來說，就能以動畫方式顯示材質座標、色彩值或其他屬性。<br /><br /> **輸出：**<br /><br /> `Output`: `float`<br /> 標準化時間，以秒為單位。|無|
|**時間**|時間 (秒)。<br /><br /> 您可以將這個當做著色器計算中的參數，如此，舉例來說，就能以動畫方式顯示材質座標、色彩值或其他屬性。<br /><br /> **輸出：**<br /><br /> `Output`: `float`<br /> 時間，以秒為單位。|無|