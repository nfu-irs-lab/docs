# HIWIN
## 目錄
- [上銀機械手臂使用指南](#上銀機械手臂使用指南)
  - [各裝置名稱](#各裝置名稱)
  - [開機與關機](#開機與關機)
  - [連線](#連線)
  - [以教導器控制](#以教導器控制)
- [工作流程 Workflow](#工作流程-workflow)
- [相關 Repository 列表](#相關-Repository-列表)

> [回到主頁面](../README.md#文件)

---

# 上銀機械手臂使用指南
## 各裝置名稱
|名稱|型號|圖片|
|-|-|-|
|關節式機器手臂（以下稱「手臂」）|RT605-710-GB|![](https://1.bp.blogspot.com/-1vYJ_BSNFzQ/YEIEqnIb9aI/AAAAAAAAAGA/-NLk58wh78cxh2eY7B2UNUohCVvJ6sTcACPcBGAsYHg/s150/rt605_710_gb_b.jpg)|
|機器手臂控制器（以下稱「控制箱」）|RTC605-710-GB|![](https://1.bp.blogspot.com/-HIKC_lc6gnI/YEIEqmm7bDI/AAAAAAAAAGA/PapbPf9fExUv0VzsgyaqdmYYGZbJH_1-wCPcBGAsYHg/s150/RCT605-710-GB.jpg)|
|教導器|TP02|![](https://1.bp.blogspot.com/-z7rLn2X9myo/YEIEqiwpunI/AAAAAAAAAGA/9u8uI128UqY6lS7uWiopcmPQdKu9NojkgCPcBGAsYHg/s150/HIWIN-TP02.png)|

## 開機與關機
|步驟|說明|圖片|
|:-:|:-|:-:|
|1|將控制箱的電源開關向上扳動至「1」，即可進行開機。||
|2|等待教導器顯示控制畫面，即完成開機。||
|3|點擊教導器 `主選單（左上角手臂圖樣） > shutdown（關機）`，即可進行關機。進行此步驟前請先確認手臂已經停止動作。||
|4|等待控制箱的運作聲停止後***等待至少 5 秒***，才可以將控制箱的電源開關向下扳動至「0」，完成關機。||
|5|關閉電源完成關機後，若想要重新開機，需在完成關機後***等待至少 30 秒***，才可以再次開機。||

## 連線
|步驟|說明|圖片|
|:-:|:-|:-:|
|1|使用 RJ-45 網路線連接電腦主機與控制箱。控制箱有兩個 RJ-45 網路孔，應先嘗試 LAN 2（上面的），並確認燈號。|![](https://1.bp.blogspot.com/-elOivsHWe7U/YEIEqj3pG5I/AAAAAAAAAGA/XYY_fmE9pxceQQGnPPXTdHQSAKTGh4EQwCPcBGAsYHg/s300/%25E6%258E%25A7%25E5%2588%25B6%25E7%25AE%25B1-RJ45%25E7%25B6%25B2%25E8%25B7%25AF%25E5%25AD%2594_result.jpg)|
|2|在教導器上依序點擊 `主選單（左上角手臂圖樣）> 顯示資訊 > 用戶組`。|![](https://1.bp.blogspot.com/-gsKab2T_R_0/YEIEqmRnNJI/AAAAAAAAAGA/1VewMuujYLkJUrjUdyBD3oPSCK78h2ZXwCPcBGAsYHg/s799/HRSS-%25E5%2588%2587%25E6%258F%259B%25E7%2594%25A8%25E6%2588%25B61_result.jpg)|
|3|選擇「Expert」按下「登入」並輸入密碼 `hiwin`。完成後會顯示用戶組爲「Expert」。|![](https://1.bp.blogspot.com/-zY3syaWgO4c/YEIEqrn8mvI/AAAAAAAAAGA/iHqbfsOJXSEe_NtiE96ECHaO91BKg4S6wCPcBGAsYHg/s800/HRSS-%25E5%2588%2587%25E6%258F%259B%25E7%2594%25A8%25E6%2588%25B62_result.jpg)|
|4|在教導器上依序點擊 `主選單 > 啓動設定 > 網路連接設定`。|![](https://1.bp.blogspot.com/-YBuEk6RLods/YEIEqmJC1vI/AAAAAAAAAGA/Zk-0wLnfp98keZJLGmvICVXUOGl2MLR7wCPcBGAsYHg/s799/HRSS-%25E7%25B6%25B2%25E8%25B7%25AF%25E9%2580%25A3%25E6%258E%25A5%25E8%25A8%25AD%25E5%25AE%259A1_result.jpg)|
|5|下方會顯示此手臂 IP 位置，通常設爲 `192.168.0.3`。|![](https://1.bp.blogspot.com/-3BiMKlNZjEY/YEIEqtC7fVI/AAAAAAAAAGA/nuCvz2ESQBk0PjcVpKtWBb9roK2ZpbW0ACPcBGAsYHg/s800/HRSS-%25E7%25B6%25B2%25E8%25B7%25AF%25E9%2580%25A3%25E6%258E%25A5%25E8%25A8%25AD%25E5%25AE%259A2_result.jpg)|
|6|將教導器右上角的鑰匙轉至「Auto.」模式。|![](https://1.bp.blogspot.com/-bH0bdIBfxRs/YEIEqgmJB2I/AAAAAAAAAGA/iLpl7L6T55kyhcH6PTuuRJR-cmfpzG9mgCPcBGAsYHg/s800/HRSS-Auto%25E6%25A8%25A1%25E5%25BC%258F_result.jpg)|
|7|在教導器上點選「EXT」。|![](https://1.bp.blogspot.com/-vBwwi7KOB4A/YEIEqpUtigI/AAAAAAAAAGA/Ik0yLbkIyig0hu907Qaxbs3RF8u8ex87gCPcBGAsYHg/s180/HRSS-%25E9%2581%25B8%25E6%2593%2587EXT.JPG)|
|8|確認教導器螢幕右上角顯示爲「EXT」模式。|![](https://1.bp.blogspot.com/-k6krFqtpVxg/YEIEqtaV-qI/AAAAAAAAAGA/C55h8eWygh48eDco6HQx0_G6wrStI887gCPcBGAsYHg/s800/HRSS-%25E7%25A2%25BA%25E8%25AA%258D%25E7%2588%25B2EXT_result.jpg)|
|9|在 Windows 中打開 `控制台 > 網路和網際網路 > 網路連線`。右鍵點擊 `目標網路介面卡 > 內容 > 網際網路通訊協定第4版(TCP/IPv4) > 內容`。<br/><br/>手動設定電腦 IP 位址爲 `192.168.0.100`、子網路遮罩爲 `255.255.255.0`，其餘可空白不填。<br/><br/>若有問題，可以嘗試將除手臂用的網路介面卡外的其他所有網路介面卡（如 Wi-Fi）都禁用。|![](https://1.bp.blogspot.com/--S6kK2kQPOc/YEIEqgy3kCI/AAAAAAAAAGA/Aw-Jaeq9I6wA8qOs3_1aUijDZ2JrdzKowCPcBGAsYHg/s826/Win-%25E7%25B6%25B2%25E8%25B7%25AF%25E5%258D%25A1%25E8%25A8%25AD%25E5%25AE%259A_result.jpg)|
|10|在 Windows 打開命令提示字元，使用 `ping` 指令檢測。使用方式爲 `ping 手臂IP`，例如 `ping 192.168.0.3`。<br/><br/>若成功（可以接收到手臂端回傳之封包）則表示網路相關設定應沒問題，可以使用程式與手臂進行連線。|![](https://1.bp.blogspot.com/-I6ogoTnAIDE/YEIEqqFA5_I/AAAAAAAAAGA/eJVm5y73h-Y_r8IBPpYNXKAq5uVHbb7XwCPcBGAsYHg/s677/CMD-ping_s.JPG)|
|11|若網路相關設定有誤或手臂 IP 不對，會顯示「目的地主機無法連線」。|![](https://1.bp.blogspot.com/-4I4G3bfN4aA/YEIEqmxIlnI/AAAAAAAAAGA/Uu54psC0xKI_DpxE7AoIBy6nmnzfmhHTwCPcBGAsYHg/s677/CMD-ping_f.JPG)|

常見問題：
- HRSS 版本與 HRSDK 版本有對應關係，如有更新任一方，應向上銀確定，否則可能會造成手臂無法連線。
- 除非有需求，不然保險起見，應將除了手臂連線用的網路介面卡外的所有網路介面卡都禁用。
- IP 位置 `127.0.0.1` 代表的是該電腦自己本身（localhost），是測試的時候才會用到的，實際使用上不應出現或使用此 IP。
- HRSDK 都應有隨附上銀所提供的 SampleCode 範例程式，可作爲手臂測試用。

> 編輯此章節時的 HRSS 版本 `3.3.11.7492`，HRSDK 版本 `2.2.9_7492`。

## 以教導器控制

# 工作流程 Workflow
工作流程大致上與 GitHub-Flow 一樣，請先去瞭解其運作，並善用 [nfu-irs-lab/test](https://github.com/nfu-irs-lab/test) 進行練習。

在此每個 repo 會有兩個 Branch：`main` 和 `develop`。其中 `develop` Branch 的功能就是 GitHub-Flow 中的 `main` 或 `master` Branch，而我們真正的 `main` Branch 只作為發行用，只由管理員負責管理，一般人不需要也不允許操作組織上的 `main` Branch（除了 Pull）。


[![圖解實驗室Git工作流程](../figs/實驗室Git工作流程_1.svg)](../figs/實驗室Git工作流程_1.svg)
###### ▲ 實驗室 Git 工作流程

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

## 管理員

# 相關 Repository 列表
- 其它
  - 基本共用程式：[hiwinrobot](https://github.com/nfu-irs-lab/hiwinrobot)
  - 手機控制程式：[hiwinrobot-controller-app](https://github.com/nfu-irs-lab/hiwinrobot-controller-app)
  - HRTK (NuGet Package)：[hiwinrobot-toolkit](https://github.com/nfu-irs-lab/hiwinrobot-toolkit)
  - 舊範例程式（不推薦）：[hiwinrobot-old-example](https://github.com/nfu-irs-lab/hiwinrobot-old-example/tree/master)
  - XEG 夾爪範例程式：[hiwinrobot-xeg-gripper-example](https://github.com/nfu-irs-lab/hiwinrobot-xeg-gripper-example)
- 14屆 `2021`
  - 智慧撞球：none
  - 智慧拼圖：none
  - 智慧創作：none
- 13屆 `2020`
  - 智慧撞球：[hiwinrobot-13-billiards](https://github.com/nfu-irs-lab/hiwinrobot-13-billiards)
  - 智慧拼圖：[hiwinrobot-13-puzzle](https://github.com/nfu-irs-lab/hiwinrobot-13-puzzle)
  - 智慧分類：[hiwinrobot-13-classification](https://github.com/nfu-irs-lab/hiwinrobot-13-classification)

<details>
  <summary>更早之前的 Repository</summary>

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

</details>
