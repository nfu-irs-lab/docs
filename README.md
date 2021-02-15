# 上銀手臂相關文件及資源
## 目錄
* [程式素養及軟體工程](#程式素養及軟體工程)
  * [程式碼風格 Coding Style](#程式碼風格-Coding-Style)
  * [統一塑模語言 UML](#統一塑模語言-UML)
  * [SOLID 原則](#SOLID-原則)
  * [單元測試 Unit Testing](#單元測試-Unit-Testing)
  * [設計模式 Design Pattern](#設計模式-Design-Pattern)
* [工具](#工具)
  * [Git 版本控制](#Git-版本控制)
  * [Visual Studio 擴充插件](#Visual-Studio-擴充插件)
  * [Vim 文字編輯器](#Vim-文字編輯器)
* [版本號](#版本號)
  * [命名規則](#命名規則)
* [其它資源](#其它資源)
* [參考資料](#參考資料)

---

# 程式素養及軟體工程
## 程式碼風格 Coding Style
Coding Style 代表的是寫程式碼的格式風格，包含了縮排和命名規則等。

### 遵守格式
世界上有很多不同的 Coding Style，它們之間沒有絕對的好壞，只有一項唯一的準則：「同一個程式、專案與團隊應該遵守同一套 Coding Style，讓各程式碼的風格統一」。

```c
// 其中一種常見的 Coding Style: K&R
if (x == y) {
    printf("Hello World");
} else {
    printf("Goodbye World");
}

// 令一種常見的 Coding Style: Allman
if (x == y)
{
    printf("Hello World");
}
else
{
    printf("Goodbye World");
}
```

以 C# 來說，應該儘量遵守 Microsoft 官方所建議的 Coding Style。簡單歸納的話，縮排格式使用「Allman」，而變數和方法等的命名規則爲除了參數（Parameter）及區域變數（Local variable）使用小駝峰（Lower camel case）外，其它統統使用大駝峰（Upper camel case，又稱帕斯卡 Pascal case），在命名時儘量避免使用縮寫。而註解文字與註解符號間加入一個空白，並且以句號結尾，例如：`// 註解。`

```cs
// C# Coding Style 簡易範例。
public class ArmController
{
    public string IpAddress = "127.0.0.1";
    
    public string GoHome(double motorSpeed)
    {
        int errorCode;
        
        // Some code here.
        
        if ( errorCode > 0)
        {
            return "Error";
        }
        else if (errorCode == 0)
        {
            return "Done";
        }
        else
        {
            return "Unknown";
        }
    }
}
```

### 保持格式一致
現在有許多 IDE 都有自動格式化（Auto format）的功能，例如 Visual Studio 可以使用快捷鍵 <kbd>Ctrl</kbd>+<kbd>K</kbd>, <kbd>Ctrl</kbd>+<kbd>D</kbd> 來自動格式化整個檔案。另外也有像 [CodeMaid](https://marketplace.visualstudio.com/items?itemName=SteveCadwallader.CodeMaid) 這種擴充插件可以使用。

而 Visual Studio 也可以使用快捷鍵 <kbd>F2</kbd> 來快速重新命名變數和方法。

### 參考資料
* [C# 編碼慣例 (C# 程式設計手冊)](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
* [命名方針](https://docs.microsoft.com/zh-tw/dotnet/standard/design-guidelines/naming-guidelines)
* [大小寫慣例](https://docs.microsoft.com/zh-tw/dotnet/standard/design-guidelines/capitalization-conventions)
* [一般命名慣例](https://docs.microsoft.com/zh-tw/dotnet/standard/design-guidelines/general-naming-conventions)
* [WiKi 駝峰式大小寫](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB)

## 統一塑模語言 UML
UML 是一種規範語言，它定義了數種不同的圖示，以圖形化的方式來協助軟體工程相關事務。

### 類別圖
對於物件導向程式（OOP），UML 最常被使用的是類別圖（Class Diagram）。類別圖是用來表示一段 OOP 中各個類別（Class）的成員（Member），以及它和其它類別的關係。使用類別圖可以很清楚地看出這段程式碼的架構，進而對程式做更進一步的分析。

## SOLID 原則
「SOLID 原則」是物件導向程式（OOP）的 5 個基本原則，遵守這些原則的程式碼會更容易維護、擴充與修正。

### 簡介
|字母|代表|概念|
|:-:|-|-|
|S|單一職責 SRP|物件、函式和方法應該僅具有一種單一功能。|
|O|開放封閉 OCP|對於擴充是開放的，對於修改是封閉的。|
|L|里氏替換 LSP|程式中的物件應該可以在不改變程式正確性的前提下，被它的子類所替換。|
|I|介面隔離 ISP|多個特定客戶端介面要好過於一個廣泛用途的介面。|
|D|依賴反轉 DIP|高層模組不應該依賴於低層模組，兩者皆應該依賴於抽象介面。|

## 單元測試 Unit Testing
## 設計模式 Design Pattern

# 工具
## Git 版本控制
[Git](https://git-scm.com/) 是一個專門設計給程式碼使用的版本控制工具。

使用 Git 可以幫助你在編寫程式時更方便地控制程式碼的修改及變化，即使不小心改錯東西了，也可以輕鬆地恢復，並在不同的版本間切換。

### 基本知識
Git 的概念是它會自動偵測一個 Repository（程式庫，簡稱 Repo）內的檔案及內容變化。如果它發現有檔案或其內容改變了，就會將此檔案加到 Unstaged 區域。你可以在 Unstaged 區域中選擇數個檔案，再將其 Stage 到 Staged 區域。當有檔案在 Staged 區域時，你就可以爲它們加上一段訊息（Summary）並送出一個 Commit。一個 Commit 就如同一個版本節點，你可以在不同的 Commit 間切換。

有使用 Git 的話，如果你修改程式後發現改錯東西了，你就可以不用一直 <kbd>Ctrl</kbd>+<kbd>Z</kbd> Undo，而可以透過 Git 來恢復到上一個功能正常的 Commit。而且 Git 會記錄所有的變化，你可以很清楚地看到每個 Commit 修改了哪些檔案的哪些內容。例如本 Repository 的 [其中一個 Commit](../../commit/ba29bf709b1a244b9b951eb565e527679b602c5f?branch=ba29bf709b1a244b9b951eb565e527679b602c5f&diff=split)。

```diff
// Git 會記錄修改的內容。
// 此處展示了將「Hello!」改成「Hello! World!\n」的 Commit。
#include <stdio.h>

void main(void)
{
-    printf("Hello!");
+    printf("Hello! World!\n");
}
```

當你的工作告一段落，例如完成了一個功能或一天結束了，可能已經累積了好幾個 Commit，這時你可以將這些 Commit Push 到 Remote Repository（遠端程式庫，例如 GitHub），這樣你做的這些變更就會隨著你送出的 Commit 一起儲存在 Remote Repository。當 Remote Repository 上有變化時，例如其他人 Push 了一些 Commit，你可以從 Remote Repository 上 Pull 這些變化到你電腦上的 Local Repository。

爲了方便管理，通常在 GitHub 上每個 Repository 會設定 2 個基本的 Branch（分支），分別爲「main (或 master)」及「develop」。「main」代表的是此 Branch 上的所有 Commit 都是功能正常的，只有功能正常的 Commit 能夠 Merge 進「main」；而「develop」代表的是開發用的 Branch，要進行程式碼的修改、更新等，請在「develop」上進行。

正常情況下，GitHub 上的 Repository 應該對「main」進行保護設定，禁止也無法直接將 Commit Push 到「main」上，只能先 Push 到「develop」後，提出 Pull Requests 來讓該 Repository 的管理員查看並審核，當管理員覺得沒問題後才會接受該 Pull Requests，並將其 Merge 進「main」，以確保「main」上只有可正常運作的程式碼存在。

另外你可以爲一個特定的 Commit 加上 Tag（標籤），但通常此功能只會用來當作管理發行版（Release）用。

### 軟體工具
原始的 Git 只能使用指令（CLI）來操作，但現在也有很多圖形介面的 Git 軟體可以使用。以下列出一些比較常見的軟體：

* [Sourcetree](https://www.sourcetreeapp.com/)
* [GitKraken](https://www.gitkraken.com/)
* [GitHub Desktop](https://desktop.github.com/)
* [TortoiseGit](https://tortoisegit.org/)

此外，現在多數的 IDE 也有內建 Git 功能。例如 Visual Studio。

### 好的 Commit
一個好的 Commit 應該只包含了最小部分的變更，修改了一部分就送一次 Commit，而不是改了一大堆彼此沒太多關係的東西後才送一個 Commit。

而且好的 Commit 的 Summary 應該要可以清楚地表達此 Commit 究竟改了些什麼，而不是只有些籠統又不夠明確的訊息。不能清楚表達的 Summary 沒有意義。

| 好的 Summary                                                              | 不好的 Summary |
|---------------------------------------------------------------------------|----------------|
| 增加自動記錄 Log 的功能                                                   | 更新程式       |
| 增加處理 Log 檔案路徑時的例外處理，來修正目標路徑不存在時會中斷程式的 bug | 修 bug         |


### 移動檔案或重新命名
當一個檔案或資料夾在 Git 的控制下時，如果你想要移動它或對它重新命名，不應該直接透過檔案總管來做這些動作，而是應該使用 [`git mv`](https://git-scm.com/docs/git-mv) 指令來完成，否則 Git 會將移動或重新命名的檔案及資料夾視爲不同的全新檔案，進而遺失以往的所有 Commit 記錄。使用時可以搭配 `ls` 指令來查看目前工作路徑內的檔案及資料夾、使用 `cd` 指令來移動工作路徑。

* 例如你想將「Test.txt」移動到資料夾「Test」底下時，應該執行指令：`git mv Test.txt Test/`
* 或是你想將「Test.txt」重新命名成「Doc.txt」時，應該執行指令：`git mv Test.txt Doc.txt`

## Visual Studio 擴充插件
## Vim 文字編輯器

# 版本號
## 命名規則
以 `v主版本號.次版本號.修訂版本號` 來進行版本命名，例如:`v1.0.0`。

* 主版本號：有重大更新時遞增。例如介面大幅變更、相關 SDK 版本更新、會有大幅度兼容性問題的更新等。
* 次版本號：有部分功能或程式更新時遞增。例如新增或刪減部分功能。
* 修訂版本號：修正小部分功能或程式時遞增。例如修正 Bug。

主板本號爲 0 代表是測試時期版本。第一個測試時期版本號應該爲 `v0.1.0`，而第一個正式版本號應該爲 `v1.0.0`。

# 其它資源
* [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
* [提問的智慧](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way)

# 參考資料
1. 
