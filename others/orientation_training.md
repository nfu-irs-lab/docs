# 新進人員訓練

推薦在 [HackMD](https://hackmd.io/@nfu-robot-lab/B1Sc0H7Ed) 上觀看。

## 目錄
- [實驗室環境介紹](#實驗室環境介紹)
  - [NAS（雲端）](#NAS雲端)
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
  - [[驗收-2] 自行設計並製作機械手臂](#驗收-2-自行設計並製作機械手臂)
- [階段三](#階段三)
  - [Robotis 套件](#robotis-套件)
  - [[驗收-3] 以 Robotis 套件控制機械手臂](#驗收-3-以-robotis-套件控制機械手臂)
- [階段三](#階段三)
  - [C# 入門](#c-入門)
  - [[驗收-4] 以 C# 控制機械手臂](#驗收-4-以-c-控制機械手臂)
- [整理與收拾](#整理與收拾)

> [回到主頁面](../README.md#文件)

---
# 實驗室環境介紹
## NAS（雲端）
實驗室的 NAS 地址為 `\\robothd`（不分大小寫）。於檔案總管上方的地址列輸入其地址就可以訪問，帳號與密碼請詢問學長。

# 階段一
## 3D 工業建模
###  軟體介紹
目前實驗室主要使用 [Onshape](https://www.onshape.com) 和 SolidWorks 來進行 3D 建模。

[Onshape](https://www.onshape.com) 可以免費使用，SolidWorks 需要付費使用，另外也可以選擇使用學校 E-mail（@gm.nfu.edu.tw）去申請 [Autodesk Inventor](https://www.autodesk.com.tw/products/inventor/overview) 的免費學術授權。

以下僅介紹 [Onshape](https://www.onshape.com)。其它軟體使用起來操作與概念相同、大同小異。

### 註冊 Onshape
進入 [Onshape](https://www.onshape.com/signup) 的註冊頁面，於下方的方案選擇「Public Maker Plan」（也可以使用學校帳號申請註冊「Education Account」）。

![](https://1.bp.blogspot.com/-NgzDc19D5Yg/YFRj9TNCxQI/AAAAAAAAAHs/ifkN-_mGGBQq2S7q-LzQXi4-HLUE96V_wCPcBGAsYHg/s1821/onshape-%25E8%25A8%25BB%25E5%2586%258A1.png)
> ▲ 選擇「Public Maker Plan」方案。

進入新的頁面後，點擊「Get Started」開始進行註冊。註冊帳號沒什麼特別要注意的，不過「What best describes you？」欄位可以選擇「Hobbyist / Maker」就好。

![](https://1.bp.blogspot.com/-6mWs7mYEC6Y/YFRnEp97-_I/AAAAAAAAAIw/xDkXwKi8eJsAi86yMlU-uvwpuNsSie4ZwCPcBGAsYHg/s666/onshape-%25E8%25A8%25BB%25E5%2586%258A2.png)
> ▲ 填寫註冊資料

完成註冊後就可以開始使用。

> - 註冊時可能會問你習慣的單位，請使用 MMGS 制：長度單位為 `Millimeter`、角度單位為 `Degree`、質量單位為 `Gram`。
> - 若有詢問習慣的滑鼠操作方式，請選擇「SolidWorks」。

### 建立檔案
> 以下內容之單位皆使用 MMGS 制。

登入 Onshape 並進到主頁面。點擊左上角的「建立」按鈕並選擇「文件」，來創建新的檔案。

![](https://1.bp.blogspot.com/-hBJMA7n1wWI/YFRpP1ESuyI/AAAAAAAAAJg/glYwCEGk14kDBs3C-_qCSPfLUINg0JtagCPcBGAsYHg/s1920/onshape-%25E4%25BD%25BF%25E7%2594%25A81.png)
> ▲ Onshape 主頁面

3D 工業建模的步驟大致如下，各個軟體都差不多：
1. 選擇一個目標平面作為起始平面。
2. 在起始平面上繪製 2D 草圖。
3. 選擇一個 2D 草圖來生成 3D 特徵。
4. 重複以上過程來增加更多的樣式。

![](https://1.bp.blogspot.com/-oELCi4ArEu8/YFRr7q4ihqI/AAAAAAAAAKg/kVHadamjFMEDKtzcZZZv-5xfSnR_SmsvACPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A82.png)
> ▲ 建模操作介面

以下示範動作時，可以注意右上角的視角姿態方塊，有注意瞭解目前畫面的視角。

### 繪製 2D 草圖

選擇平面「Top」來作為起始平面，並點選左上角的「草圖」來繪製草圖。在上方工具列中選擇「中心點矩形」，以平面為中心拉出矩形。大小尺寸還不用太精準。

![](https://1.bp.blogspot.com/-hvylk6miWRY/YFRtgfpBkvI/AAAAAAAAALM/FcRROM5JACM_yU-GsExaMSYCRurty9hlwCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A83.png)
> ▲ 繪製草圖

點需上方工具列的「尺寸」來點擊矩形的邊線，並指定該矩形的實際尺寸為長 100 mm、寬 50 mm。注意使用的是 MMGS 制，長度單位為毫米 mm。

在使用「尺寸」工具輸入數字時，可以直接使用基本的加減乘除運算。例如在輸入尺寸時可以直接輸入 `(100.5/2)+3.15`。

![](https://1.bp.blogspot.com/-h25sLJ_5JSg/YFRv9QM1IGI/AAAAAAAAAMQ/5m1_1PEimSQtBQWaDg9tOUrkV9lmbVR0gCPcBGAsYHg/s1833/onshape-%25E4%25BD%25BF%25E7%2594%25A84.png)
> ▲ 設定尺寸

點選左上角「草圖1」的綠色勾勾，完成此 2D 草圖。

### 生成 3D 特徵

選擇「草圖1」，並點選上方工具列的「擠出」。在擠出視窗中將「深度」設為 15 mm，點擊綠色勾勾來完成。

此時模型已經是 3D 的了。

![](https://1.bp.blogspot.com/-3Yjb1kbQQrk/YFRxvJre-lI/AAAAAAAAANA/GLnkraNhv5YdoSxtyzNpoGcZi83JM6AIACPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A85.png)
> ▲ 擠出

繼續點選「擠出1」長方體的頂面，再次新增草圖，並使用「中心點畫圓」與「尺寸」工具在此草圖的中心點畫一個直徑為 35 mm 的圓形。符號「Ø」代表該尺寸為直徑。

點選綠色勾勾來完成此草圖（草圖2）。

![](https://1.bp.blogspot.com/-1yQb4TyLiRE/YFRzzyaWc7I/AAAAAAAAANw/JffC0CpRHHk0G8fbFcipDSQRVnp04G_fwCPcBGAsYHg/s1838/onshape-%25E4%25BD%25BF%25E7%2594%25A86.png)
> ▲ 再畫一個圓形

選擇「草圖2」並點選「擠出」，在「擠出2」視窗中選擇「移除」，並選擇「完全貫穿」。完成此特徵。

此時原本的長方體中間會有一個圓形的洞，並且完全貫穿。

![](https://1.bp.blogspot.com/-7GBn7b-eg9g/YFR1b5OY-0I/AAAAAAAAAOc/Leppc9W4lNQFxUIkv0K3G41rtBlr9tTWgCPcBGAsYHg/s1832/onshape-%25E4%25BD%25BF%25E7%2594%25A87.png)
> ▲ 使用「擠出-移除」來挖空

### 複製-鏡射
有些特徵會重複出現，這時可以使用各種複製功能，就不用每個相同的特徵都要畫。

選擇長方體的側面（Z-X 面、前視），並新增一草圖。在此平面的短邊（Z 方向的邊線）的中心點位置旁邊新增一個「中心點畫圓」，並將圓的直徑設為 5 mm。

再使用「尺寸」工具依序點選圓心與短邊。將圓心到短邊的距離設為 8 mm。一般在設定圓的位置時會以圓心為基準，而不是使用圓周為基準，以圓心為基準的好處是改變圓的大小（直徑）時不會影響其位置。

完成此草圖（草圖3）。

![](https://1.bp.blogspot.com/-d8wqcC5achk/YFR5IQwHZ_I/AAAAAAAAAPg/EHXRNyCJ4HkzazKkfQpZ7Jfs5GUmS4HvgCPcBGAsYHg/s1842/onshape-%25E4%25BD%25BF%25E7%2594%25A88.png)
> ▲ 再畫圓

將草圖3使用「擠出-移除-完成貫穿」來挖空（擠出3）。

點選「鏡射」工具。在鏡射視窗上選擇「鏡射特徵」，「要鏡射的特徵」選擇「擠出3」、「鏡射平面」選擇「Right」（透過點擊左方的清單來選擇）。

點擊綠色勾勾來完成鏡射。

![](https://1.bp.blogspot.com/-Bl7UsR8aFGk/YFR7LUzhW6I/AAAAAAAAAQQ/CMP9a-c_myEjeOEOx0ZGt5HkPFS6EVEYgCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A89.png)
> ▲ 鏡射

### 複製-環狀複製排列
點擊長方體的頂面（Y-X 面、上視），新增草圖並在距離中心大圓孔（擠出2）20 mm（圓心中心距）的上面畫一個直徑為 3 mm 的圓。並完成此草圖（草圖4）。

![](https://1.bp.blogspot.com/-AuiSrFPCcVo/YFR9iTdhSqI/AAAAAAAAARA/xyTgwYsOkmsg757nEn-ctx7uBqHwFeofgCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A810.png)
> ▲ 畫圓

選擇「草圖4」並「擠出」，選擇「新增」並將深度設為 5 mm。完成此擠出（擠出4）。

點選「環狀複製排列」，並選擇「特徵複製排列」，「要複製排列的特徵」選擇「擠出4」、「複製排列軸」點選中心圓心（擠出2）的圓周、「實例數量」設為 3、勾選「同等間距」。完成此環狀複製排列。

![](https://1.bp.blogspot.com/-CuVV61MGwgA/YFR_C_LJTFI/AAAAAAAAARs/rkrAE-3bkj0ybgHINTbNmi4cSkMrG3OFwCPcBGAsYHg/s1836/onshape-%25E4%25BD%25BF%25E7%2594%25A811.png)
> ▲ 進行「環狀複製排列」

「線性複製排列」的操作概念與「環狀複製排列」差不多，請自行摸索並嘗試。

### 圓角與倒角

點選「圓角」。「要圓角的圖元」選擇前視的兩個長邊與兩個圓周。並完成圓角。

![](https://1.bp.blogspot.com/-xAeF-cuAacw/YFSBTuqa6dI/AAAAAAAAASg/ZNIWIiUvGBg3VDyywr31pMDTxznb2B_CQCPcBGAsYHg/s1835/onshape-%25E4%25BD%25BF%25E7%2594%25A812.png)
> ▲ 圓角

點選「倒角」。「要倒角的圖元」選擇後視的兩個長邊與兩個圓周。並完成倒角。

![](https://1.bp.blogspot.com/-3w_d2eEs4n0/YFSCHm_eSII/AAAAAAAAATI/zGSM59XGR90_s2RLckW7QgMY368YqDJEACPcBGAsYHg/s1830/onshape-%25E4%25BD%25BF%25E7%2594%25A813.png)
> ▲ 倒角

### 組合
點擊左下角的「+」來「插入新元素」，並選擇「Part Studio」。在剛剛新增的「Part Studio」（Part Studio 2）中繪製一個直徑為 35 mm、高度為 25 mm 的圓柱體。

在下方的元素列中點選「Assembly 1」（若沒有請自行新增）。點擊左上角的「插入」並選擇「Part Studio 1」，將其放置到畫面上。再選擇「Part Studio 2」放置到畫面上。點擊綠色勾勾完成插入。

在左側的清單中對「Part 1」（Part Studio 1）點擊滑鼠右鍵，並選擇「固定」。

![](https://1.bp.blogspot.com/-LRd2WO5H2dg/YFSEeWcGxWI/AAAAAAAAAT4/jlcHg8qI90UCX_EdB2Fw8XlMqcBcTZrSQCPcBGAsYHg/s1837/onshape-%25E4%25BD%25BF%25E7%2594%25A814.png)
> ▲ 插入零件

點選「滑動結合」。在「結合連接器」中選擇 2 元件的圓柱面。點擊綠色勾勾完成。

此時圓柱體可以在圓孔中滑動（Z 方向）。

![](https://1.bp.blogspot.com/-VRUvCG8dR-U/YFSG4DGZITI/AAAAAAAAAU4/ImVpfsLXuqAYLJ93sru_hznezfqJ4yD_ACPcBGAsYHg/s1836/onshape-%25E4%25BD%25BF%25E7%2594%25A815.png)
> ▲ 滑動結合

結合的方式有許多種，操作皆大同小異，請自行摸索練習。

## [驗收-1] 繪製馬達之 3D 模型

# 階段二
## 雷射切割機
## 3D 列印機
## [驗收-2] 自行設計並製作機械手臂

# 階段三
## Robotis 套件
## [驗收-3] 以 Robotis 套件控制機械手臂

# 階段四
## C# 入門
## [驗收-4] 以 C# 控制機械手臂

# 整理與收拾
