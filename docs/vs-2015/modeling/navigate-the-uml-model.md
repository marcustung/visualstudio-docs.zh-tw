---
title: 巡覽 UML 模型 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
helpviewer_keywords:
- UML API
ms.assetid: 6d789b6d-2aa9-4ceb-92c4-84a300065a76
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b61492d992d37d7377e73185202bfbdd97063195
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60116663"
---
# <a name="navigate-the-uml-model"></a>巡覽 UML 模型
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主題說明 UML 模型的主要類型。  
  
## <a name="the-model-elements-model-and-model-store"></a>模型項目、模型和模型存放區  
 組件中定義的型別**Microsoft.VisualStudio.Uml.Interfaces.dll**對應到定義中的型別[UML 規格，2.1.2 版](http://www.omg.org/spec/UML/2.1.2/Superstructure/PDF/)。  
  
 「UML 規格」中的類型會實現成 Visual Studio 中的介面。 字母 'I' 會附加至每個類型的名稱。 例如：<xref:Microsoft.VisualStudio.Uml.Classes.IElement>、<xref:Microsoft.VisualStudio.Uml.Classes.IClass>、<xref:Microsoft.VisualStudio.Uml.Interactions.IInteraction>、<xref:Microsoft.VisualStudio.Uml.Classes.IOperation>。  
  
 IElement 以外的所有類型都繼承一或多個超級類型的屬性。  
  
- 如需模型類型的摘要，請參閱 < [UML 模型項目類型](../modeling/uml-model-element-types.md)。  
  
- 完整的 api 的詳細資訊，請參閱 < [UML 模型擴充性的 API 參考](../modeling/api-reference-for-uml-modeling-extensibility.md)。  
  
### <a name="relationships"></a>關聯性  
 「UML 規格」中所定義的屬性和關聯性會實作為 .NET 屬性。  
  
 大部分的關聯性都可以雙向進行巡覽。 一個關聯性對應於一組屬性，而每一端的類型上會有一個屬性。 例如，`IElement.Owner` 和 `IElement.OwnedElements` 屬性代表關聯性的兩端。 因此，這個運算式一律會評估為 true：  
  
 `IElement c; ...  c.OwnedElements.All(x => x.Owner == c)`  
  
 也可以透過具有專屬屬性的物件來代表多個關聯性 (例如 IAssociation)。  
  
 如果您從模型中刪除項目，則會自動刪除它參與的任何關聯性，並更新另一端的屬性。  
  
 如果「UML 規格」將多重性 0..1 指派給屬性，則值可能是 `null`。 多重性的最大值大於 1，表示.NET 屬性類型：`IEnumerable<`*型別*`>`。  
  
 如需有關如何周遊關聯性的詳細資訊，請參閱 <<c0> [ 使用 UML API 巡覽關聯性](../modeling/navigate-relationships-with-the-uml-api.md)。  
  
### <a name="the-ownership-tree"></a>擁有權樹狀結構  
 模型包含 <xref:Microsoft.VisualStudio.Uml.Classes.IElement> 物件的樹狀結構。 每個項目都具有 `OwnedElements` 和 `Owner` 屬性。  
  
 在大部分情況下，其他具有更特定名稱的屬性也會參考 `Owner` 和 `OwnedElements` 屬性的目標。 例如，UML 類別會擁有每個 UML 作業。 因此，<xref:Microsoft.VisualStudio.Uml.Classes.IOperation> 具有名為 <xref:Microsoft.VisualStudio.Uml.Classes.IOperation.Class%2A> 的屬性，而在每個 <xref:Microsoft.VisualStudio.Uml.Classes.IOperation> 物件中則是 `Class == Owner`。  
  
 樹狀結構中的最上層項目 (沒有 Owner) 是 <xref:Microsoft.VisualStudio.Uml.AuxiliaryConstructs.IModel> IModel 包含在 <xref:Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml.IModelStore> 內，在其中，它是 <xref:Microsoft.VisualStudio.ArchitectureTools.Extensibility.Uml.IModelStore.Root%2A>。  
  
 每個模型項目都會建立具有一個 Owner。 如需詳細資訊，請參閱 < [UML 模型中建立項目和關聯性](../modeling/create-elements-and-relationships-in-uml-models.md)。  
  
 ![類別圖表：模型、 圖表、 圖形與項目](../modeling/media/uml-mm1.png "UML_MM1")  
  
## <a name="shapes-and-diagrams"></a>圖案和圖表  
 UML 模型中的項目可以顯示在圖表上。 不同類型的圖表可以顯示不同的 IElement 子類型。  
  
 在某些情況下，項目會出現在多個圖表上。 例如，IUseCase 項目可以有數個 IShape，而它們可以出現在一個圖表或不同圖表上。  
  
 圖形是在樹狀結構中進行組織。 樹狀結構的邊緣是透過 ParentShape 和 ChildShapes 屬性來表示。 圖表是唯一沒有父項的圖形。 圖表介面上的圖形是由較小的部分所組成。 例如，類別圖形具有屬性和作業的區間。  
  
 如圖形的詳細資訊，請參閱 <<c0> [ 在圖表上顯示 UML 模型](../modeling/display-a-uml-model-on-diagrams.md)。  
  
## <a name="access-to-the-model-in-extensions"></a>擴充功能中模型的存取權  
 在定義為 MEF 元件的 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 擴充功能中，您可以宣告從執行擴充功能的內容中匯入資訊的屬性。  
  
|屬性類型|這提供下列項目的存取權|詳細資訊|  
|--------------------|----------------------------------|----------------------|  
|Microsoft.VisualStudio.ArchitectureTools.Extensibility.Presentation<br /><br /> .IDiagramContext<br /><br /> (在 Microsoft.VisualStudio.ArchitectureTools.Extensibility.dll 中)|目前焦點圖。|[在模型圖上定義功能表命令](../modeling/define-a-menu-command-on-a-modeling-diagram.md)|  
|Microsoft.VisualStudio.Modeling.ExtensionEnablement<br /><br /> .ILinkedUndoContext<br /><br /> (在 Microsoft.VisualStudio.Modeling.Sdk.[version].dll 中)|可讓您將變更群組為異動。|[使用異動連結 UML 模型更新](../modeling/link-uml-model-updates-by-using-transactions.md)|  
|Microsoft.VisualStudio.Shell .SVsServiceProvider<br /><br /> (在 Microsoft.VisualStudio.Shell.Immutable.[version].dll 中)|主機 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]。 您可以在這裡存取檔案、專案和其他層面。|[使用 Visual Studio API 開啟 UML 模型](../modeling/open-a-uml-model-by-using-the-visual-studio-api.md)|  
  
