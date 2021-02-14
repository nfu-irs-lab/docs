# 上銀手臂相關文件及資源
## 目錄
* [程式素養及軟體工程](#程式素養及軟體工程)
  * [程式碼風格 Coding Style](#程式碼風格-Coding-Style)
  * [統一塑模語言 UML](#統一塑模語言-UML)
  * [SOLID 原則](#SOLID-原則)
  * [單元測試 Unit Testing](#單元測試-Unit-Testing)
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
## 統一塑模語言 UML
## SOLID 原則
## 單元測試 Unit Testing

# 工具
## Git 版本控制
[Git](https://git-scm.com/) 是一個專門設計給程式碼使用的版本控制工具。

使用 Git 可以幫助你在編寫大型程式時更方便控制程式碼的修改及變化，即使不小心改錯東西了，也可以輕鬆地恢復，並在不同的版本間切換。

Git 的基本概念是，它會自動偵測一個 Repository （程式庫，簡稱 Repo）內的檔案及內容變化。如果它發現有檔案或其內容改變了，它就會將此改變的檔案加到 Unstaged 區域。你可以在 Unstaged 區域中選擇數個檔案，再將其 Stage 到 Staged 區域。當有檔案在 Staged 區域時，你就可以爲它們加上一段訊息（Summary）並送出一個 Commit。一個 Commit 就如同一個版本節點，你可以在不同的 Commit 間切換。

有使用 Git 的話，如果你修改程式後發現改錯東西了，你就可以不用一直 <kbd>Ctrl</kbd>+<kbd>Z</kbd> Undo，而可以透過 Git 來恢復到上一個功能正常的 Commit。而且 Git 會記錄所有的變化，你可以很清楚地看到每個 Commit 修改了哪些檔案的哪些內容。

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

當你的工作告一段落，例如完成了一個功能或一天結束了，你可能已經累積了好幾個 Commit，這時你可以將這些 Commit Push 到 Remote Repository（遠端程式庫，例如 GitHub），這樣你做的這些變更就會隨著你送出的 Commit 一起儲存在 Remote Repository。當 Remote Repository 上有變化時，例如其他人 Push 了一些 Commit，你可以從 Remote Repository 上 Pull 這些變化到你電腦上的 Local Repository。

爲了方便管理，通常在 GitHub 上每個 Repository 會設定 2 個基本的 Branch（分支），分別爲「main (或 master)」及「develop」。「main」代表的是此 Branch 上的所有 Commit 都是功能正常的，只有功能正常的 Commit 能夠 Merge 進「main」；而「develop」代表的是開發用的 Branch，要進行程式碼的修改、更新等，請在「develop」上進行。

正常情況下，GitHub 上的 Repository 應該對「main」進行保護設定，禁止也無法直接將 Commit Push 到「main」上，只能先 Push 到「develop」後，提出 Pull Requests 來讓該 Repository 的管理員查看並審核，當管理員覺得沒問題後才會接受該 Pull Requests，並將其 Merge 進「main」，以確保「main」上只用可正常運作的程式碼存在。

另外你可以爲一個特定的 Commit 加上 Tag（標籤），通常此功能只會用來當作管理發行版（Release）用。

## Visual Studio 擴充插件
## Vim 文字編輯器

# 版本號
## 命名規則
以 `v主版本號.次版本號.修訂版本號` 來進行版本命名，例如:`v1.0.0`。

* 主版本號：有重大更新時遞增。例如介面大幅變更、相關 SDK 版本更新、會有大幅度兼容性問題的更新等。
* 次版本號：有部分功能或程式更新時遞增。例如新增或刪減部分功能。
* 修訂版本號：修正小部分功能或程式時遞增。例如修正 Bug。

# 其它資源
* [中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)
* [提問的智慧](https://github.com/ryanhanwu/How-To-Ask-Questions-The-Smart-Way)

# 參考資料
1. 
