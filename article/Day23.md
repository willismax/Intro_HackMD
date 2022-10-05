# Day 23 : HackMD 嵌入 Colab with Gist


[![Yes](https://img.youtube.com/vi/ecVj5DnKCCY/0.jpg)](https://www.youtube.com/watch?v=ecVj5DnKCCY)

## 為什麼需要 [Colab](https://colab.research.google.com/) 
- Colab (Colaboratory) 為Google 推出的雲端執行 Python 程式碼的服務，依據 Jupyter Notebook 的筆記本(以下稱筆記本)發展而來，可在瀏覽器中編寫及執行 Python 程式碼，並且可以透過 Linux 指令操作虛擬機（Colab 的虛擬機是採用 Linux 系統的 Debain，Ubuntu 大多數常用指令共用）。
- 筆者也是Colab的愛用者，在第12屆[用Line聊天機器人串起多媒體系統 ](https://ithelp.ithome.com.tw/users/20121130/ironman/3131)系列文[Day 10 : 左手只是輔助 - 用 Google Colab 協助開發日常](https://ithelp.ithome.com.tw/articles/10234527)之後，只要是分享Python實作的程式碼全都提供Colab連結，如果您對先前筆者的鐵人賽的Colab
實作有興趣，清單都在最後一天，像是第12屆的[Dya 30 : 完結灑花](https://ithelp.ithome.com.tw/articles/10242827)、2021年的 [從 AI 落地談 MLOps ](https://ithelp.ithome.com.tw/users/20121130/ironman/4015)系列的[Day 30 : 綜合整理 MLOps 成熟度模型](https://ithelp.ithome.com.tw/articles/10274317)。



## Colab的優點
- 不必進行任何設定
    - 可以直接瀏覽頁面，直接建立好可以執行程式碼的筆記本環境，登入Google帳號即可互動。
- 免付費使用
    - 目前免費服務提供12小時虛擬機執行時間、佛心的GPU資源，關閉視窗即停止虛擬機；付費版目前可運行至24小時、較優先的GPU資源、可重新訪問關閉視窗尚在執行的筆記本。
- 輕鬆共用
    - 如同Google文件系列的檔案共享方式，可以限制使用者與個別邀請、提供分享連結供檢視或編輯。


## 如何儲存您要的 Colab 檔案
您可以選擇以下方式
- 在 Google 雲端硬碟儲存
- 在 GitHub Gist 儲存
- 在 GitHub 儲存
- 在本機儲存為`.ipynb`
- 在本機儲存為`.py`
    ![](https://hackmd.io/_uploads/H1S1oTtfo.png)


## 在 HackMD 結合 Colab 的方法
### Colab 不能用`<iframe>` 嵌入
如果用HackMD的`<iframe>`嵌入或書本模式的外部連結，都不能直接嵌入，與 Google 的試算表、簡報與文件不同，是特別的存在。

### Colab 以超連結分享
- 可以用分享連結供使用者點選，另開視窗即可。
- 人人都會的[分享超連結](https://colab.research.google.com/gist/willismax/171dccff8e7ade253ea6ddad3ae262d4/-qrcode.ipynb)。

## Colab 以 Gist 用`{}`內嵌
- HackMD 針對嵌入 Gist 程式碼已有優化，所以要在 HackMD 嵌入 Colob ，不是存在 GitHub，而是存在 Gist 才行唷!
- [存至Gist以`{}`內嵌Colab](https://gist.github.com/willismax/171dccff8e7ade253ea6ddad3ae262d4)範例
  ![](https://hackmd.io/_uploads/H1pzywqGj.png)

    ```
    {%gist 171dccff8e7ade253ea6ddad3ae262d4 %}
    ```
- 結合`:::spoiler`切換展示效果
    - 收合
      ![](https://hackmd.io/_uploads/H1GhJw5Mo.png)
    - 開啟
      ![](https://hackmd.io/_uploads/B1sq1vczs.png)
        ```
        :::spoiler
        {%gist 171dccff8e7ade253ea6ddad3ae262d4 %}
        :::
        ```
- 附帶一提，如果 Colab 已經與 Gist 同步的話，您有修正 Colab 而儲存時，會自動更新 Gist 內容，非常方便唷!

> 也分享[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-23)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!