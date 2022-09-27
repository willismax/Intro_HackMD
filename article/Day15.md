---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 15 : HackMD 簡報 YAML 設定

[![Yes](https://img.youtube.com/vi/T4m8xRQ46WQ/0.jpg)](https://www.youtube.com/watch?v=T4m8xRQ46WQ)


- 今日簡報[Day 15 : HackMD 簡報 YAML 設定-簡報](https://hackmd.io/@wiimax/intro-hackmd-15)

今日會將所知道的YAML檔案一次羅列，方便您自行調整合適的設定。

## 簡報模式的 YAML 檔
- 簡報模式可透過YAML檔，修改動畫與設計，一樣在文件的第一行開頭開始用YAML撰寫設定。
- 簡報過場特效為`slideOptions:\  transition:`，分別有`none, fade, slide, convex, concave, zoom`這些可用特效。
- 簡報主題為`slideOptions:\  transition:`，分別有`white, black, league, beige, sky, night, serif, simple, solarized, blood, moon`等主題。
    ```
    ---
    slideOptions:
      transition: slide #[none, fade, slide, convex, concave, zoom]
      theme: league #[white, black, league, beige, sky, night, serif, simple, solarized, blood, moon]
    ---
    ```


## 簡報修改動畫與設計
- 影片所使用的範例[DEMO](https://hackmd.io/@wiimax/r1eK3r8nq)
- 樣式表參見
    - [Reveal.js](https://revealjs.com/themes/)
    - [YAML metadata 說明 | HackMD](https://hackmd.io/@hackmd/N1tNqMEOl)


## 簡報YAML設定
- 羅列有蒐集到可用的YAML參數，註解`#`之後的說明文字不會執行。
    ```
    ---
    title: 文件標題
    description: 文件描述
    date: 2022-08-13
    langs: zh #見https://en.wikipedia.org/wiki/List_of_ISO_639-1_code
    dir: rtl #[rtl, ltr]右至左、左至右
    author: Willis Chen
    disqus: willismax #替換為您申請的disqus
    image: https://hackmd.io/screenshot.png #文件圖片，Twitter需1200:675才會預覽顯示
    tags: `tag1`、`tag2` #自訂標籤，優先於文內標籤
    GA: G-CH7FZ71WRC #自己申請的GA ID
    ---

    ```

您可以將本篇的YAML設定做為一個範本，日後使用時從範本建立文章，可以節省許多設定時間喔!

> 提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-15)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!