### <a name="to-get-the-context"></a>取得內容  
 在擴充功能類別內，宣告下列一個或兩個介面：  
  
```  
[Import] public IDiagramContext DiagramContext { get; set; }  
  
```  
  
 Managed Extensibility Framework (MEF) 會將這些項目繫結至從中取得目前圖表、模型存放區、根物件等的定義：  
  
```  
IDiagram diagram = this.DiagramContext.CurrentDiagram;  
IClassDiagram classDiagram = diagram as IClassDiagram;  
       // or diagrams of other types  
IModelStore modelStore = diagram.ModelStore;  
IModel model = modelStore.Root;  
foreach (IDiagram diagram in modelStore.Diagrams) {...}  
foreach (IElement element in modelStore.AllInstances<IUseCase>) {...}  
```  
  
### <a name="to-get-the-current-selection"></a>取得目前選取範圍  
  
```  
// All selected shapes and their elements  
foreach (IShape shape in diagram.SelectedShapes)  
{    
   IDiagram selectedDiagram = shape as IDiagram;  
   if (selectedDiagram != null)  
   { // no shape selected - user right-clicked the diagram  
     ... Context.CurrentDiagram ...  
   }  
   else  
   {  
     IElement selectedElement = shape.Element;  
   ...}  
// All selected shapes that display a specfic type of element  
foreach (IShape<IInterface> in   
   diagram.GetSelectedShapes<IInterface>())   
{...}  
```  
  
## <a name="accessing-another-model-or-diagrams"></a>存取另一個模型或圖表  
 您可以：  
  
- 使用 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 模型匯流排，來建立不同模型中項目之間的連結。 如需詳細資訊，請參閱 <<c0> [ 整合 UML 模型與其他模型及工具](../modeling/integrate-uml-models-with-other-models-and-tools.md)。  
  
- 以唯讀模式載入模型專案和圖表，而不讓它顯示在 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 使用者介面中。 如需詳細資訊，請參閱 <<c0> [ 讀取程式碼中的 UML 模型](../modeling/read-a-uml-model-in-program-code.md)。  
  
- 在 [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] 中開啟模型專案和其圖表，然後存取內容。 如需詳細資訊，請參閱 <<c0> [ 使用 Visual Studio API 開啟 UML 模型](../modeling/open-a-uml-model-by-using-the-visual-studio-api.md)。  
  
## <a name="see-also"></a>另請參閱  
 [擴充 UML 模型和圖表](../modeling/extend-uml-models-and-diagrams.md)   
 [使用 UML API 進行程式設計](../modeling/programming-with-the-uml-api.md)
