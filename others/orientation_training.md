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
  - [[驗收-1] 繪製馬達之 3D 模型](#驗收-1-繪製馬達之-3d-模型)
- [階段二](#階段二)
  - [雷射切割機](#雷射切割機)
  - [3D 列印機](#3d-列印機)
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

:triangular_flag_on_post: 在 YouTube 上觀看示範影片。連結：[\[新進人員訓練\] 3D 建模教學-基礎 (onshape)](https://youtu.be/4y7vu-GDY1o)

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

> 該馬達模型在後續也會用到，所以尺寸不能差太多。

# 階段二
## 雷射切割機

:warning: **`雷射切割機若操作不當將導致火災，操作時請小心並多加確認`** :warning:

[![](https://1.bp.blogspot.com/-inS00IaK8AM/YFoMVhr0hHI/AAAAAAAAAZw/I48W9jR7JPMMzH0a-a7l__aPabTkHscVQCPcBGAsYHg/w640-h480/01-%25E6%25A9%259F%25E8%2587%25BA1.jpg)](https://1.bp.blogspot.com/-inS00IaK8AM/YFoMVhr0hHI/AAAAAAAAAZw/I48W9jR7JPMMzH0a-a7l__aPabTkHscVQCPcBGAsYHg/w640-h480/01-%25E6%25A9%259F%25E8%2587%25BA1.jpg)
> ▲ 實驗室的雷射切割機


> 以下將雷射切割機簡稱為雷切機。

### 取得 DXF 檔

雷切機需要使用 DXF 檔（或其它類似的 2D 圖檔）。若檔案是使用 onshape 繪製，只要將目標平面匯出即可。

在 onshape 中打開目標模型，選擇目標平面並按下滑鼠右鍵，在右鍵選單中點選「匯出為 DXF/DWG」。

[![](https://1.bp.blogspot.com/-7M2AEZ8qRP8/YFrfeQCG5xI/AAAAAAAAAbA/IUP9S-vfsVkyNDiMZztX6F7nUDo2WK2pACPcBGAsYHg/s16000/onshape%25E5%258C%25AF%25E5%2587%25BA1.png)](https://1.bp.blogspot.com/-7M2AEZ8qRP8/YFrfeQCG5xI/AAAAAAAAAbA/IUP9S-vfsVkyNDiMZztX6F7nUDo2WK2pACPcBGAsYHg/s16000/onshape%25E5%258C%25AF%25E5%2587%25BA1.png)
> ▲ onshape 匯出

調整匯出參數如下：
- 檔案名稱：*自行決定*
- 格式：DXF
- 版本：Release 14
- 選項：*自行決定*
- `[ ]` 將不規則曲線匯出為聚合線
- `[√]` 將 z-高度設定為零，法線設定為正的

[![](https://1.bp.blogspot.com/-uKTHjaTOjWI/YFrfeR5lRHI/AAAAAAAAAbA/BiZJI6zGRnk63ZRUEEF8zAhoDVmxS7ItgCPcBGAsYHg/w400-h256/onshape%25E5%258C%25AF%25E5%2587%25BA2.png)](https://1.bp.blogspot.com/-uKTHjaTOjWI/YFrfeR5lRHI/AAAAAAAAAbA/BiZJI6zGRnk63ZRUEEF8zAhoDVmxS7ItgCPcBGAsYHg/w400-h256/onshape%25E5%258C%25AF%25E5%2587%25BA2.png)
> ▲ DXF 匯出設定

按下「匯出」後就會下載該 DXF 檔。然後將該 DXF 檔放到實驗室 NAS 或使用隨身碟複製到雷切機電腦上，就可以後續的步驟。

> 若使用 SolidWorks 的話，請調整視角以正對目標平面，再另存新檔（Save As）並在檔案格式選擇「DXF」後，確認就可以了。

### 雷切機開機

開機前先確認鑰匙開關是否已開啟，且緊急停機按鈕「STOP」沒有被按下。

雷切機相關的設備總共有 4 個，使用時請將它們依序打開電源，依序分別為：
- 水冷機
- 水冷液幫補
- 排風扇
- 雷射切割機

:warning: **`打開電源後一定要注意各機器是否有在運作，若有問題將有可能導致火災`** :warning:

[![](https://1.bp.blogspot.com/-djki5Xvaxtg/YFoMVrybnfI/AAAAAAAAAZw/07Gr55Bl0Ws1l9bqmLG9agfbK5rbA5IPwCPcBGAsYHg/w640-h480/02-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E9%259B%25BB%25E6%25BA%25901.jpg)](https://1.bp.blogspot.com/-djki5Xvaxtg/YFoMVrybnfI/AAAAAAAAAZw/07Gr55Bl0Ws1l9bqmLG9agfbK5rbA5IPwCPcBGAsYHg/w640-h480/02-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E9%259B%25BB%25E6%25BA%25901.jpg)
> ▲ 雷切機各電源開關

[![](https://1.bp.blogspot.com/-CqzjryPf4Ls/YFoMVp4KD-I/AAAAAAAAAZw/7oDZZwrRuGcaibOQ23PiCQWvOF0UcBL1gCPcBGAsYHg/w640-h480/03-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25B7%258A%25E6%2580%25A5%25E5%2581%259C%25E6%25AD%25A21.jpg)](https://1.bp.blogspot.com/-CqzjryPf4Ls/YFoMVp4KD-I/AAAAAAAAAZw/7oDZZwrRuGcaibOQ23PiCQWvOF0UcBL1gCPcBGAsYHg/w640-h480/03-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25B7%258A%25E6%2580%25A5%25E5%2581%259C%25E6%25AD%25A21.jpg)
> ▲ 雷切機開機

### 導入 DXF 檔

操作雷切機請使用雷切機專用的電腦，並打開專用程式「LaserCut 5.3」。

[![](https://1.bp.blogspot.com/-GNeeNNRqJnQ/YFoMVs90AeI/AAAAAAAAAZw/MKrPW63fEs832Du9bRtbUDwfzBxYAmV8wCPcBGAsYHg/w400-h300/04-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F1.jpg)](https://1.bp.blogspot.com/-GNeeNNRqJnQ/YFoMVs90AeI/AAAAAAAAAZw/MKrPW63fEs832Du9bRtbUDwfzBxYAmV8wCPcBGAsYHg/w400-h300/04-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F1.jpg)
> ▲ 雷切機程式「LaserCut 5.3」

依序點擊 `文件 > 導入` 並選擇目標 DXF 檔後開啟。注意是「導入」而不是「打開」。

[![](https://1.bp.blogspot.com/-_71qPd0lqss/YFoMVs-c7lI/AAAAAAAAAZw/nDBLps1yCLw4Z0u0Tc55YMRWpKG9MILJACPcBGAsYHg/s461/05-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%25B0%258E%25E5%2585%25A51.jpg)](https://1.bp.blogspot.com/-_71qPd0lqss/YFoMVs-c7lI/AAAAAAAAAZw/nDBLps1yCLw4Z0u0Tc55YMRWpKG9MILJACPcBGAsYHg/s461/05-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%25B0%258E%25E5%2585%25A51.jpg)
> ▲ 導入 DXF 檔

由於繪圖軟體換成 DXF 檔後會形成斷點，而每個斷點都會是一個路徑 ，故在切割前需要使用「合併相連線」減少斷點。

請全選後依序點擊 `工具 > 合併相連線`。調整容差值，視圖檔情況而定，通常預設 `0.01`，點選「OK」即完成。

[![](https://1.bp.blogspot.com/-HbxgFj0BShE/YFoMVrbTRjI/AAAAAAAAAZw/Kpi5kHHpwdUn5OW390s42Bd3OrHSN3DZwCPcBGAsYHg/w640-h480/06-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%2590%2588%25E5%25B9%25B6%25E7%259B%25B8%25E9%2580%25A31.jpg)](https://1.bp.blogspot.com/-HbxgFj0BShE/YFoMVrbTRjI/AAAAAAAAAZw/Kpi5kHHpwdUn5OW390s42Bd3OrHSN3DZwCPcBGAsYHg/w640-h480/06-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%2590%2588%25E5%25B9%25B6%25E7%259B%25B8%25E9%2580%25A31.jpg)
> ▲ 合併相連線

### 設定參數及圖層

接下來要設定雷切參數及圖層。

在雷切機程式右上角會看到目前的圖層及設定。若要進行雷射切割，請將該圖層的「模式」改成「鐳射切割」。

[![](https://1.bp.blogspot.com/-z5uycffSND0/YFoMVmctYjI/AAAAAAAAAZw/C_zmxI_m4LkY98lYtgt5gTB8KhJ6dA9KQCPcBGAsYHg/w286-h640/07-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%259C%2596%25E5%25B1%25A41.jpg)](https://1.bp.blogspot.com/-z5uycffSND0/YFoMVmctYjI/AAAAAAAAAZw/C_zmxI_m4LkY98lYtgt5gTB8KhJ6dA9KQCPcBGAsYHg/w286-h640/07-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%259C%2596%25E5%25B1%25A41.jpg)
> ▲ 圖層

對目標圖層點擊 2 下來開啟參數設置視窗。基本的雷切參數設定如下：
- 加工速度：*視實際要切割之壓克力厚度而定*
- 加工功率：`80.0`（:warning: **`請勿超過此數值，嚴重將導致火災`** :warning:）
- 拐彎功率：`80.0`（:warning: **`請勿超過此數值，嚴重將導致火災`** :warning:）
- 封口重疊長度：`0.0`
- 吹氣模式：`一直吹氣`（:warning: **`請勿亂調此設定，嚴重將導致火災`** :warning:）

而雷切參數中的加工速度要視要切割的壓克力厚度而定。實際數值請詢問學長或自行嘗試。

[![](https://1.bp.blogspot.com/-RcFi3SqJJRI/YFoMVgKN6xI/AAAAAAAAAZw/qCr9a_jQjy89onwwBC805N06PSOS5tHTgCPcBGAsYHg/w400-h275/08-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%258F%2583%25E6%2595%25B8%25E8%25A8%25AD%25E5%25AE%259A1.jpg)](https://1.bp.blogspot.com/-RcFi3SqJJRI/YFoMVgKN6xI/AAAAAAAAAZw/qCr9a_jQjy89onwwBC805N06PSOS5tHTgCPcBGAsYHg/w400-h275/08-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E7%25A8%258B%25E5%25BC%258F%25E5%258F%2583%25E6%2595%25B8%25E8%25A8%25AD%25E5%25AE%259A1.jpg)
> ▲ 雷切參數設定

若要切割的目標零件是中間沒有孔洞，只有外框輪廓的，那就只要設定一個圖層就可以了。但如果是中間有孔洞（如螺絲孔、鏤空）的話，那外框輪廓的線條與內部孔洞的線條要設定不同的圖層，且內部孔洞的圖層順序要在前（雷切機製作的順序為圖層較高的先），這樣做的目的是避免零件切割掉落後產生的誤差。

### 雷切機操作

:warning: **`操作雷切機時，如果出現任何問題或預期外事件，立刻按下緊急停機按鈕（STOP）`** :warning:

設定好參數後就可以按下雷切機程式右下角的「下載數據」，再按下「下載當前加工資料」，程式就會將資料傳輸到雷切機中。

> - 有時後會跳出資料傳輸失敗的訊息，請多嘗試幾次。
> - 請確定雷切機已經開機了再下載數據。

開啟雷切機上蓋，將要切割的壓克力板放入。要注意切割範圍**不可以**超過底下的金屬蜂巢網。

使用雷切機程式上的「Y+」、「Y-」、「X+」、「X-」來移動雷射頭。

將雷射頭移動到壓克力板上，預計要切割的圖形最右上角的位置，並在雷射頭及壓克力板之間放置對焦片。手扶著雷射頭下方，並用手輕輕地將雷射頭對焦螺絲轉鬆，令雷射頭碰觸對焦片，再用手轉緊螺絲，即完成對焦。

對焦完成後就可以將對焦片拿起並收納好。

:warning: **`注意事項`** :warning:
- 請注意手一定要扶著雷射頭再轉鬆螺絲，不然雷射頭會突然掉落造成撞擊，導致失焦。
- 這裡要轉靜/鬆的螺絲是比較上面的內六角黑色螺絲，不是連接著吹氣管的銀色手轉螺絲（吹氣氣閥調整螺絲）。若發現轉錯請**立即停止操作**，並告知學長。

[![](https://1.bp.blogspot.com/-pMr6tegd9sg/YFsfv4MV9HI/AAAAAAAAAcE/gmQty2k4YWAshViaTQrBhRQ1RzHLvVprACPcBGAsYHg/s16000/10-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E5%25B0%258D%25E7%2584%25A6%25E7%2589%25871.jpg)](https://1.bp.blogspot.com/-pMr6tegd9sg/YFsfv4MV9HI/AAAAAAAAAcE/gmQty2k4YWAshViaTQrBhRQ1RzHLvVprACPcBGAsYHg/s16000/10-%25E9%259B%25B7%25E5%2588%2587%25E6%25A9%259F%25E5%25B0%258D%25E7%2584%25A6%25E7%2589%25871.jpg)
> ▲ 雷射頭對焦。

完成對焦後可以按下雷切機程式右側的「走邊框」，這時雷射頭會繞著要切割形狀的最大外接矩形，可以依據它移動的路徑與範圍來判斷壓克力板的空間是否足夠，若不足夠請調整雷射頭位置或移動/更換壓克力板。

都確定沒問題後，將雷切機的上蓋蓋起，並按下雷切機程式右側的「開始」，機台就會開始進行動作。雷切機運作時會產生高強度雷射，請勿用眼睛直視，否則會受傷。

:warning: **``雷切機運作時一定要待旁邊，若有意外發生請立刻按下緊急停機按鈕（STOP）``** :warning:

等雷切機完成後即可打開上蓋，小力觸碰切割零件，確認是否已經完全切斷，如果沒有切斷，可以再次進行切割。如果已經完全切斷，就可以將零件及壓克力板拿起，將切割之餘碎料丟到垃圾桶。

### 復歸

如果雷切工作都已經結束了，請進行復歸動作。
- 將雷射頭對焦調整螺絲轉鬆，把雷射對焦頭完全升起後再鎖上。
- 按下雷切機程式的「原點」（X-Y 平面），等待雷射頭自動回到原點。
- 將壓克力板拿出並且清潔乾淨。
- 蓋上雷切機的上蓋。

### 雷切機關機

要關機的話，請將各設備依序開機時的相反順序關閉電源，依序分別為：
- 雷射切割機
- 排風扇
- 水冷液幫補
- 水冷機

:warning: **`一定要確定機台都確實關機停止運作，否則有可能導致火災`** :warning:

## 3D 列印機
目前實驗室共有 3 台 3D 列印機，分別為：
- ATOM 2.5 EX（Delta 型）
- ATOM 2.5 FX（Delta 型）
- UP BOX（笛卡爾型）

一般都是使用「ATOM 2.5 EX」與「ATOM 2.5 FX」。以下僅示範它們的使用操作。

### 取得 STL 檔
要列印 3D 模型，首先要取得該模型的 STL 檔。若想要列印在 onshape 上繪製的模型，只要將該模型匯出即可。

在 onshape 中打開欲列印的檔案，在下方的元件列中以對目標元件點擊滑鼠右鍵，並選擇「匯出」。調整匯出的設定如下：

- 檔案名稱：*自行決定*
- 格式：STL
- STL 格式：二進制
- 單位：Milimeter（實驗室習慣 MMGS 制，實際請依照該模型的真實單位選擇。）
- 解析度：*自行決定*
- 選項：*自行決定*

按下「確定」後就會下載該模型的 STL 檔。

> 若使用 SolidWorks 的話，請直接開啟目標模型的檔案，並另存新檔（Save As），在檔案格式中選擇「STL」即可。

[![](https://1.bp.blogspot.com/-X1lSfXJWSEo/YFn1FmfBAJI/AAAAAAAAAW4/pKJuCXIQoRQCqu_p5Zq6qMWdW8OgYZjVwCPcBGAsYHg/w640-h334/01-onshape%25E5%258C%25AF%25E5%2587%25BA1.png)](https://1.bp.blogspot.com/-X1lSfXJWSEo/YFn1FmfBAJI/AAAAAAAAAW4/pKJuCXIQoRQCqu_p5Zq6qMWdW8OgYZjVwCPcBGAsYHg/w640-h334/01-onshape%25E5%258C%25AF%25E5%2587%25BA1.png)

> ▲ 在 onshape 匯出

[![](https://1.bp.blogspot.com/-PmdzrisaDxI/YFn1FmTfmVI/AAAAAAAAAW4/PROqaxx-WY0rF-MFRvbk0NUgzIbguN2hwCPcBGAsYHg/w400-h383/02-onshape%25E5%258C%25AF%25E5%2587%25BASTL%25E8%25A8%25AD%25E5%25AE%259A1.png)](https://1.bp.blogspot.com/-PmdzrisaDxI/YFn1FmTfmVI/AAAAAAAAAW4/PROqaxx-WY0rF-MFRvbk0NUgzIbguN2hwCPcBGAsYHg/w400-h383/02-onshape%25E5%258C%25AF%25E5%2587%25BASTL%25E8%25A8%25AD%25E5%25AE%259A1.png)
> ▲ onshape 匯出 STL 設定

### 設定切片軟體
3D 列印機無法直接列印 STL 檔，必須要使用切片軟體設定好列印參數後，再將 STL 檔轉換成 G-Code 檔（.gcode）才可以進行列印。

切片軟體有非常多種，如 Cura、Slic3r 或 KISSlicer。以下僅示範 ATOM 官方所推薦及提供的 Cura。

> Cura 軟體可以在實驗室 NAS 中找到，也可以去 [ATOM](https://www.atom3dp.com/%E5%88%87%E7%89%87%E8%BB%9F%E9%AB%94%E8%A8%AD%E5%AE%9A%E6%AA%94) 官網下載。  
> 唯要注意 ATOM 官網所提供的 Cura 才有包含其 3D 列印機的基本設定，直接到 Ultimaker 下載的 Cura 沒有。

首次安裝完 Cura 時，應會請你選擇 3D 列印機的型號（如：2.5 EX 或 2.5 FX），請依照自己實際要使用的機台作選擇（未來還可以改）。

[![](https://1.bp.blogspot.com/-TTJjUNSidy0/YFn1Fr-FooI/AAAAAAAAAW4/fzBvqrs0kZs7WhGooczqQFXVI7hcVqhnACPcBGAsYHg/w640-h376/03-Cura%25E8%25A8%25AD%25E5%25AE%259A1.png)](https://1.bp.blogspot.com/-TTJjUNSidy0/YFn1Fr-FooI/AAAAAAAAAW4/fzBvqrs0kZs7WhGooczqQFXVI7hcVqhnACPcBGAsYHg/w640-h376/03-Cura%25E8%25A8%25AD%25E5%25AE%259A1.png)
> ▲ Cura 介面

開啟 Cura 後，在右側是列印的參數設定，請將「列印設定」由「推薦」改成「自訂選項」，並修改其中的設定值如下：

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
>   - 方法 2：將滑鼠移動到該參數群組（如速度、冷卻）的箭頭左邊，會顯示一個齒輪的圖案，點擊就會顯示「參數顯示設定」視窗，將沒有顯示的參數設定在此清單勾選起。
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

[![](https://1.bp.blogspot.com/-AwqCQbbow1I/YFn1Flf4EII/AAAAAAAAAW4/A_X4116ATW4KTTmszFDk8qDlqfgI6UalQCPcBGAsYHg/w640-h376/04-Cura%25E5%2588%2587%25E7%2589%25871.png)](https://1.bp.blogspot.com/-AwqCQbbow1I/YFn1Flf4EII/AAAAAAAAAW4/A_X4116ATW4KTTmszFDk8qDlqfgI6UalQCPcBGAsYHg/w640-h376/04-Cura%25E5%2588%2587%25E7%2589%25871.png)
> ▲ Cura 的分層檢視

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
使用「驗收-1」所繪製的 AX-12 馬達 3D 模型，再自行繪製其支撐零件，設計一個帶夾爪的機械手臂。並利用雷射切割機或 3D 列印機將零件製作出來，並完成組裝。

夾爪與機械手臂的結構不限（關節式、SCARA），但應要有辦法完成「驗收-4」的要求。

> 組裝時會用到螺絲，請將所有用到的螺絲規格（如 `M2×10mm`）列表記錄，以方便之後拆解完可以將螺絲按照正確的規格分類。

# 階段三
## Robotis 套件

### RoboPlus Manager
拿出一台「CM-530」控制器及至少一顆「AX-12」馬達，並使用傳輸線連接。「CM-530」使用 USB 線連接電腦，接上電源並開啟。

[![](https://1.bp.blogspot.com/-KLyF24RRlCA/YFwZQQzBexI/AAAAAAAAAfI/zHGCvbyp8cUegHPTCGWP7GrsAmfNpAJJQCPcBGAsYHg/w400-h299/MX530.png)](https://1.bp.blogspot.com/-KLyF24RRlCA/YFwZQQzBexI/AAAAAAAAAfI/zHGCvbyp8cUegHPTCGWP7GrsAmfNpAJJQCPcBGAsYHg/w400-h299/MX530.png)
> ▲ CM-530

打開「RoboPlus」程式，在中間的標籤頁中選擇「BIOLOID」，再點選「RoboPlus Manager」即會開啟新的視窗。

[![](https://1.bp.blogspot.com/-NrjL7EmsBL8/YFwZQRNncuI/AAAAAAAAAfI/zlktxG81QqcmCJUA5UF1wDcGbjiUEg6GwCPcBGAsYHg/s16000/%25E6%2593%25B7%25E5%258F%2596.PNG)](https://1.bp.blogspot.com/-NrjL7EmsBL8/YFwZQRNncuI/AAAAAAAAAfI/zlktxG81QqcmCJUA5UF1wDcGbjiUEg6GwCPcBGAsYHg/s16000/%25E6%2593%25B7%25E5%258F%2596.PNG)
> ▲ RoboPlus 程式

「RoboPlus Manager」視窗中，點擊左上角的下拉式選單來選擇「CM-530」的COM Port，實際的 COM Port 請使用 Windows 的「裝置管理員」得知，或直接選擇「Auto Search」。完成後就可以按下旁邊的「Connect」按鈕進行連線。

[![](https://1.bp.blogspot.com/--1lPrJ4TLlI/YFwZQQSyDrI/AAAAAAAAAfI/W4CTYcriRhcmcD4LtH15Ap_gpR-9jmwqQCPcBGAsYHg/s16000/RP-COM.png)](https://1.bp.blogspot.com/--1lPrJ4TLlI/YFwZQQSyDrI/AAAAAAAAAfI/W4CTYcriRhcmcD4LtH15Ap_gpR-9jmwqQCPcBGAsYHg/s16000/RP-COM.png)
> ▲ RoboPlus Manager 頁面

連線成功後就會在左側列出所有找到的裝置。

[![](https://1.bp.blogspot.com/-m_1ViZJsmRs/YFwZQWqUQPI/AAAAAAAAAfI/O1eDZgPS6Sk8gjqylhBmEh0ZdvILIj2KACPcBGAsYHg/s16000/RP-Connected1.png)](https://1.bp.blogspot.com/-m_1ViZJsmRs/YFwZQWqUQPI/AAAAAAAAAfI/O1eDZgPS6Sk8gjqylhBmEh0ZdvILIj2KACPcBGAsYHg/s16000/RP-Connected1.png)
> ▲ RoboPlus Manager 連線成功

AX-12（或其它 AI 馬達）有兩種操作模式：Joint（關節）與Wheel（輪子）。正如其名，「關節模式」適合用於機器人關節，它使用角度位置來進行控制；「輪子模式」適合用在車輪等持續旋轉的地方，使用轉速及方向控制。

「關節模式」的角度範圍為：`0° ~ 300°`，對應的數值為：`0 ~ 1023`。中心點在 `150° (512)`。預計要使用「關節模式」來進行組裝的話，請記得在組裝前先將其轉到中心點。

在「RoboPlus Manager」視窗的右上角選擇「Joint」，在中間區域點選「Goal Position」就可以進行「關節模式」的控制。

[![](https://1.bp.blogspot.com/-onR6Fm_Fn0k/YFwZQa-88pI/AAAAAAAAAfI/fBvNWGtg2IAVk6BHGyZXbDb9E01BjLC6wCPcBGAsYHg/s16000/RP-Connected3.png)](https://1.bp.blogspot.com/-onR6Fm_Fn0k/YFwZQa-88pI/AAAAAAAAAfI/fBvNWGtg2IAVk6BHGyZXbDb9E01BjLC6wCPcBGAsYHg/s16000/RP-Connected3.png)
> ▲ 關節模式控制頁面

「輪子模式」可以 `360°` 連續不斷地旋轉。並且可以控制方向為「CW（順時針）」或「CCW（逆時針）」。旋轉速度的數值範圍為：`0 ~ 1023`，數值為 `0` 代表停止轉動。

在「RoboPlus Manager」視窗的右上角選擇「Wheel」，在中間區域點選「Moving Speed」就可以進行「輪子模式」的控制。

[![](https://1.bp.blogspot.com/-1j9aCzzWjI0/YFwZQX8-fII/AAAAAAAAAfI/nDdeqI7pNdczM6KYbvhsH5AriKAC1go_QCPcBGAsYHg/s16000/RP-whell.png)](https://1.bp.blogspot.com/-1j9aCzzWjI0/YFwZQX8-fII/AAAAAAAAAfI/nDdeqI7pNdczM6KYbvhsH5AriKAC1go_QCPcBGAsYHg/s16000/RP-whell.png)
> ▲ 輪子模式控制頁面

使用完「RoboPlus Manager」記得點擊「Disconnect」進行斷線，否則「CM-530」會被它佔用，導致其它程式沒辦法使用「CM-530」。



## [驗收-3] 以 Robotis 套件控制機械手臂
使用 Robotis 套件來控制「驗收-2」所設計的機械手臂。要求僅需要進行簡單的動作控制，只要能看出可以控制馬達即可。

開啟RoboPlsu，選擇上方的BIOLOID，並選擇RoboPlus Task。
[![](C:\Users\lab\Desktop\Train\RoboPlusTask.png)
>RoboPlus Task介面

於任意一行點擊兩下進行版本選擇，選擇Firmware Version 1.0的CM-530。
[![](C:\Users\lab\Desktop\Train\Version.png)
>版本選擇

選擇完版本後，於最上面一行點擊兩下開始進行程式撰寫。
首先為`START PROGRAM`為程式伊始，必須要有。而END PROGRAM則未必要有，通常會接著`ENDLESS LOOP`做永不中斷的迴圈執行動作。
IF判斷式則為判斷式，使用方法為

# 階段四
## C# 入門
### 使用程式控制馬達

準備通訊轉換器、馬達、電源套件、12V變壓器、2條3Pin線。
[![](C:\Users\lab\Desktop\Train\Necessary_Device.png)]
> 範例套件
並如下圖連接。
[![](C:\Users\lab\Desktop\Train\Connect.png)]
> 連接方式

確認通訊轉換器的模式，AX / MX 系列使用TTL模式，DX / RX / EX / MX系列使用RS485模式。
本例使用AX-12A+馬達，因此為TTL模式，如果選擇錯誤則會導致後續失敗。
[![](C:\Users\lab\Desktop\Train\CommunityTR.png)]
>模式選擇的開關

確認連接正確，接上電腦並確認COM Port後，開啟RoboPlus於上方選擇Expert模式並點選`Dynamixel Wizard`。
[![](C:\Users\lab\Desktop\Train\Dynamixel Wizard UI.png)]
>開啟Dynamixel Wizard的介面

選擇COM Port並點選Start searching尋找馬達，成功連接後獲取ID與鮑率。

[![](C:\Users\lab\Desktop\Train\NeedKnow.png)]
>馬達的ID與鮑率

### 撰寫程式封包
實驗室透過撰寫[`ROBOTIS Protocol 1`](https://emanual.robotis.com/docs/en/dxl/protocol1/)協定封包，達成馬達控制。

此封包必須包含以下幾項(`皆為Byte型態`)：
1. 兩個標頭 (0xff)
2. 馬達id
3. 封包長度 (參數+3)
4. 封包指令 ([指令表](C:\Users\lab\Desktop\Train\Action_List.png))
5. 指令數據起始位置 ([AX-12A](https://emanual.robotis.com/docs/en/dxl/ax/ax-12a/#control-table-of-eeprom-area))
6. 參數 
7. 校驗碼 ([算法](C:\Users\lab\Desktop\Train\CheckCode.png))

>透過(第5點)指令位址來判斷指令有幾位元。Goal Position 與 Moving Speed皆為2Byte

### 以C#為例

開啟Visual Stduio，新增C#新專案，並於兩側ToolBox中新增Serial Port，並修改COM Port與鮑率。
[![](C:\Users\lab\Desktop\Train\SerialPort.png)]
>新增專案與Serial Port。

[![](C:\Users\lab\Desktop\Train\NeedKnow.png)]
>控制`Goal Position`與`Moving Speed`的程式碼。

此程式碼宣告了byte[] data陣列
1. data[0]、data[1]為0xff標頭
2. data[2]為馬達id
3. data[3]是封包長度7，有4個參數(Postion 2個與Speed 2個)+3
4. data[4]為0x03表示寫入的意思
5. data[5] 0x1e代表從十進制30(即Goal Position)開始寫入。`注意為2Byte因此需要寫兩格`
6. data[6]為寫入Goal Position之**低位元**。
7. data[7]為寫入Goal Position之**高位元**。
8. data[8]為寫入Moving Speed之**低位元**。
9. data[9]為寫入Moving Speed之**高位元**。
10. data[10]為計算校驗碼。

撰寫完成封包後，透過SerialPort做傳輸。


到實驗室的 GitHub 下載 AX-12 馬達控制程式。連結：[nfu-irs-lab/AX12_motor_controller](https://github.com/nfu-irs-lab/AX12_motor_controller)

在 GitHub 頁面上點擊「Code」，再點擊「Download ZIP」即可下載程式碼。

> 如果你已經會使用 Git 的話，可以使用你自己習慣的方式來取得此程式碼。

[![](https://1.bp.blogspot.com/-A41nPy0eULA/YFwSl_OYOrI/AAAAAAAAAdI/5inEvp7YqrIMq3HSwm8XX1PHz89H_LQDQCPcBGAsYHg/w1684-h1069-p-k-no-nu/github-%25E4%25B8%258B%25E8%25BC%2589.png)](https://1.bp.blogspot.com/-A41nPy0eULA/YFwSl_OYOrI/AAAAAAAAAdI/5inEvp7YqrIMq3HSwm8XX1PHz89H_LQDQCPcBGAsYHg/w1684-h1069-p-k-no-nu/github-%25E4%25B8%258B%25E8%25BC%2589.png)
> ▲ 在 GitHub 上下載 AX-12 控制程式

使用 [Visual Studio](https://visualstudio.microsoft.com/) 來開啟「AX12_motor_controller.sln」檔案，就可以開始編寫程式。Visual Studio 可以安裝免費的 Community 版就好。

## [驗收-4] 以 C# 控制機械手臂
使用 C# 撰寫一個視窗程式，自行設計其圖形介面，並可以用來控制「驗收-2」所設計的機械手臂。

要求動作為，以圖形介面操控機械手臂及其夾爪，從「位置-A」夾取目標物（如空寶特瓶），並將其放到「位置-B」。位置 A 與 B 視情況由學長指定。

# 整理與收拾

當所有驗收都完成後，請將組裝的機械手臂拆解，將螺絲、馬達、電線等零件和工具物歸原處，打掃工作環境並整理乾淨。全部都完成後告知學長並確認後，才算是正式結束新進人員訓練。
