---
title: 繫結至功能表項目的的鍵盤快速鍵 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- keyboard command
- keyboards
- command key
- keyboard shortcuts
- menu items
ms.assetid: 19f483b6-4d3e-424e-9d68-dc129c788e47
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c799d2733c4deca07cdcbe087b1b694f9d1725e6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/23/2019
ms.locfileid: "58944287"
---
# <a name="binding-keyboard-shortcuts-to-menu-items"></a>將鍵盤快速鍵繫結至功能表項目
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

要繫結的自訂功能表命令鍵盤快速鍵，只要新增項目套件.vsct 檔。 本主題說明如何將鍵盤快速鍵對應至自訂的按鈕、 功能表項目或工具列命令，以及如何套用的預設編輯器中的鍵盤對應或將它限制成自訂編輯器。  
  
 若要將鍵盤快速鍵指派給現有的 Visual Studio 功能表項目中，請參閱[識別及自訂鍵盤快速鍵](../ide/identifying-and-customizing-keyboard-shortcuts-in-visual-studio.md)。  
  
## <a name="choosing-a-key-combination"></a>選擇的按鍵組合  
 Visual Studio 中已使用許多的鍵盤快速鍵。 您不應該指派給多個命令相同的快顯，因為重複的繫結很難偵測得到，而且也可能會造成無法預期的結果。 因此，它是個不錯的主意，確認快顯的可用性，才能將它指派。  
  
#### <a name="to-verify-the-availability-of-a-keyboard-shortcut"></a>若要確認可用性的鍵盤快速鍵  
  
1. 在 **工具 / 選項 / 環境**視窗中，選取**鍵盤**。  
  
2. 請確定**新的快速鍵**設為**Global**。  
  
3. 在 **按下快捷鍵**方塊中，輸入您想要使用的鍵盤快速鍵。  
  
    如果已在 Visual Studio 中，使用捷徑**目前所使用的快顯**方塊會顯示快顯目前呼叫的命令。  
  
4. 直到您找到未對應的其中一個，請嘗試不同的組合索引鍵。  
  
   > [!NOTE]
   >  使用 alt 鍵的鍵盤快速鍵可能會開啟功能表，並不是直接執行命令。 因此，**目前所使用的快顯**方塊可能是空白，當您輸入包含 ALT 捷徑。 您可以確認捷徑不會透過關閉開啟功能表**選項**] 對話方塊中，然後按 [索引鍵。  
  
   下列程序假設您有現有的 VSPackage，具有功能表命令。 如果您需要這麼做的說明，看看[建立具有功能表命令的擴充](../extensibility/creating-an-extension-with-a-menu-command.md)。  
  
#### <a name="to-assign-a-keyboard-shortcut-to-a-command"></a>若要指派給命令的鍵盤快速鍵  
  
1. 開啟.vsct 檔為您的封裝。  
  
2. 建立空`<KeyBindings>`區段之後`<Commands>`如果尚不存在。  
  
   > [!WARNING]
   >  如需有關索引鍵繫結的詳細資訊，請參閱[按鍵繫結關係](../extensibility/keybinding-element.md)。  
  
    在 `<KeyBindings>`區段中，建立`<KeyBinding>`項目。  
  
    設定`guid`和`id`您想要叫用命令的屬性。  
  
    設定`mod1`屬性設定為**控制**， **Alt**，或**Shift**。  
  
    按鍵繫結關係區段應該看起來像這樣：  
  
   ```xml  
   <KeyBindings>  
       <KeyBinding guid="<name of command set>" id="<name of command id>"  
           editor="guidVSStd97" key1="1" mod1="CONTROL"/>  
   </KeyBindings>  
  
   ```  
  
   如果您的鍵盤快速鍵需要兩個以上的索引鍵，將`mod2`和`key2`屬性。  
  
   在大部分情況下， **Shift**不應該使用而不需要的第二個修飾詞，因為它已按下會導致大部分英數字元的按鍵輸入大寫的字母或符號。  
  
   虛擬按鍵碼可讓您存取並沒有與其相關聯，例如，函式的索引鍵的字元的特殊按鍵和**退格鍵**索引鍵。 如需詳細資訊，請參閱 <<c0> [ 虛擬按鍵碼](http://go.microsoft.com/fwlink/?LinkID=105932)。  
  
   若要讓命令在 Visual Studio 編輯器，請設定`editor`屬性設定為`guidVSStd97`。  
  
   若要使命令只適用於自訂編輯器，將`editor`屬性所產生的自訂編輯器的名稱[!INCLUDE[vsprvs](../includes/vsprvs-md.md)]當您建立 VSPackage 的封裝範本包含自訂編輯器。 若要尋找的名稱值，請查看`<Symbols>`一節`<GuidSymbol>`節點其`name`結尾為屬性"`editorfactory`。 」這是自訂編輯器的名稱。  
  
## <a name="example"></a>範例  
 此範例中將鍵盤快速鍵 CTRL + ALT + C 繫結至名為的命令`cmdidMyCommand`名為封裝中`MyPackage`。  
  
```  
<CommandTable>  
. . .  
<Commands>  
. . .  
</Commands>  
<KeyBindings>  
  <KeyBinding guid="guidMyPackageCmdSet" id="cmdidMyCommand"   
      key1="C" mod1="CONTROL" mod2="ALT" editor="guidVSStd97" />  
</KeyBindings>  
. . .  
</CommandTable>  
```  
  
## <a name="example"></a>範例  
 此範例中將鍵盤快速鍵 CTL + B 繫結至名為的命令`cmdidBold`在專案中名為`TestEditor`。 使用只在自訂編輯器中，而不是在其他編輯器命令。  
  
```xml  
<KeyBinding guid="guidVSStd97" id="cmdidBold" editor="guidTestEditorEditorFactory" key1="B" mod1="Control" />  
```  
  
## <a name="see-also"></a>另請參閱  
 [擴充功能表和命令](../extensibility/extending-menus-and-commands.md)
