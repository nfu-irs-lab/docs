# HIWIN
## 目錄
> [回到主頁](../README.md#目錄)

- [工作流程 Workflow](#工作流程-workflow)
- [相關 Repository 列表](#相關-Repository-列表)

---
# 工作流程 Workflow
工作流程大致上與 GitHub-Flow 一樣，請先去瞭解其運作，並善用 [nfu-irs-lab/test](https://github.com/nfu-irs-lab/test) 進行練習。

在此每個 repo 會有兩個 Branch：`main` 和 `develop`。其中 `develop` Branch 的功能就是 GitHub-Flow 中的 `main` 或 `master` Branch，而我們真正的 `main` Branch 只作為發行用，只由管理員負責管理，一般人不需要也不允許操作組織上的 `main` Branch（除了 Pull）。

## 一般人
### 首次使用
1. 登入網頁版 GitHub。
2. 進入目標的「組織 Remote repo」，點選「fork」按鈕，將其 fork 進自己的 GitHub 帳號，它會變成「個人 Remote repo」。
3. 將「個人 Remote repo」Clone 到個人電腦上。此時電腦上的就是「個人 Local repo」。
4. 將「組織 Remote repo」添加到「個人 Local repo」作為新的 Remote repo。
5. 確認此時的「個人 Local repo」應該有 2 個 Remote repo，分別為：「個人 Remote repo (origin)」和「組織 Remote repo」。
6. 完成。

### 一般作業
1. 確定好本次的作業目標。
2. 在「個人 Local repo」上從 `develop` Branch 中開啟一個新 Branch，並命名為：`feature/TARGET_NAME`，其中 `TARGET_NAME` 是本次目標要做的事情。
3. 確認已經 Checkout 到剛剛新開的 `feature/TARGET_NAME` Branch 上。
4. 在 `feature/TARGET_NAME` Branch 上進行作業、送 Commit。
5. 當本次目標要做的事都已經完成、Commit 都送好了後，Checkout 到「個人 Local repo」上的 `develop` Branch。
6. Pull「組織 Remote repo」上的 `develop` Branch 到「個人 Local repo」上的 `develop` Branch。此步驟是為了避免你在 `feature/TARGET_NAME` Branch 上進行作業時，有其它人 Push 到「組織 Remote repo」上，因不同步而造成的衝突。
7. 將「個人 Local repo」上的 `feature/TARGET_NAME` Branch Merge 進「個人 Local repo」上的 `develop` Branch。
8. 若上一步驟有衝突而無法進行 Merge，與團隊進行溝通並解決衝突，直到完成 Merge。
9. 將「個人 Local repo」上的 `develop` Branch Push 到「個人 Remote repo」上的 `develop` Branch。
10. 發起 Pull request。方向為「*base:* 組織 Remote repo/develop 」←「*compare:* 個人 Remote repo/develop」。
11. 與團隊進行溝通，等待發起的 Pull request 被管理員接受並 Merge。若有需要，請更新該 Pull request 以符合管理員和團隊的要求。
12. 若該 Pull request 已經被接受並 Merge，將「組織 Remote repo」上的 `develop` Branch Pull 到「個人 Local repo」上從 `develop` Branch。
13. 為了保持整潔，可以刪除「個人 Local repo」上的 `feature/TARGET_NAME` Branch，因為它的工作已經結束了。
14. 本次作業完成。

[![圖解一般作業流程](../figs/實驗室Git工作流程_1.svg)](../figs/實驗室Git工作流程_1.svg)

## 管理員


# 相關 Repository 列表
- 其它
  - 基本共用程式：[hiwinrobot](https://github.com/nfu-irs-lab/hiwinrobot)
  - 手機控制程式：[hiwinrobot-controller-app](https://github.com/nfu-irs-lab/hiwinrobot-controller-app)
  - 舊範例程式（不建議）：[hiwinrobot-old-example](https://github.com/nfu-irs-lab/hiwinrobot-old-example/tree/master)
  - XEG 夾爪範例程式：[hiwin-xeg-gripper-example](https://github.com/nfu-irs-lab/hiwin-xeg-gripper-example)
- 14屆 `2021`
  - 智慧撞球：none
  - 智慧拼圖：none
  - 智慧創作：none
- 13屆 `2020`
  - 智慧撞球：[hiwinrobot-13-billiards](https://github.com/nfu-irs-lab/hiwinrobot-13-billiards)
  - 智慧拼圖：[hiwinrobot-13-puzzle](https://github.com/nfu-irs-lab/hiwinrobot-13-puzzle)
  - 智慧分類：[hiwinrobot-13-classification](https://github.com/nfu-irs-lab/hiwinrobot-13-classification)
- 12屆 `2019`
  - 智慧撞球：[hiwinrobot-12-billiards](https://github.com/nfu-irs-lab/hiwinrobot-12-billiards)
  - 智慧搖飲：[hiwinrobot-12-shake-drink](https://github.com/nfu-irs-lab/hiwinrobot-12-shake-drink)
  - 智慧分類：[hiwinrobot-12-classification](https://github.com/nfu-irs-lab/hiwinrobot-12-classification)
- 11屆 `2018`
  - 智慧堆疊：[hiwinrobot-11-stacked](https://github.com/nfu-irs-lab/hiwinrobot-11-stacked)
  - 智慧分類：[hiwinrobot-11-classification](https://github.com/nfu-irs-lab/hiwinrobot-11-classification)
  - 機械揮毫：[hiwinrobot-11-brush](https://github.com/nfu-irs-lab/hiwinrobot-11-brush)
  - 智慧澆注：[hiwinrobot-11-pouring](https://github.com/nfu-irs-lab/hiwinrobot-11-pouring)
- 10屆 `2017`
  - 智慧堆疊：[hiwinrobot-10-stacked](https://github.com/nfu-irs-lab/hiwinrobot-10-stacked)
  - 機械揮毫：[hiwinrobot-10-brush](https://github.com/nfu-irs-lab/hiwinrobot-10-brush)
  - 眼明手快：[hiwinrobot-10-sharp-eyes](https://github.com/nfu-irs-lab/hiwinrobot-10-sharp-eyes)
  - 智慧裝配：[hiwinrobot-10-assembly](https://github.com/nfu-irs-lab/hiwinrobot-10-assembly)
