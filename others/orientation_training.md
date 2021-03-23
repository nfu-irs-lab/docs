# 新進人員訓練

推薦在 [HackMD](https://hackmd.io/@nfu-robot-lab/B1Sc0H7Ed) 上觀看。

<details>
  <summary>QR Code</summary>
  <a href="https://1.bp.blogspot.com/-plBvVKkiokc/YFazM6wl8zI/AAAAAAAAAVw/_cnYyq1dUb0eIqVaayKUot3pl-l3rplBQCPcBGAsYHg/s333/%25E5%25AF%25A6%25E9%25A9%2597%25E5%25AE%25A4-%25E6%2596%25B0%25E9%2580%25B2%25E4%25BA%25BA%25E5%2593%25A1%25E8%25A8%2593%25E7%25B7%25B4%2528HackMD%2529.png"><img src="https://1.bp.blogspot.com/-plBvVKkiokc/YFazM6wl8zI/AAAAAAAAAVw/_cnYyq1dUb0eIqVaayKUot3pl-l3rplBQCPcBGAsYHg/s333/%25E5%25AF%25A6%25E9%25A9%2597%25E5%25AE%25A4-%25E6%2596%25B0%25E9%2580%25B2%25E4%25BA%25BA%25E5%2593%25A1%25E8%25A8%2593%25E7%25B7%25B4%2528HackMD%2529.png"></a>
</details>

## 目錄
- [新進人員訓練](#新進人員訓練)
  - [目錄](#目錄)
- [實驗室環境介紹](#實驗室環境介紹)
  - [NAS（雲端）](#nas雲端)
- [階段一](#階段一)
  - [3D 工業建模](#3d-工業建模)
    - [軟體介紹](#軟體介紹)
    - [註冊 Onshape](#註冊-onshape)
    - [建立檔案](#建立檔案)
    - [繪製 2D 草圖](#繪製-2d-草圖)
    - [生成 3D 特徵](#生成-3d-特徵)
    - [複製-鏡射](#複製-鏡射)
    - [複製-環狀複製排列](#複製-環狀複製排列)
    - [圓角與倒角](#圓角與倒角)
    - [組合](#組合)
  - [[驗收-1] 繪製馬達之 3D 模型](#驗收-1-繪製馬達之-3d-模型)
- [階段二](#階段二)
  - [雷射切割機](#雷射切割機)
  - [3D 列印機](#3d-列印機)
    - [取得 STL 檔](#取得-stl-檔)
    - [設定切片軟體](#設定切片軟體)
    - [切片](#切片)
    - [進行列印](#進行列印)
    - [列印完成](#列印完成)
    - [其它注意事項](#其它注意事項)
  - [[驗收-2] 自行設計並製作機械手臂](#驗收-2-自行設計並製作機械手臂)
- [階段三](#階段三)
  - [Robotis 套件](#robotis-套件)
  - [[驗收-3] 以 Robotis 套件控制機械手臂](#驗收-3-以-robotis-套件控制機械手臂)
- [階段四](#階段四)
  - [C# 入門](#c-入門)
  - [[驗收-4] 以 C# 控制機械手臂](#驗收-4-以-c-控制機械手臂)
- [整理與收拾](#整理與收拾)

> [回到主頁面](https://github.com/nfu-irs-lab/docs#實驗室文件)

---
# 實驗室環境介紹
## NAS（雲端）
實驗室的 NAS 地址為 `\\robothd`（不分大小寫，注意斜線方向）。於檔案總管上方的地址列輸入其地址就可以訪問，帳號與密碼請詢問學長。

# 階段一
## 3D 工業建模
###  軟體介紹
目前實驗室主要使用 [Onshape](https://www.onshape.com) 和 SolidWorks 來進行 3D 建模。

[Onshape](https://www.onshape.com) 可以免費使用，SolidWorks 需要付費使用，另外也可以選擇使用學校 E-mail（@gm.nfu.edu.tw）去申請 [Autodesk Inventor](https://www.autodesk.com.tw/products/inventor/overview) 的免費學術授權。

以下僅介紹 [Onshape](https://www.onshape.com)。其它軟體使用起來操作與概念相同、大同小異。

### 註冊 Onshape
進入 [Onshape](https://www.onshape.com/signup) 的註冊頁面，於下方的方案選擇「Public Maker Plan」（也可以使用學校帳號申請註冊「Education Account」）。

[![](https://1.bp.blogspot.com/-NgzDc19D5Yg/YFRj9TNCxQI/AAAAAAAAAHs/ifkN-_mGGBQq2S7q-LzQXi4-HLUE96V_wCPcBGAsYHg/s1821/onshape-%25E8%25A8%25BB%25E5%2586%258A1.png)](https://1.bp.blogspot.com/-NgzDc19D5Yg/YFRj9TNCxQI/AAAAAAAAAHs/ifkN-_mGGBQq2S7q-LzQXi4-HLUE96V_wCPcBGAsYHg/s1821/onshape-%25E8%25A8%25BB%25E5%2586%258A1.png)
> ▲ 選擇「Public Maker Plan」方案。

進入新的頁面後，點擊「Get Started」開始進行註冊。註冊帳號沒什麼特別要注意的，不過「What best describes you？」欄位可以選擇「Hobbyist / Maker」就好。

[![](https://1.bp.blogspot.com/-6mWs7mYEC6Y/YFRnEp97-_I/AAAAAAAAAIw/xDkXwKi8eJsAi86yMlU-uvwpuNsSie4ZwCPcBGAsYHg/s666/onshape-%25E8%25A8%25BB%25E5%2586%258A2.png)](https://1.bp.blogspot.com/-6mWs7mYEC6Y/YFRnEp97-_I/AAAAAAAAAIw/xDkXwKi8eJsAi86yMlU-uvwpuNsSie4ZwCPcBGAsYHg/s666/onshape-%25E8%25A8%25BB%25E5%2586%258A2.png)
> ▲ 填寫註冊資料

完成註冊後就可以開始使用。

> - 若有詢問習慣的單位，請使用 MMGS 制：長度單位為 `Millimeter`、角度單位為 `Degree`、質量單位為 `Gram`。
> - 若有詢問習慣的滑鼠操作方式，請選擇「SolidWorks」。

### 建立檔案
> 以下內容之單位皆使用 MMGS 制。

登入 Onshape 並進到主頁面。點擊左上角的「建立」按鈕並選擇「文件」，來創建新的檔案。

[![](https://1.bp.blogspot.com/-hBJMA7n1wWI/YFRpP1ESuyI/AAAAAAAAAJg/glYwCEGk14kDBs3C-_qCSPfLUINg0JtagCPcBGAsYHg/s1920/onshape-%25E4%25BD%25BF%25E7%2594%25A81.png)](https://1.bp.blogspot.com/-hBJMA7n1wWI/YFRpP1ESuyI/AAAAAAAAAJg/glYwCEGk14kDBs3C-_qCSPfLUINg0JtagCPcBGAsYHg/s1920/onshape-%25E4%25BD%25BF%25E7%2594%25A81.png)
> ▲ Onshape 主頁面

3D 工業建模的步驟大致如下，各個軟體都差不多：
1. 選擇一個目標平面作為起始平面。
2. 在起始平面上繪製 2D 草圖。
3. 選擇一個 2D 草圖來生成 3D 特徵。
4. 重複以上過程來增加更多的樣式。

[![](https://1.bp.blogspot.com/-oELCi4ArEu8/YFRr7q4ihqI/AAAAAAAAAKg/kVHadamjFMEDKtzcZZZv-5xfSnR_SmsvACPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A82.png)](https://1.bp.blogspot.com/-oELCi4ArEu8/YFRr7q4ihqI/AAAAAAAAAKg/kVHadamjFMEDKtzcZZZv-5xfSnR_SmsvACPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A82.png)
> ▲ 建模操作介面

以下示範動作時，可以注意右上角的視角姿態方塊，有助於瞭解目前畫面的視角。

### 繪製 2D 草圖

選擇平面「Top」來作為起始平面，並點選左上角的「草圖」來繪製草圖。在上方工具列中選擇「中心點矩形」，以平面為中心拉出矩形。大小尺寸還不用太精準。

[![](https://1.bp.blogspot.com/-hvylk6miWRY/YFRtgfpBkvI/AAAAAAAAALM/FcRROM5JACM_yU-GsExaMSYCRurty9hlwCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A83.png)](https://1.bp.blogspot.com/-hvylk6miWRY/YFRtgfpBkvI/AAAAAAAAALM/FcRROM5JACM_yU-GsExaMSYCRurty9hlwCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A83.png)
> ▲ 繪製草圖

點需上方工具列的「尺寸」來點擊矩形的邊線，並指定該矩形的實際尺寸為長 `100 mm`、寬 `50 mm`。

在使用「尺寸」工具輸入數字時，可以直接使用基本的加減乘除運算。例如在輸入尺寸時可以直接輸入 `(100.5/2)+3.15`。

[![](https://1.bp.blogspot.com/-h25sLJ_5JSg/YFRv9QM1IGI/AAAAAAAAAMQ/5m1_1PEimSQtBQWaDg9tOUrkV9lmbVR0gCPcBGAsYHg/s1833/onshape-%25E4%25BD%25BF%25E7%2594%25A84.png)](https://1.bp.blogspot.com/-h25sLJ_5JSg/YFRv9QM1IGI/AAAAAAAAAMQ/5m1_1PEimSQtBQWaDg9tOUrkV9lmbVR0gCPcBGAsYHg/s1833/onshape-%25E4%25BD%25BF%25E7%2594%25A84.png)
> ▲ 設定尺寸

點選左上角「草圖1」的綠色勾勾，完成此 2D 草圖。

### 生成 3D 特徵

選擇「草圖1」，並點選上方工具列的「擠出」。在擠出視窗中將「深度」設為 `15 mm`，點擊綠色勾勾來完成。

此時模型已經是 3D 的了。

[![](https://1.bp.blogspot.com/-3Yjb1kbQQrk/YFRxvJre-lI/AAAAAAAAANA/GLnkraNhv5YdoSxtyzNpoGcZi83JM6AIACPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A85.png)](https://1.bp.blogspot.com/-3Yjb1kbQQrk/YFRxvJre-lI/AAAAAAAAANA/GLnkraNhv5YdoSxtyzNpoGcZi83JM6AIACPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A85.png)
> ▲ 擠出

繼續點選「擠出1」長方體的頂面，再次新增草圖，並使用「中心點畫圓」與「尺寸」工具在此草圖的中心點畫一個直徑為 `35 mm` 的圓形。符號「Ø」代表該尺寸為直徑。

點選綠色勾勾來完成此草圖（草圖2）。

[![](https://1.bp.blogspot.com/-1yQb4TyLiRE/YFRzzyaWc7I/AAAAAAAAANw/JffC0CpRHHk0G8fbFcipDSQRVnp04G_fwCPcBGAsYHg/s1838/onshape-%25E4%25BD%25BF%25E7%2594%25A86.png)](https://1.bp.blogspot.com/-1yQb4TyLiRE/YFRzzyaWc7I/AAAAAAAAANw/JffC0CpRHHk0G8fbFcipDSQRVnp04G_fwCPcBGAsYHg/s1838/onshape-%25E4%25BD%25BF%25E7%2594%25A86.png)
> ▲ 再畫一個圓形

選擇「草圖2」並點選「擠出」，在「擠出2」視窗中選擇「移除」，並選擇「完全貫穿」。完成此特徵。

此時原本的長方體中間會有一個圓形的洞，並且完全貫穿。

[![](https://1.bp.blogspot.com/-7GBn7b-eg9g/YFR1b5OY-0I/AAAAAAAAAOc/Leppc9W4lNQFxUIkv0K3G41rtBlr9tTWgCPcBGAsYHg/s1832/onshape-%25E4%25BD%25BF%25E7%2594%25A87.png)](https://1.bp.blogspot.com/-7GBn7b-eg9g/YFR1b5OY-0I/AAAAAAAAAOc/Leppc9W4lNQFxUIkv0K3G41rtBlr9tTWgCPcBGAsYHg/s1832/onshape-%25E4%25BD%25BF%25E7%2594%25A87.png)
> ▲ 使用「擠出-移除」來挖空

### 鏡射
有些特徵會重複出現，這時可以使用各種複製功能，就不用每個相同的特徵都要畫。

選擇長方體的側面（Z-X 面、前視），並新增一草圖。在此平面的短邊（Z 方向的邊線）的中心點位置旁邊新增一個「中心點畫圓」，並將圓的直徑設為 `5 mm`。

再使用「尺寸」工具依序點選圓心與短邊。將圓心到短邊的距離設為 `8 mm`。一般在設定圓的位置時會以圓心為基準，而不是使用圓周為基準，以圓心為基準的好處是改變圓的大小（直徑）時不會影響其位置。

完成此草圖（草圖3）。

[![](https://1.bp.blogspot.com/-d8wqcC5achk/YFR5IQwHZ_I/AAAAAAAAAPg/EHXRNyCJ4HkzazKkfQpZ7Jfs5GUmS4HvgCPcBGAsYHg/s1842/onshape-%25E4%25BD%25BF%25E7%2594%25A88.png)](https://1.bp.blogspot.com/-d8wqcC5achk/YFR5IQwHZ_I/AAAAAAAAAPg/EHXRNyCJ4HkzazKkfQpZ7Jfs5GUmS4HvgCPcBGAsYHg/s1842/onshape-%25E4%25BD%25BF%25E7%2594%25A88.png)
> ▲ 再畫圓

將草圖3使用「擠出-移除-完成貫穿」來挖空（擠出3）。

點選「鏡射」工具。
- 在鏡射視窗上選擇「鏡射特徵」。
- 「要鏡射的特徵」選擇「擠出3」
- 「鏡射平面」選擇「Right」（透過點擊左方的清單來選擇）。

點擊綠色勾勾來完成鏡射。

[![](https://1.bp.blogspot.com/-Bl7UsR8aFGk/YFR7LUzhW6I/AAAAAAAAAQQ/CMP9a-c_myEjeOEOx0ZGt5HkPFS6EVEYgCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A89.png)](https://1.bp.blogspot.com/-Bl7UsR8aFGk/YFR7LUzhW6I/AAAAAAAAAQQ/CMP9a-c_myEjeOEOx0ZGt5HkPFS6EVEYgCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A89.png)
> ▲ 鏡射

### 環狀複製排列
點擊長方體的頂面（Y-X 面、上視），新增草圖並在距離中心大圓孔（擠出2）`20 mm`（圓心中心距）的上面畫一個直徑為 `3 mm` 的圓。並完成此草圖（草圖4）。

[![](https://1.bp.blogspot.com/-AuiSrFPCcVo/YFR9iTdhSqI/AAAAAAAAARA/xyTgwYsOkmsg757nEn-ctx7uBqHwFeofgCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A810.png)](https://1.bp.blogspot.com/-AuiSrFPCcVo/YFR9iTdhSqI/AAAAAAAAARA/xyTgwYsOkmsg757nEn-ctx7uBqHwFeofgCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A810.png)
> ▲ 畫圓

選擇「草圖4」並「擠出」，選擇「新增」並將深度設為 `5 mm`。完成此擠出（擠出4）。

點選「環狀複製排列」工具。
- 在視窗上選擇「特徵複製排列」。
- 「要複製排列的特徵」選擇「擠出4」
- 「複製排列軸」點選中心圓心（擠出2）的圓周
- 「實例數量」設為 3
- 勾選「同等間距」。

完成此環狀複製排列。

[![](https://1.bp.blogspot.com/-CuVV61MGwgA/YFR_C_LJTFI/AAAAAAAAARs/rkrAE-3bkj0ybgHINTbNmi4cSkMrG3OFwCPcBGAsYHg/s1836/onshape-%25E4%25BD%25BF%25E7%2594%25A811.png)](https://1.bp.blogspot.com/-CuVV61MGwgA/YFR_C_LJTFI/AAAAAAAAARs/rkrAE-3bkj0ybgHINTbNmi4cSkMrG3OFwCPcBGAsYHg/s1836/onshape-%25E4%25BD%25BF%25E7%2594%25A811.png)
> ▲ 進行「環狀複製排列」

「線性複製排列」的操作概念與「環狀複製排列」差不多，請自行摸索並嘗試。

### 圓角與倒角

點選「圓角」。「要圓角的圖元」選擇前視的兩個長邊與兩個圓周。並完成圓角。

[![](https://1.bp.blogspot.com/-xAeF-cuAacw/YFSBTuqa6dI/AAAAAAAAASg/ZNIWIiUvGBg3VDyywr31pMDTxznb2B_CQCPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A812.png)](https://1.bp.blogspot.com/-xAeF-cuAacw/YFSBTuqa6dI/AAAAAAAAASg/ZNIWIiUvGBg3VDyywr31pMDTxznb2B_CQCPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A812.png)
> ▲ 圓角

點選「倒角」。「要倒角的圖元」選擇後視的兩個長邊與兩個圓周。並完成倒角。

[![](https://1.bp.blogspot.com/-3w_d2eEs4n0/YFSCHm_eSII/AAAAAAAAATI/zGSM59XGR90_s2RLckW7QgMY368YqDJEACPcBGAsYHg/s1830/onshape-%25E4%25BD%25BF%25E7%2594%25A813.png)](https://1.bp.blogspot.com/-3w_d2eEs4n0/YFSCHm_eSII/AAAAAAAAATI/zGSM59XGR90_s2RLckW7QgMY368YqDJEACPcBGAsYHg/s1830/onshape-%25E4%25BD%25BF%25E7%2594%25A813.png)
> ▲ 倒角

### 組合
點擊左下角的「+」來「插入新元素」，並選擇「Part Studio」。在剛剛新增的「Part Studio」（Part Studio 2）中繪製一個直徑為 `35 mm`、高度為 `25 mm` 的圓柱體。

在下方的元素列中點選「Assembly 1」（若沒有請自行新增）。點擊左上角的「插入」並選擇「Part Studio 1」，將其放置到畫面上。再選擇「Part Studio 2」放置到畫面上。點擊綠色勾勾完成插入。

在左側的清單中對「Part 1」（Part Studio 1）點擊滑鼠右鍵，並選擇「固定」。

[![](https://1.bp.blogspot.com/-LRd2WO5H2dg/YFSEeWcGxWI/AAAAAAAAAT4/jlcHg8qI90UCX_EdB2Fw8XlMqcBcTZrSQCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A814.png)](https://1.bp.blogspot.com/-LRd2WO5H2dg/YFSEeWcGxWI/AAAAAAAAAT4/jlcHg8qI90UCX_EdB2Fw8XlMqcBcTZrSQCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A814.png)
> ▲ 插入零件

點選「滑動結合」。在「結合連接器」中選擇兩元件的圓柱面。點擊綠色勾勾完成。

此時圓柱體可以在圓孔中滑動（Z 方向）。

[![](https://1.bp.blogspot.com/-VRUvCG8dR-U/YFSG4DGZITI/AAAAAAAAAU4/ImVpfsLXuqAYLJ93sru_hznezfqJ4yD_ACPcBGAsYHg/s1836/onshape-%25E4%25BD%25BF%25E7%2594%25A815.png)](https://1.bp.blogspot.com/-VRUvCG8dR-U/YFSG4DGZITI/AAAAAAAAAU4/ImVpfsLXuqAYLJ93sru_hznezfqJ4yD_ACPcBGAsYHg/s1836/onshape-%25E4%25BD%25BF%25E7%2594%25A815.png)
> ▲ 滑動結合

結合的方式有許多種，操作皆大同小異，請自行摸索練習。

## [驗收-1] 繪製馬達之 3D 模型
請拿一個實驗室的 AX-12 馬達，並繪製其 3D 模型。馬達的尺寸請使用遊標卡尺自行測量。

# 階段二
## 雷射切割機
## 3D 列印機
目前實驗室共有 3 臺 3D 列印機，分別為：
- ATOM 2.5 EX（Delta 型）
- ATOM 2.5 FX（Delta 型）
- UPBOX（笛卡爾型）

一般都是使用「ATOM 2.5 EX 」與「ATOM 2.5 FX」。以下僅示範它們的使用操作。

### 取得 STL 檔
要列印 3D 模型，首先要取得該模型的 STL 檔。若想要列印在 onshape 上繪製的模型，只要將該模型匯出即可。

在 onshape 中打開欲列印的檔案，在下方的元件列中以對目標元件點擊滑鼠右鍵，並選擇「匯出」。並調整匯出的設定如下：

- 檔案名稱：*自行決定*
- 格式：STL
- STL 格式：二進制
- 單位：Milimeter（實驗室習慣 MMGS 制，實際請依照該模型的真實單位選擇。）
- 解析度：*自行決定*
- 選項：*自行決定*

按下「確定」後就會下載該模型的 STL 檔。

> 若使用 SolidWorks 的話，請直接開啟目標模型的檔案，並另存新檔（Save as），並在檔案格式中選擇「STL」即可。

### 設定切片軟體
3D 列印機無法直接列印 STL 檔，必須要使用切片軟體設定好列印參數後，再將 STL 檔轉換成 G-Code 檔（.gcode）才可以進行列印。

切片軟體有非常多種，如 Cura、Slic3r 或 KISSlicer。以下僅示範 ATOM 官方所推薦及提供的 Cura。

> Cura 軟體可以在實驗室 NAS 中找到，也可以去 [ATOM](https://www.atom3dp.com/%E5%88%87%E7%89%87%E8%BB%9F%E9%AB%94%E8%A8%AD%E5%AE%9A%E6%AA%94) 官網下載。  
> 唯要注意 ATOM 官網所提供的 Cura 才有包含其 3D 列印機的基本設定，直接到 Ultimaker 下載的 Cura 沒有。

首次安裝完 Cura 時，應會請你選擇 3D 列印機的型號（如：2.5 EX 或 2.5 FX），請依照自己實際要使用的機台作選擇（未來還可以改）。

開啟 Cura 後，在右側是列印的參數設定，請將「列印設定」由「推薦」改成「自訂選項」。並修改其中的設定值如下：

- 品質
  - 層高：`0.3 mm`
- 外殼
  - 牆壁線條圈數：`3`
  - 頂部層數：`3`
  - 底部層數：`3`
  - 水平擴展：`0 mm`
- 填充
  - 填充密度：`15%`（通常不用設超過 `25%`，再高的意義不大。）
  - 填充列印樣式：`網格`（可以讓 Cura 依照填充密度自動調整。）
- 耗材
  - 列印溫度：`200°C`（ATOM 2.5 EX (FX) 使用的材料為 PLA。）
  - 列印平台溫度：`60°C`
  - 啟用回抽：`[√]`
- 速度
  - 列印速度：`25 mm/s`
  - 起始層速度：`17.5 mm/s`
- 空跑
  - 回抽時 Z 抬升：`[√]`
- 冷卻
  - 開啟列印冷卻：`[√]`
  - 最大風扇轉速：`100%`
  - 起始層風扇轉速：`0%`
- 支撐
  - 產生支撐：`[√]`（可依據實際模型是否需要支撐來決定。）
- 列印平台附著
  - 列印平台附著類型：`外圍`
  - 列印平台附著擠出機：`Ext 0`
  - 外圍線條數量：`3`
  - 外圍/邊緣最小長度：`150 mm`
- 雙重擠出機
  - Preload Extruder Retraction：`[√]`
  - 噴頭切換回抽距離：`110 mm`
  - 啟用換料塔：`[ ]`

> - 以上的列印參數都不是絕對的，可以依照不同的需要去自行調整。
> - 如果有上面沒提到的列印參數，請保持原始數值或讓它自動設定。
> - 有些列印參數會互相影響、限制。
> - 如果有些參數沒有顯示出來，請依照以下的方法：
>   - 方法 1：點選上方的「偏好設定」，在打開的視窗中選擇「設定」頁面，在顯示的「參數顯示設定」視窗，將沒有顯示的參數設定在此清單勾選起。
>   - 方法 2：將滑鼠移動到該參數群組（如速度、冷卻）的箭頭（`⋁`）左邊，會顯示一個齒輪的圖案，點擊就會顯示「參數顯示設定」視窗，將沒有顯示的參數設定在此清單勾選起。
> - 若要列印的模型底面積太小，請將「列印平台附著」改成以下的設定：
>   - 列印平台附著類型：`邊緣`
>   - 列印平台附著擠出機：`Ext 0`
>   - 外圍/邊緣最小長度：`150 mm`
>   - 邊緣寬度：`10 mm`
>   - 僅在外部列印邊緣：`[√]`

### 切片
設定好列印參數後就可以進行切片。

將目標 STL 檔加到 Cura 中（開啟檔案或直接拖拉）。當模型進入到 Cura 中時，可以選擇它，並利用左側的列表來旋轉、移動或複製該模型。

點擊右下角的「準備」就會開始進行切片。切片完成後可以在上方的下拉時選單中將「實體檢視」改成「分層檢視」，來觀察切片完成後的模型。

確定沒問題後就可以點擊右下角的「儲存檔案」，來輸出成 G-Code 檔（.gcode）。

### 進行列印
將「ATOM 2.5 EX (FX)」的 SD 卡取下，並將目標 G-Code 檔（.gcode）放到 SD 卡內，再將 SD 卡插回機台並開啟電源即可。

> ATOM 2.5 EX (FX) 無法讀取中文檔名，會變成亂碼，故檔名請使用英文或數字。

在「ATOM 2.5 EX (FX)」中按下旋鈕進入到選單中，並旋轉旋鈕直到選擇到「Print Form SD」再按下旋鈕，旋轉旋鈕來選擇要列印的 G-Code 檔案並按下旋鈕。

此時就會進入列印程序，機台會先進行平台（熱床）加熱，完成後再進行擠出頭加熱。當平台與擠出頭都加熱到目標溫度後，就會自動開始進行列印。

開始進行列印後，可以先觀察一開始第一層的列印情況，如果有問題（如沒有附著）的話，可以馬上暫停列印，進行調整後再重新列印。如果第一層的列印沒有什麽問題的話，就可以等待列印完成了。

> 要停止列印，請按下旋鈕進入選單，並旋轉旋鈕直到選擇到「Stop Print & Home」並按下旋鈕。 

### 列印完成
列印完成後可以利用鏟刀來將列印完成之列印件從列印平台上剷起。使用尖嘴鉗或斜口鉗將多餘的部分（如支撐支架、邊緣）去除。

等待 3D 列印機的擠出頭溫度降到 `100°C` 以下後就可以關閉電源。離開時記得清潔乾净、將垃圾丟到垃圾桶並將工具放回原位。

### 其它注意事項
- 3D 列印的尺寸誤差較大，在進行模型繪製時請將此因素考慮進尺寸的設定中。
- 嘗試列印時可以將列印品質調低（如降低填充密度），來節省時間與耗材，等確定該模型沒問題後，再進行正式的列印。
- 3D 列印件的强度有限，如果需要較高强度的零件，請選擇其它加工成型方式，而不是一味地增加填充密度（填充密度建議不要超過 `25%`，再高的意義不大、强度增加有限，但會大幅增加列印時間與耗材使用）。

## [驗收-2] 自行設計並製作機械手臂
使用之前所繪製的 AX-12 馬達 3D 模型，再自行繪製其支撐零件，設計一個帶夾爪的機械手臂。並利用雷射切割機或 3D 列印機將零件製作出來，並完成組裝。

機械手臂的結構不限（關節式、SCARA），但應要有辦法完成「驗收-4」的要求。夾抓結構不限，但應要能將夾抓張開到至少 `8 cm`，以便完成「驗收-4」的要求。

> 組裝時會用到螺絲，請將所有用到的螺絲規格（如 `M2×10mm`）列表記錄，以方便之後拆解完可以將螺絲按照正確的規格分類。

# 階段三
## Robotis 套件
## [驗收-3] 以 Robotis 套件控制機械手臂

# 階段四
## C# 入門
## [驗收-4] 以 C# 控制機械手臂

# 整理與收拾
