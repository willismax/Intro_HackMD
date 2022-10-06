---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 24 : HackMD 與 本機 VS Code 協作

[![Yes](https://img.youtube.com/vi/rWYo4lArW7I/0.jpg)](https://www.youtube.com/watch?v=rWYo4lArW7I)



- 一般來說我們都很習慣HackMD在線上編輯與共筆，其實用[VS Code](https://code.visualstudio.com/)在自己的電腦安裝插件後，就可以進行某程度的互動，今日來跟大家介紹。

## 本機電腦可以一鍵下載所有筆記
- 在眾多筆記平台中，HackMD一鍵下載所有筆記是最乾脆的，有些平台會不希望您離開他。
- 在 HackMD 的編輯介面點選 HackMD 圖示，到我的空間左下方的選單，選擇設定。
- 在設定裡選擇筆記設定，下載所有筆記即可。
- 下載的檔案是`.zip`壓縮檔，解開來會是一篇篇的`.md`檔案。
    ![](https://hackmd.io/_uploads/Sy7uU0tfi.png =500x)

## VS Code 與 HackMD 檔案互動

### 用途1. 從本機開啟解壓縮的資料夾
- 該資料夾全都是以 MarkDown 語法編輯筆記
- 此方法只是下載了 HackMD 檔案，本地編輯與網頁檔案不同步。
  ![](https://hackmd.io/_uploads/rJzG9v9zo.png =500x)
  ![](https://hackmd.io/_uploads/SJvLqPqzs.png =500x)

### 用途2. 安裝 VS Code 的 HackMD 套件
- 在 VS Code 擴充套件搜尋 [HackMD - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=HackMD.vscode-hackmd)套件，安裝即可。
    ![](https://hackmd.io/_uploads/HkP60D9Gj.png =500x)

- 點選左邊側欄有 HackMD 圖示，登入 HackMD 後完成連線，可閱覽 HackMD 編輯歷史資料，也可以雙欄預覽。  
    ![](https://hackmd.io/_uploads/rJZHJOqfo.png =500x)
    ![](https://hackmd.io/_uploads/Sk4WN_qMj.png =500x)

- 可是可是可是無法直接編輯 HackMD 筆記，只能預覽。




### 用途3. VS Code命令列指令建立新筆記、建立新程式碼筆記
- 依據官方[可用命令列指令](https://hackmd.io/@docs/vscode-hackmd-release-notes)的資訊，VS Code 安裝 HackMD 外掛後，在"命令列選擇區"有`HackMD: Create note from editor`及` HackMD: Create a code snippet`兩個新指令。
- 呼叫"命令列選擇區"的方式，可以用滑鼠右鍵選擇，或以快捷組合鍵`ctrl + shift + p` 呼叫。

#### 從編輯器建立HackMD筆記:
- 在 VS Code 之中的任一檔案，用命令區執行指令`HackMD: Create note from editor`，即會依據檔案內容新建筆記，可以另開 HackMD 網頁確認。

    ![](https://hackmd.io/_uploads/HyhOeqczj.png =500x)
#### 選取程式碼建立程式筆記:
- 在 VS Code 選取要貼去 HackMD 的程式碼片段，用命令列執行`HackMD: Create a code snippet` 指令，即會新建程式筆記，可以另開 HackMD 網頁確認
    ![](https://hackmd.io/_uploads/r1O0gq9fj.png =500x)
 
> 分享[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-24)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!