---
title: JavaScript 主控台命令 |Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- JavaScript Console commands [Windows Store apps]
- JavaScript debugging, console [Windows Store apps]
- debugging JavaScript, console [Windows Store apps]
ms.assetid: 359e2b24-6bb7-48e7-8b55-b570df0cb774
caps.latest.revision: 50
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: aeaba355e101bd8e48126bfa01f95668a37abe3e
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "60081420"
---
# <a name="javascript-console-commands"></a>JavaScript Console commands
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

適用於 Windows 和 Windows Phone] (../Image/windows_and_phone_content.png"windows_and_phone_content")  
  
 您可以在 Visual Studio [JavaScript 主控台] 視窗中，使用命令傳送訊息及執行其他工作。 如需示範如何使用該視窗的範例，請參閱[快速入門：偵錯 JavaScript](../debugger/quickstart-debug-javascript-using-the-console.md)。 本主題資訊適用於 Windows 市集應用程式、Windows Phone 市集應用程式和使用 Visual Studio Tools for Apache Cordova 建立的應用程式。 如需 Cordova 應用程式支援的主控台命令相關資訊，請參閱 [Debug Your App](http://msdn.microsoft.com/library/c2a4a1d4-a4e8-47ec-811f-ad207c54f4d1)。 如需在 Internet Explorer F12 工具中使用主控台的詳細資訊，請參閱 [本主題](http://msdn.microsoft.com/library/ie/dn255006.aspx)。  
  
 如果 [JavaScript 主控台] 視窗已關閉，您可以開啟偵錯時在 Visual Studio 中選擇**偵錯** > **Windows** > **JavaScript主控台**。  
  
> [!NOTE]
>  如果在偵錯工作階段期間無法使用該視窗，請確定在專案的 [偵錯] 屬性中的偵錯工具類型已設為 [指令碼]  。  
  
## <a name="console-object-commands"></a>主控台物件命令  
 此表格顯示 `console` 物件命令的語法，該命令可用於 [JavaScript 主控台] 視窗，也可以用來從程式碼傳送訊息至主控台。 此物件提供數種格式，以便您在必要時可區分告知性訊息與錯誤訊息。  
  
 如需避免與本機物件命名的主控台相混淆，您可以使用較長的命令格式 `window.console.[command]` 。  
  
> [!TIP]
>  舊版的 Visual Studio 不支援完整的命令集。 請使用主控台物件中的 IntelliSense，取得支援命令的快速資訊。  
  
|命令|描述|範例|  
|-------------|-----------------|-------------|  
|`assert(expression, message)`|如果 `expression` 評估為 **false**，則會傳送訊息。|`console.assert((x == 1), "assert message: x != 1");`|  
|`clear()`|清除主控台視窗中的訊息 (包括指令碼錯誤訊息) 和顯示的指令碼， 但是不會清除您在主控台輸入提示中輸入的指令碼。|`console.clear();`|  
|`count(title)`|將 count 命令呼叫的次數傳送至主控台視窗。 count 的每一個呼叫是由選擇性 `title`所唯一識別。<br /><br /> 主控台視窗中的現有項目是由 `title` 參數 (如果有的話) 所識別並由 count 命令更新。 不會建立新的項目。|`console.count();`<br /><br /> `console.count("inner loop");`|  
|`debug(message)`|將 `message` 傳送至主控台視窗。<br /><br /> 這個命令與 console.log 相同。<br /><br /> 使用這個命令傳遞的物件，會轉換為字串值。|`console.debug("logging message");`|  
|`dir(object)`|將指定的物件傳送至主控台視窗，並在視覺化檢視中顯示物件。 您可以使用視覺化檢視在主控台視窗中檢查屬性。|`console.dir(obj);`|  
|`dirxml(object)`|將指定的 XML 節點 `object` 傳送至主控台視窗，並將它顯示為 XML 節點樹狀結構。|`console.dirxaml(xmlNode);`|  
|`error(message)`|將 `message` 傳送至主控台視窗。 訊息文字是紅色的，且開頭處會有錯誤符號。<br /><br /> 使用這個命令傳遞的物件，會轉換為字串值。|`console.error("error message");`|  
|`group(title)`|開始群組傳送至主控台視窗的訊息，並傳送選擇性 `title` 當做群組標籤。 群組可以是巢狀並且顯示在主控台視窗的樹狀檢視。<br /><br /> 在某些情況下 group* 命令可讓您更方便檢視主控台視窗輸出，例如當元件模型正在使用中時。|`console.group("Level 2 Header");` <br /> `console.log("Level 2");` <br /> `console.group();` <br /> `console.log("Level 3");` <br /> `console.warn("More of level 3");` <br /> `console.groupEnd();` <br /> `console.log("Back to level 2");` <br /> `console.groupEnd();` <br /> `console.debug("Back to the outer level");`|  
|`groupCollapsed(title)`|開始群組傳送至主控台視窗的訊息，並傳送選擇性 `title` 當做群組標籤。 使用 `groupCollapsed` 傳送的群組，預設會出現在摺疊的檢視中。 群組可以是巢狀並且顯示在主控台視窗的樹狀檢視。|用法與 `group` 命令相同。<br /><br /> 請參閱 `group` 命令的範例。|  
|`groupEnd()`|結束目前的群組。<br /><br /> 需求：<br /><br /> Visual Studio 2013|請參閱 `group` 命令的範例。|  
|`info(message)`|將 `message` 傳送至主控台視窗。 訊息開頭處會有資訊符號。|`console.info("info message");`<br /><br /> 如需更多範例，請參閱本主題稍後的 [Formatting console.log output](#ConsoleLog) 。|  
|`log(message)`|將 `message` 傳送至主控台視窗。<br /><br /> 如果您傳遞物件，這個命令會將該物件傳送至主控台視窗，並在視覺化檢視中顯示物件。 您可以使用視覺化檢視在主控台視窗中檢查屬性。|`console.log("logging message");`|  
|`msIsIndependentlyComposed(element)`|使用於 Web 應用程式。 不支援使用 JavaScript 的市集應用程式。|不支援。|  
|`profile(reportName)`|使用於 Web 應用程式。 不支援使用 JavaScript 的市集應用程式。|不支援。|  
|`profileEnd()`|使用於 Web 應用程式。 不支援使用 JavaScript 的市集應用程式。|不支援。|  
|`select(element)`|選取 `element` DOM 總管 [中指定的 HTML](../debugger/quickstart-debug-html-and-css.md)。|console.select(element);|  
|`time (name)`|啟動由選擇性 `name` 參數識別的計時器。 與 `console.timeEnd`搭配使用時，計算 `time` 與 `timeEnd`之間經過的時間，並使用 `name` 字串做為前置詞，將結果 (以毫秒為單位) 傳送至主控台。 用來啟用應用程式程式碼的檢測以測量效能。|`console.time("app start");  app.start();  console.timeEnd("app start");`|  
|`timeEnd(name)`|停止由選擇性 `name` 參數識別的計時器。 請參閱 `time` 主控台命令。|`console.time("app start"); app.start(); console.timeEnd("app start");`|  
|`trace()`|將堆疊追蹤傳送至主控台視窗。 追蹤包括完整的呼叫堆疊和資訊，例如檔案名稱、行號和欄號。|`console.trace();`|  
|`warn(message)`|將 `message` 傳送至主控台視窗 (開頭處會有警告符號)。<br /><br /> 使用這個命令傳遞的物件，會轉換為字串值。|`console.warn("warning message");`|  
  
## <a name="miscellaneous-commands"></a>其他命令  
 在 [JavaScript 主控台] 視窗中也可以使用這些命令 (程式碼不提供)。  
  
|命令|描述|範例|  
|-------------|-----------------|-------------|  
|`$0`, `$1`, `$2`, `$3`, `$4`|將指定的項目傳回主控台視窗。 `$0` 會傳回目前在 [DOM 總管] 中選取的項目，`$1` 則會傳回前次在 [DOM 總管] 中選取的項目，依此類推，最多可回推至前四次選取的項目。|$3|  
|`$(id)`|依 ID 傳回項目。 這是 `document.getElementById(id)`的捷徑命令，其中 `id` 是代表項目 ID 的字串。|`$("contenthost")`|  
|`$$(selector)`|傳回項目陣列，其符合使用 CSS 選取器語法的指定選取器。 這是 `document.querySelectorAll()`的捷徑命令。|`$$(".itemlist")`|  
|`cd()`<br /><br /> `cd(window)`|可讓您將運算式評估的內容，從頁面的預設最上層視窗變更為指定框架的視窗。 呼叫不帶參數的 `cd()` ，會將內容傳回至最上層視窗。|`cd();`<br /><br /> `cd(myframe);`|  
|`select(element)`|選取 [DOM 總管](../debugger/quickstart-debug-html-and-css.md)中指定的項目。|`select(document.getElementById("element"));`<br /><br /> `select($("element"));`<br /><br /> `select($1);`|  
|`dir(object)`|傳回指定物件的視覺化檢視。 您可以使用視覺化檢視在主控台視窗中檢查屬性。|`dir(obj);`|  
  
## <a name="checking-whether-a-console-command-exists"></a>檢查主控台命令是否存在  
 您可以在嘗試使用之前檢查特定命令是否存在。 這個範例會檢查 `console.log` 命令的存在。 如果 `console.log` 存在，程式碼會呼叫它。  
  
```javascript  
if (console && console.log) {  
    console.log("msg");  
}  
  
```  
  
## <a name="examining-objects-in-the-javascript-console-window"></a>檢查 JavaScript 主控台視窗中的物件  
 當您使用 JavaScript 主控台視窗時，可以與範圍內的任何物件互動。 若要在主控台視窗中檢查超出範圍的物件，請從您的程式碼使用 `console.log` 、 `console.dir`或其他命令。 或者，當物件在範圍內時，可以在程式碼中設定中斷點 ([中斷點] > **Insert**)，即可從主控台視窗與物件互動。  
  
## <a name="ConsoleLog"></a> 格式化 console.log 輸出  
 如果您將多個引數傳遞至 `console.log`，主控台會將這些引數視為陣列處理並串連輸出。  
  
```javascript  
var user = new Object();  
user.first = "Fred";  
user.last = "Smith";  
  
console.log(user.first, user.last);  
// Output:  
// Fred Smith  
  
```  
  
 `console.log` 也支援以模式 "printf" 替代格式輸出。 如果您在第一個引數中使用替代模式，其他的引數會用來按照指定模式所使用的順序來取代它們。  
  
 支援的替代模式如下：  
  
- %s - 字串  
   %i - 整數  
   %d - 整數  
   %f - 浮點數  
   %o - 物件  
   %b - 二進位  
   %x - 十六進位  
   %e - 指數  
  
  以下是在 `console.log`中使用替代模式的一些範例：  
  
```javascript  
var user = new Object();  
user.first = "Fred";  
user.last = "Smith";  
user.age = 10.01;  
console.log("Hi, %s %s!", user.first, user.last);  
console.log("%s is %i years old!", user.first, user.age);  
console.log("%s is %f years old!", user.first, user.age);  
  
// Output:  
// Hi, Fred Smith!  
// Fred is 10 years old!  
// Fred is 10.01 years old!  
```  
  
## <a name="see-also"></a>另請參閱  
 [快速入門：對 JavaScript 進行偵錯](../debugger/quickstart-debug-javascript-using-the-console.md)   
 [快速入門：對 HTML 和 CSS 進行偵錯](../debugger/quickstart-debug-html-and-css.md)
