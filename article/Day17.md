---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 17 : 炫炮的 HackMD 簡報客製背景設定

[![Yes](https://img.youtube.com/vi/GYZH8LB_ees/0.jpg)](https://www.youtube.com/watch?v=GYZH8LB_ees)

- HackMD簡潔的簡報功能已經非常實用，今天要分享的是客製化背景，背景可以是另一種顏色、漸層、圖檔、動畫、影片，甚至是iframe，真的很扯，迫不及待分享給您。
- 今日簡報[Day 17 : HackMD 簡報客製背景設定-簡報](https://hackmd.io/@wiimax/intro-hackmd-17)，請搭配使用觀看動態效果。


## 設定單頁簡報背景  

- 設定簡報的各種特效為`<!-- .slide: -->`，參數可以接背景圖片的`data-background`，該參數可以給圖片網址、gif檔網址，就是一整個星爆。

    ```
    <!-- .slide: data-background="https://hackmd.io/_uploads/rkZ8MIjbi.png" -->

    ### 美美的背景
    ```
    ![](https://hackmd.io/_uploads/r1vYxkyzj.png)

- 如果用的是`.gif`背景，像是用了
  
  ![](https://hackmd.io/_uploads/rkVUwSoZi.gif)
  ![](https://hackmd.io/_uploads/SJq0ekkzj.png)

    ```
    # 大腦在星爆.gif
    ![](https://hackmd.io/_uploads/rkVUwSoZi.gif)

    <!-- .slide: data-background="https://hackmd.io/_uploads/rkVUwSoZi.gif" -->
    ```

## 設定影片當背景
- 在`<!-- .slide: -->`之中以`data-background-video`參數，提供`.mp4`的連結，就可以當作滿版的影片撥放，並且可以重複撥放的`data-background-video-loop`參數，以及靜音的`data-background-video-muted`參數，讓簡報更生動吸睛。
- 在範例影片中的前景仍可以寫文案，HackMD的`:::warning :::`語法也有支援，形成了一個文字底圖~
- 因為`.mp4`網址不好找，直接引用Revealjs的簡報背景影片如下(後續會使用Google雲端硬碟的解法，再請拭目以待)。
    ![](https://hackmd.io/_uploads/HyBwGyyzj.png)

    ```
    <!--.slide:data-background-video="https://static.slid.es/site/homepage/v1/homepage-video-editor.mp4" data-background-video-loop data-background-video-muted  -->

    :::warning
    ## <font color="#003366">背景嵌入影片</font>
    :::
    ```

## 設定iframe當背景
- 同理在`<!-- .slide: -->`之中，改以`ata-background-iframe`參數的話，該連結就是一個滿版的iframe嵌入，加上`data-background-interactive`參數就可以與iframe互動。
- 以下為影片中示範滿版iframe的畫面，但濫用iframe除了不利於SEO搜尋，也容易讓使用者混淆，請警慎採用。
    ![](https://hackmd.io/_uploads/HyEhmykfj.png)

    ```
    <!--.slide:data-background-iframe="https://hackmd.io/@wiimax/Bk0dCIiWs/edit"
     data-background-interactive preloadIframes  -->

    :::danger
    ## <font color="#003366">沒事不要用滿版的背景iframe</font>
    ## <font color="#003366">太容易混淆有資安風險</font>
    :::
    ```

## 最後不妨去看看Reveal.js的功能吧
- [revealjs簡報 DEMO](https://revealjs.com/demo/?parallaxBackgroundImage=https%3A%2F%2Fs3.amazonaws.com%2Fhakim-static%2Freveal-js%2Freveal-parallax-1.jpg&parallaxBackgroundSize=2100px%20900px)，程式碼在此。
- 也提醒您Reaveal.js的語法都是以`<session></session>`包起來，在HackMD的簡報中您改用`<!-- .slide: -->`包起來即可。


大腦在星爆~~

> 提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-17)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!
