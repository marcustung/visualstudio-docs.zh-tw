---
title: HOW TO：擴充特定領域語言設計工具
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 85a4356837180d13428acf34636f28cca668a423
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60063149"
---
# <a name="how-to-extend-the-domain-specific-language-designer"></a>HOW TO：擴充特定領域語言設計工具

您可以對您用來編輯在 DSL 定義設計工具的延伸模組。 類型的擴充功能，可讓您加入功能表命令加入處理常式，如拖曳，然後按兩下筆勢和特定類型的值或關聯性變更時觸發的規則。 延伸模組可以封裝成 Visual Studio 整合擴充功能 (VSIX)，並散發給其他使用者。

範例程式碼和有關這項功能的詳細資訊，請參閱 Visual Studio [Visualization and Modeling SDK](https://code.msdn.microsoft.com/Visualization-and-Modeling-313535db)。

## <a name="set-up-the-solution"></a>設定解決方案

設定包含您的延伸模組的程式碼的專案，並將專案匯出的 VSIX 專案。 方案可以包含相同的 VSIX 會納入其他專案。

### <a name="to-create-a-dsl-designer-extension-solution"></a>若要建立的 DSL 設計工具擴充功能方案

1. 建立新的專案使用**類別庫**專案範本。 這個專案會包含您的擴充功能的程式碼。

2. 建立新**VSIX 專案**專案。

     選取 **加入至方案**。

     *Source.extension.vsixmanifest* VSIX 資訊清單編輯器中開啟。

3. 上方的 [內容] 欄位中，按一下**加入內容**。

4. 中**加入內容** 對話方塊中，將**內容類型選取**來**MEF 元件**，並將**專案**您類別庫專案。

5. 按一下 **選取版本**並確定**Visual Studio Enterprise**已核取。

6. 請確定 VSIX 專案方案的啟始專案。

7. 在類別庫專案中，加入下列組件的參考：

     Microsoft.VisualStudio.CoreUtility

     Microsoft.VisualStudio.Modeling.Sdk.11.0

     Microsoft.VisualStudio.Modeling.Sdk.Diagrams.11.0

     Microsoft.VisualStudio.Modeling.Sdk.DslDefinition.11.0

     Microsoft.VisualStudio.Modeling.Sdk.Integration.11.0

     System.ComponentModel.Composition

     System.Drawing

     System.Drawing.Design

     System.Windows.Forms

## <a name="test-and-deployment"></a>測試和部署

若要測試本主題中的任何延伸模組，建置並執行方案。 Visual Studio 的實驗執行個體隨即開啟。 在本例中，開啟 DSL 方案。 編輯 DslDefinition 圖表。 可以看到延伸模組行為。

若要為主要的 Visual Studio 中，以及其他電腦，請部署延伸模組，請遵循下列步驟：

1. VSIX 安裝檔案，尋找 VSIX 專案中分類收納\\*\*\\\*.vsix

2. 這個檔案複製到目標電腦，並在 Windows 檔案總管 （或檔案總管） 中，按兩下它。

     若要確認延伸模組已安裝 Visual Studio 延伸模組管理員隨即開啟。

若要解除安裝擴充功能，請遵循下列步驟：

1. 在 Visual Studio 中，在**工具**功能表上，按一下**延伸模組管理員**。

2. 選取擴充功能，並將它刪除。

## <a name="add-a-shortcut-menu-command"></a>加入快顯功能表命令

若要讓 DSL 設計工具介面上或在 [DSL 總管] 視窗中顯示的捷徑功能表命令，撰寫類別，如下列所示。

此類別必須實作`ICommandExtension`必須有屬性和`DslDefinitionModelCommandExtension`。

```csharp
using System.Collections.Generic;
using System.ComponentModel.Composition;
using System.Linq;
using Microsoft.VisualStudio.Modeling.Diagrams;
using Microsoft.VisualStudio.Modeling.Diagrams.ExtensionEnablement;
using Microsoft.VisualStudio.Modeling.DslDefinition;
using Microsoft.VisualStudio.Modeling.DslDefinition.ExtensionEnablement;
using Microsoft.VisualStudio.Modeling.DslDesigner;
using Microsoft.VisualStudio.Modeling.ExtensionEnablement;

namespace Fabrikam.SimpleDslDesignerExtension
{
  /// <summary>
  /// Command extending the DslDesigner.
  /// </summary>
  [DslDefinitionModelCommandExtension]
  public class MyDslDesignerCommand : ICommandExtension
  {
    /// <summary>
    /// Selection Context for this command
    /// </summary>
    [Import]
    IVsSelectionContext SelectionContext { get; set; }

    /// <summary>
    /// Is the command visible and active?
    /// This is called when the user right-clicks.
    /// </summary>
    public void QueryStatus(IMenuCommand command)
    {
      command.Visible = true;
      // Is there any selected DomainClasses in the Dsl explorer?
      command.Enabled =
        SelectionContext.AtLeastOneSelected<DomainClass>();

      // Is there any selected ClassShape on the design surface?
      command.Enabled |=
        (SelectionContext.GetCurrentSelection<ClassShape>()
                .Count() > 0);
    }
    /// <summary>
    /// Executes the command
    /// </summary>
    /// <param name="command">Command initiating this action</param>
    public void Execute(IMenuCommand command)
    {
      ...
    }
    /// <summary>
    /// Label for the command
    /// </summary>
    public string Text
    {
      get { return "My Command"; }
    }
  }
}
```

## <a name="handle-mouse-gestures"></a>處理滑鼠筆勢

程式碼很類似功能表命令的程式碼。

```csharp
[DslDefinitionModelGestureExtension]
 class MouseGesturesExtensions : IGestureExtension
 {
  /// <summary>
  /// Double-clicking on a shape representing a Domain model element displays this model element in a dialog box
  /// </summary>
  /// <param name="targetElement">Shape element on which the user has clicked</param>
  /// <param name="diagramPointEventArgs">event args for this double-click</param>
  public void OnDoubleClick(ShapeElement targetElement,
       DiagramPointEventArgs diagramPointEventArgs)
  {
   ModelElement modelElement = PresentationElementHelper.
        GetDslDefinitionModelElement(targetElement);
   if (modelElement != null)
   {
    MessageBox.Show(string.Format(
      "Double clicked on {0}", modelElement.ToString()),
      "Model element double-clicked");
   }
  }

  /// <summary>
  /// Tells if the DslDesigner can consume the to-be-dropped information
  /// </summary>
  /// <param name="targetMergeElement">Shape on which we try to drop</param>
  /// <param name="diagramDragEventArgs">Drop event</param>
  /// <returns><c>true</c> if we can consume the to be dropped data, and <c>false</c> otherwise</returns>
  public bool CanDragDrop(ShapeElement targetMergeElement,
        DiagramDragEventArgs diagramDragEventArgs)
  {
   if (diagramDragEventArgs.Data.GetDataPresent(DataFormats.FileDrop))
   {
    diagramDragEventArgs.Effect = DragDropEffects.Copy;
    return true;
   }
   return false;
  }

  /// <summary>
  /// Processes the drop by displaying the dropped text
  /// </summary>
  /// <param name="targetMergeElement">Shape on which we dropped</param>
  /// <param name="diagramDragEventArgs">Drop event</param>
  public void OnDragDrop(ShapeElement targetDropElement, DiagramDragEventArgs diagramDragEventArgs)
  {
   if (diagramDragEventArgs.Data.GetDataPresent(DataFormats.FileDrop))
   {
    string[] droppedFiles =
      diagramDragEventArgs.Data.
               GetData(DataFormats.FileDrop) as string[];
    MessageBox.Show(string.Format("Dropped text {0}",
        string.Join("\r\n", droppedFiles)), "Dropped Text");
   }
  }
 }
```

## <a name="respond-to-value-changes"></a>回應值變更

這個處理常式必須正常運作的領域模型。 我們提供簡單的領域模型。

```csharp
using System.Diagnostics;
using Microsoft.VisualStudio.Modeling;
using Microsoft.VisualStudio.Modeling.DslDefinition;
namespace Fabrikam.SimpleDslDesignerExtension
{
  /// <summary>
  /// Rule firing when the type of a domain model property is changed. The change is displayed
  /// in the debugger (Output window of the Visual Studio instance debugging this extension)
  /// </summary>
  [RuleOn(typeof(PropertyHasType))]
  public class DomainPropertyTypeChangedRule : RolePlayerChangeRule
  {
    /// <summary>
    /// Method called when the Type of a Domain Property
    /// is changed by the user in a DslDefinition
    /// </summary>
    /// <param name="e"></param>
    public override void RolePlayerChanged(RolePlayerChangedEventArgs e)
    {
      // We are only interested in the type
      if (e.DomainRole.Id == PropertyHasType.TypeDomainRoleId)
      {
        PropertyHasType relationship =
           e.ElementLink as PropertyHasType;
        DomainType newType = e.NewRolePlayer as DomainType;
        DomainType oldType = e.OldRolePlayer as DomainType;
        DomainProperty property = relationship.Property;

         // We write about the Type change in the debugguer
        Debug.WriteLine(string.Format("The type of the Domain property '{0}' of domain class '{1}' changed from '{2}' to '{3}'",
          property.Name,
          property.Class.Name,
          oldType.GetFullName(false),
          newType.GetFullName(false))
} }  }  );
```

下列程式碼會實作簡單的模型。 建立新的 GUID 來取代預留位置。

```csharp
using System;
using System.ComponentModel.Composition;
using Microsoft.VisualStudio.Modeling;
using Microsoft.VisualStudio.Modeling.DslDefinition;
namespace Fabrikam.SimpleDslDesignerExtension
{
    /// <summary>
    /// Simplest possible domain model
    /// needed only for extension rules.
    /// </summary>
    [DomainObjectId(SimpleDomainModelExtension.DomainModelId)]
    public class SimpleDomainModelExtension : DomainModel
    {
        // Id of this domain model extension
        // Please replace this with a new GUID:
        public const string DomainModelId =
                  "00000000-0000-0000-0000-000000000000";

        /// <summary>
        /// Constructor for the domain model extension
        /// </summary>
        /// <param name="store">Store in which the domain model will be loaded</param>
        public SimpleDomainModelExtension(Store store)
            : base(store, new Guid(SimpleDomainModelExtension.DomainModelId))
        {

        }

        /// <summary>
        /// Rules brought by this domain model extension
        /// </summary>
        /// <returns></returns>
        protected override System.Type[] GetCustomDomainModelTypes()
        {
            return new Type[] {
                     typeof(DomainPropertyTypeChangedRule)
                              };
        }
    }

    /// <summary>
    /// Provider for the DomainModelExtension
    /// </summary>
    [Export(typeof(DomainModelExtensionProvider))]    [ProvidesExtensionToDomainModel(typeof(DslDefinitionModelDomainModel))]
    public class SimpleDomainModelExtensionProvider
          : DomainModelExtensionProvider
    {
        /// <summary>
        /// Extension model type
        /// </summary>
        public override Type DomainModelType
        {
            get
            {
                return typeof(SimpleDomainModelExtension);
            }
        }

    }
}
```