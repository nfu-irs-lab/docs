# 文件

**許多新手程式設計師（就像小學生一樣）並未特別遵守這樣的建議。**  
**他們認為寫程式的首要目標，是要讓程式能夠順利運作。**

—— Robert C. Martin《無瑕的程式碼》*p.223*

## 目錄
- [程式素養及軟體工程](#程式素養及軟體工程)
  - [程式碼風格 Coding Style](#程式碼風格-Coding-Style)
  - [統一塑模語言 UML](#統一塑模語言-UML)
  - [設計模式 Design Pattern](#設計模式-Design-Pattern)
  - [SOLID 原則](#SOLID-原則)
  - [複合優於繼承](#複合優於繼承)
  - [單元測試 Unit Testing](#單元測試-Unit-Testing)
  - [無瑕的程式碼 Clean Code](#無瑕的程式碼-Clean-Code)
- [工具](#工具)
  - [Git 版本控制](#Git-版本控制)
  - [GitHub](#GitHub)
  - [Git-Flow、GitHub-Flow](#Git-FlowGitHub-Flow)
  - [Visual Studio](#Visual-Studio)
- [發行](#發行)
  - [版本號命名規則](#版本號命名規則)
- [HIWIN](/others/hiwin.md#目錄)
- [C#](/others/csharp.md#目錄)
- [其它資源](#其它資源)

> 各章節後的參考資料基本上都是以筆者認為有幫助的程度、從高至低排序。

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
        
        if (errorCode > 0)
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
- [C# 編碼慣例 (C# 程式設計手冊)](https://docs.microsoft.com/zh-tw/dotnet/csharp/programming-guide/inside-a-program/coding-conventions)
- [命名方針](https://docs.microsoft.com/zh-tw/dotnet/standard/design-guidelines/naming-guidelines)
- [大小寫慣例](https://docs.microsoft.com/zh-tw/dotnet/standard/design-guidelines/capitalization-conventions)
- [一般命名慣例](https://docs.microsoft.com/zh-tw/dotnet/standard/design-guidelines/general-naming-conventions)
- [WiKi 駝峰式大小寫](https://zh.wikipedia.org/wiki/%E9%A7%9D%E5%B3%B0%E5%BC%8F%E5%A4%A7%E5%B0%8F%E5%AF%AB)

## 統一塑模語言 UML
UML 是一種規範語言，它定義了數種不同的圖示，以圖形化的方式來協助軟體工程相關事務。

### 類別圖
對於物件導向程式（OOP），UML 最常被使用的是類別圖（Class Diagram）。類別圖是用來表示一段 OOP 中各個類別（Class）的成員（Member），以及它和其它類別的關係。使用類別圖可以很清楚地看出這段程式碼的架構，進而對程式做更進一步的分析。

#### 關係
- 依賴（Dependency）
  - 關鍵字：uses a
  - 開口箭頭虛線。<----
- 關聯（Association）
  - 關鍵字：has a
  - 開口箭頭實線。<——
- 聚合（Aggregation）
  - 關鍵字：owns a
  - 空心菱形實線，菱形在母體（較大的）端。◇——
  - 概念：
    - 弱擁有。
    - 生命週期無關。
    - 互無部署關係的多個事物組成的***集合***。
  - 舉例：
    - 機場中的飛機。
    - 飛機可以飛離機場，機場也可以都沒飛機。機場被拆除的話飛機不用也跟著拆除，反之依然。
    - `機場` ◇—— `飛機`。
- 組合（Composition）
  - 關鍵字：is a part of
  - 實心菱形實線，菱形在母體（較大的）端。◆——
  - 概念：
    - 強擁有。
    - 生命週期有關。
    - 某個事物是另一事物的***一部分***。
  - 舉例：
    - 機場中的跑道。
    - 要拆除機場的話跑道也會一起拆除。
    - `機場` ◆—— `跑道`。
- 繼承（Inheritance）
  - 關鍵字：is a
  - 空心三角形實線。◁——
- 實作（Implementation / Realization）
  - 關鍵字：is like a
  - 空心三角形虛線。◁----

### 參考資料
- [[Design Pattern] UML基礎 - 類別圖 ~ Code Paradise](http://glj8989332.blogspot.com/2018/02/design-pattern-uml.html?m=1)
- [Dependency Inversion Implies Interfaces Are Owned by High-level Modules | Mikhail Shilkov](https://mikhail.io/2016/05/dependency-inversion-implies-interfaces-are-owned-by-high-level-modules/)
- [Inversion of Control Containers and the Dependency Injection pattern](https://www.martinfowler.com/articles/injection.html)
- [【UML】Class Diagram 類別圖 (下)：Relationships 關係 - SpicyBoyd 部落格](https://spicyboyd.blogspot.com/2018/07/umlclass-diagram-relationships.html)
- [UML類別圖：Aggregation vs. Composition | 自學程式誌](https://chenglearning.blogspot.com/2015/02/classrelationship.html#more)
- [軟體設計及架構---UML 入門](https://ithelp.ithome.com.tw/articles/10223499)


## 設計模式 Design Pattern
### 參考資料
- [我為什麼想學設計模式 ( Design Pattern )](https://ithelp.ithome.com.tw/articles/10201706)


## SOLID 原則
SOLID 原則是物件導向程式（OOP）的 5 個基本原則，遵守這些原則的程式碼會更容易維護、擴充與修正。

### 簡介
|字母|代表|概念|
|:-:|-|-|
|S|單一職責 SRP|物件、函式和方法應該僅具有一種單一功能。|
|O|開放封閉 OCP|對於擴充是開放的，對於修改是封閉的。|
|L|里氏替換 LSP|程式中的物件應該可以在不改變程式正確性的前提下，被它的子類所替換。|
|I|介面隔離 ISP|多個特定客戶端介面要好過於一個廣泛用途的介面。|
|D|依賴反轉 DIP|高層模組不應該依賴於低層模組，兩者皆應該依賴於抽象介面。|

個人認爲這 5 項原則的重要程度爲：
- 非常重要
  - S-單一職責
  - D-依賴反轉
- 重要
  - O-開放封閉
  - I-介面隔離
- 一般
  - L-里氏替換

如果程式不遵守「單一職責」原則的話，會很容易出現無法對此程式進行修改、擴充的情況，會缺乏很多的靈活度。而且這樣的程式往往也會非常的冗長、不易閱讀；不遵守「依賴反轉」原則的程式會在程式進行功能增減、API、SDK或硬體變更時容易出現問題，而且常常會是一連串的問題，因爲這樣的程式耦合性太高了，也會造成難以甚至是無法進行單元測試的情況。

遵守「開放封閉」的程式代表該程式碼在編寫前就已經設想好它整體的架構，在確保其有足夠多彈性下才進行真正的編寫，這樣的程式更利於擴充功能，而且新加入的功能不會對原本就有的功能造成問題；「介面隔離」是管理程式安全性的一種做法，爲不同的客戶端提供適合它的介面，避免它擁有不應屬於它的權限，也確保不會出現它所不想看到的功能，讓編寫時更方便。

「里氏替換」的概念基本是建築在類繼承，不過因爲現代 OOP 主要提倡「[偏好複合而非繼承](#複合優於繼承)」，因此會真正使用到繼承的情況應比較少。

### 依賴反轉

```cs
// 一般的寫法。

class Engine
{
    void Start()
    {
        // Some code here.
    }
}

class Car
{
    // 高層模組「Car」直接依賴於低層模組「Engine」。
    Engine MyEngine = new Engine();
    
    // Some code here.
}
```

```cs
// 依賴反轉的基本寫法。

interface EngineInterface
{
    void Start();
}

// 低層模組「Engine」繼承並實作了介面「EngineInterface」。
class Engine : EngineInterface
{
    void Start()
    {
        // Some code here.
    }
}

class Car
{
    // 高層模組「Car」不直接依賴於低層模組「Engine」，而是依賴於介面「EngineInterface」。
    EngineInterface MyEngine = new Engine();
    
    // Some code here.
}
```


```cs
// 依賴反轉的進階寫法。

interface EngineInterface
{
    void Start();
}

class Engine : EngineInterface
{
    void Start()
    {
        // Some code here.
    }
}

class Car
{
    EngineInterface MyEngine = null;
    
    // 使用依賴注入（Dependency Injection，DI）的方式實現控制反轉（Inversion of Control，IoC）。
    // 將低層模組「Engine」在高層模組「Car」之外實例化後，才透過建構子傳入「Car」。
    Car(EngineInterface engine)
    {
        MyEngine = engine;
    }
    
    // Some code here.
}

// 實際呼叫「Car」時：
Engine V8Engine = new Engine();
Car MySuperCar = new Car(V8Engine);
```
### 參考資料
- 無瑕的程式碼（Robert C. Martin, Clean Code）
- [我該學會SOLID嗎?](https://medium.com/@f40507777/%E6%88%91%E8%A9%B2%E5%AD%B8%E6%9C%83solid%E5%97%8E-4e73887c9156)
- [物件導向設計原則—SOLID](https://ithelp.ithome.com.tw/articles/10191553)
- [使人瘋狂的 SOLID 原則：目錄](https://medium.com/%E7%A8%8B%E5%BC%8F%E6%84%9B%E5%A5%BD%E8%80%85/%E4%BD%BF%E4%BA%BA%E7%98%8B%E7%8B%82%E7%9A%84-solid-%E5%8E%9F%E5%89%87-%E7%9B%AE%E9%8C%84-b33fdfc983ca)
- [物件導向程式設計基本原則 - SOLID](https://skyyen999.gitbooks.io/-study-design-pattern-in-java/content/oodPrinciple.html)

## 複合優於繼承
Favor composition over inheritance.

### 概念與理由

假設今天有個夾爪控制器，它需要透過 Serial Port 來進行通訊。這時我們有 2 種選擇：
- 繼承（Inheritance）：夾爪控制器「是一個」Serial Port 裝置。
- 複合（Composition）：夾爪控制器「有一個」Serial Port 裝置。

這樣看起來好像沒什麼差別，但實際上「繼承」的做法會降低其彈性。例如今天有一個裝置，它需要同時使用 2 個 Serial Port，這時如果使用「繼承」的話就會變成非常麻煩、難以達成；但如果是用「複合」的話，就只要再多宣告一個 Serial Port 就可以了。

```cs
// 使用繼承的方式。難以達成 2 個 Serial Port 的需求。
class Device : SerialPort
{
}

// 使用複合的方式。
class Device
{
    SerialPort SerialPortA = new SerialPort();
    SerialPort SerialPortB = new SerialPort();
}
```

### 參考資料
- [物件導向程式設計：為何說composition優於inheritance？](https://tw.twincl.com/programming/-662v)
- [Why composition is often better than inheritance](http://joostdevblog.blogspot.com/2014/07/why-composition-is-often-better-than.html)

## 單元測試 Unit Testing
單元測試指的是一種自動化的程式，專門用來對另一個目標程式進行測試，以驗證目標程式的運作與邏輯是否正常。

### 基本概念

單元測試的概念其實很簡單，甚至大部分的人都有寫過類似的程式。例如以下有一個數學加分的程式，他會將兩個參數相加後回傳。
```cs
// File name: Math.cs
class Math
{
    int Add(int a, int b)
    {
        return (a + b);
    }
}
```

對於上面這個程式，我們如果想要用程式來測試它的功能是否正常，我們可以編寫以下程式：
```cs
// File name: MathTest.cs
class MathTest
{
    void Add_Input1And2_Return3()
    {
        // Arrange.
        Math math = new Math();
        
        int firstNumber = 1;
        int secondNumber = 2;
        
        int expected = 3;
        int actual;
        
        // Act.
        actual = math.Add(firstNumber, secondNumber);
        
        // Assert.
        Assert.AreEqual(expected, actual);
    }
}
```

上面這個「MathTest.cs」就可以視爲一個簡單的單元測試程式。可以注意它使用了「3A（Arrange-Act-Assert，準備-操作-驗證）」的結構，這樣做的好處是很方便瞭解該單元測試程式的運作方式。而該測試方法的命名使用了「目標被測方法_假設條件_預期行爲」的結構。

### 參考資料
- [Unit Testing 簡介](https://ithelp.ithome.com.tw/articles/10102264)
- 單元測試的藝術 第二版（Roy Osherove, The Art of Unit Testing: with wxamples in C#, 2nd Edition）
- [單元測試的藝術-讀後整理](https://sunxiaoshan.medium.com/%E5%96%AE%E5%85%83%E6%B8%AC%E8%A9%A6%E7%9A%84%E8%97%9D%E8%A1%93-%E8%AE%80%E5%BE%8C%E6%95%B4%E7%90%86-ba2a4d3491c5)
- [《單元測試的藝術》學習筆記](https://zh-tw.coderbridge.com/series/89e2405766bc423b965adcdd4af244a0)

## 無瑕的程式碼 Clean Code
> 你因為兩個原因來讀這本書：  
> 首先，你是位程式設計師。再者，你想成為一位更好的程式設計師。  
> 非常好，我們需要更好的程式設計師。  
> 
> —— Robert C. Martin《無瑕的程式碼》

### 參考資料
- [Clean Code 無瑕的程式碼 | 閱讀筆記. Uncle… | by Airwaves | 手寫筆記 | Medium](https://medium.com/%E6%89%8B%E5%AF%AB%E7%AD%86%E8%A8%98/clean-code-index-51e209cc47db)

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

另外你可以爲一個特定的 Commit 加上 Tag（標籤），但通常此功能只會用來當作管理發行版（Release）用。

而 Branch（分支）的用法請見 [Git-Flow、GitHub-Flow](#Git-FlowGitHub-Flow)。

### 軟體工具
原始的 Git 只能使用指令（CLI）來操作，但現在也有很多圖形介面的 Git 軟體可以使用。以下列出一些比較常見的軟體：

- [Sourcetree](https://www.sourcetreeapp.com/)
- [GitKraken](https://www.gitkraken.com/)
- [GitHub Desktop](https://desktop.github.com/)
- [TortoiseGit](https://tortoisegit.org/)

此外，現在多數的 IDE 也有內建 Git 功能。例如 Visual Studio。

### 好的 Commit
一個好的 Commit 應該只包含了最小部分的變更，修改了一部分就送一次 Commit，而不是改了一大堆彼此沒太多關係的東西後才送一個 Commit。

而且好的 Commit 的 Summary 應該要可以清楚地表達此 Commit 究竟改了些什麼，而不是只有些籠統又不夠明確的訊息。不能清楚表達的 Summary 沒有意義。

| 好的 Summary                                                         | 不好的 Summary |
|---------------------------------------------------------------------|----------------|
| 增加自動記錄 Log 的功能                                               | 更新程式       |
| 增加處理 Log 檔案路徑時的例外處理，來修正目標路徑不存在時會中斷程式的 bug | 修 bug         |


### 移動檔案或重新命名
當一個檔案或資料夾在 Git 的控制下時，如果你想要移動它或對它重新命名，不應該直接透過檔案總管來做這些動作，而是應該使用 [`git mv`](https://git-scm.com/docs/git-mv) 指令來完成，否則 Git 會將移動或重新命名的檔案及資料夾視爲不同的全新檔案，進而遺失以往的所有 Commit 記錄。使用時可以搭配 `ls` 指令來查看目前工作路徑內的檔案及資料夾、使用 `cd` 指令來移動工作路徑。

- 例如你想將「Test.txt」移動到資料夾「Test」底下時，應該執行指令：`git mv Test.txt Test/`
- 或是你想將「Test.txt」重新命名成「Doc.txt」時，應該執行指令：`git mv Test.txt Doc.txt`

### 參考資料
- [Pro Git, 繁體中文第 2 版（免費書籍）](https://taichunmin.gitlab.io/progit2-zh-tw/)
- [為你自己學 Git！](https://gitbook.tw/chapters/introduction/about-this-book.html)
- [什麼是 Git？為什麼要學習它？](https://gitbook.tw/chapters/introduction/what-is-git.html)

## GitHub
### Repository
GitHub 上 Repository 的空間容量是有上限的，而且它本來就是針對儲存程式碼而設計的，因此容量不大，所以應該仔細地審視什麼檔案該或不該上傳到 GitHub。

例如以下舉例的檔案基本上***不應該***上傳到 GitHub，請善用「.gitignore」來忽略它們。
- 程式編譯而自動產生的中間檔、執行檔。
- 暫存檔。
- Log 檔。
- 非於程式緊緊相關的圖片、影片或 PDF 等類似的大型檔案。
- 含有個資或敏感資料的內容。

對於 Visual Studio 的相關程式，可以透過 Visual Studio 內建的 Git 功能來自動產生設定好的「.gitignore」，或是使用 GitHub 官方提供的樣板[ github/gitignore ](https://github.com/github/gitignore/blob/master/VisualStudio.gitignore)。

## Git-Flow、GitHub-Flow
Git-Flow 與 GitHub-Flow 都是一種 Workflow（工作流程）。對於實驗室來說，筆者個人比較推薦使用 GitHub-Flow。

### 參考資料
- [Git 版本控制系統 - GitHub Flow 工作流程與實際演練 | Roya's Blog](https://awdr74100.github.io/2020-05-11-git-githubflow/)
- [三種版控流程. git flow vs github flow vs gitlab flow | by 沈一二 | Medium](https://medium.com/@lf2lf2111/%E4%B8%89%E7%A8%AE%E7%89%88%E6%8E%A7%E6%B5%81%E7%A8%8B-29c82f5d4469)
- [讓我們來了解 GitHub Flow 吧！. 除了會 Git 你還需要 Work Flow。 | by MrGG（CHANG, TZU-YEN - 張子晏） | Medium](https://medium.com/@trylovetom/%E8%AE%93%E6%88%91%E5%80%91%E4%BE%86%E4%BA%86%E8%A7%A3-github-flow-%E5%90%A7-4144caf1f1bf)
- [GitHub Flow 及 Git Flow 流程使用時機 | 小惡魔 - 電腦技術 - 工作筆記 - AppleBOY](https://blog.wu-boy.com/2017/12/github-flow-vs-git-flow/)

## Visual Studio
### 快捷功能
- [重構 | Microsoft Docs](https://docs.microsoft.com/zh-tw/previous-versions/visualstudio/visual-studio-2008/719exd8s(v=vs.90))

# 發行
## 版本號命名規則
以 `v主版本號.次版本號.修訂版本號` 來進行版本命名，例如:`v1.0.0`。

- 主版本號：有重大更新時遞增。例如介面大幅變更、相關 SDK 版本更新、會有大幅度兼容性問題的更新等。
- 次版本號：有部分功能或程式更新時遞增。例如新增或刪減部分功能。
- 修訂版本號：修正小部分功能或程式時遞增。例如修正 Bug。

主板本號爲 0 代表是測試時期版本。第一個測試時期版本號應該爲 `v0.1.0`，而第一個正式版本號應該爲 `v1.0.0`。

## 參考資料
- [語意化版本 2.0.0 | Semantic Versioning](https://semver.org/lang/zh-TW/)

# 其它資源
- [提問的智慧](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way)
- [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
