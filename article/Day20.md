---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 20 : HackMD 嵌入 iframe 運用

[![hackmd-github-sync-badge](https://hackmd.io/6-ZXlkVtTIG61mxjIdNprQ/badge)](https://hackmd.io/6-ZXlkVtTIG61mxjIdNprQ)


[![Yes](https://img.youtube.com/vi/h1xCGrrCFJE/0.jpg)](https://www.youtube.com/watch?v=h1xCGrrCFJE)


大家好，今日特別將 HackMD 嵌入 `<iframe>` 的用途整理與示範，也特別整理在公開場合DEMO時的嵌入版型，建議閱讀時配合此[HackMD 示範](https://hackmd.io/@wiimax/iframe-demo)服用。

## HackMD 嵌入 Slido
- HackMD 嵌入 Slido 是常見的做法，像是 [PYCON 2022](https://hackmd.io/@pycontw/2022/)，各議軌預先製作了共筆連結與Slido留言互動區，是可以跨越時空合作的絕妙組合。
- 在使用`<iframe>`語法時，除了替換`src`屬性的網址，另外我常會將寬度改為`width="100%"`滿版呈現，較能兼顧在行動裝置上的呈現。
  ![](https://hackmd.io/_uploads/Sy0uCgwzi.png)

    ```
    <iframe
      src="https://app.sli.do/event/1WNiGw9ubYFtZ7iUcjt4KL" 
      frameborder="0"
      width="100%" 
      height="600" >
  </iframe>
    ```

## `<iframe>`在簡報的運用
- 透過`<iframe>`嵌入的頁面可以互動的特性，會比靜態的簡報讓觀眾更有參與感，此時用 slido 可以留言，也可以嵌入 HackMD 做更彈性的互動。
- 您可以配合本日的[HackMD 示範](https://hackmd.io/@wiimax/iframe-demo)，改以剪報模式檢視示範效果。
- 以下是 `Slido + QRcode + 縮網址 + 超連結` 的組合示範，觀眾如果是在大講堂的場地，可以掃描 QRCode 或輸入縮網址參與，如果已取得簡報，觀眾可以自行點選超連結操作，考慮多種互動情境。
- 以下是透過 HackMD 表格的方式完成雙表格排版，一邊是`<iframe>`，一邊是QRCode與縮網址(QRCede與縮網址中間以2個空白達到換行效果。
  ![](https://hackmd.io/_uploads/B1s--WDGo.png)

    ```
    |<iframe src="https://hackmd.io/@wiimax/H16p-nGGo/edit" frameborder="0" width="600" height="400" ></iframe>|![](https://hackmd.io/_uploads/rkvVz2MMi.png)  ppt.cc/feipNx|
    |:-:|:-:|
    ```
- 同理，HackMD 裡用`<iframe>`嵌入 HackMD，以可以用表格達到`共筆 + QRcode + 縮網址 + 超連結`的組合運用。
  ![](https://hackmd.io/_uploads/ryC8GZwGj.png)
    ```
    |<iframe src="https://hackmd.io/@wiimax/intro-hackmd-slides" frameborder="0" width="600" height="400" ></iframe>|![](https://hackmd.io/_uploads/BJn0i2fzi.png )  ppt.cc/fD1uqx|
    |:-:|:-:|
    ```
- 最後，如果要滿版的嵌入`<iframe>`在簡報裡，使用簡報的`<!--.slide:data-background-iframe -->`屬性設定，亦即背景嵌入`<iframe>`，前景仍可以用MarkDown語法寫字。
  ![](https://hackmd.io/_uploads/ry9TMZPMi.png)
    ```
    <!--.slide:
      data-background-iframe="https://hackmd.io/@wiimax/H16p-nGGo/edit" 
      data-background-interactive 
      preloadIframes 
      -->
    ```
    
## 嵌入`<iframe>`注意事項
- 優點是可以彈性整合各資源
- 缺點是會增加頁面載入速度、消耗記憶體資源、不利搜索引擎檢索。以自己的使用經驗，`<iframe>`的簡報會獨立一份，減少崩潰風險。



> 提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-20)
> ，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!
