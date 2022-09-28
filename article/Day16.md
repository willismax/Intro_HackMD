---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 16 : HackMD 簡報客製動畫設定

[![hackmd-github-sync-badge](https://hackmd.io/ht1jYfi-T_6XSOQJazruKw/badge)](https://hackmd.io/ht1jYfi-T_6XSOQJazruKw)



[![Yes](https://img.youtube.com/vi/oZcSrHm7QZA/0.jpg)](https://www.youtube.com/watch?v=oZcSrHm7QZA)

- 本篇分享讓您HackMD製作簡報更有彈性的動畫設定，包含依序出現的要點、圖片輪播功能，並且提醒您該注意的小細節。
- 今日簡報[Day 16 : HackMD 簡報客製動畫設定-簡報](https://hackmd.io/@wiimax/intro-hackmd-16)。

## 順續出現的動畫
- 使用`<!-- .element: class="fragment" data-fragment-index="1" -->`語法，就可以指定該行文字撥放的順序為1，如果要改順序，在`data-fragment-index="1"`的數字處更改。
- 如果該行文字中間有空格，則視為中斷，會造成不如預期的出現效果，所以建議都要預覽檢視效果。
- 文字中間的空格包含有序清單`1. `、無序清單`- `的空格，取消空格的話MarkDown會視為同段文字，但排版就會改成置中非靠左對齊的排版，使用時須有取捨，另外，請以**兩個空白鍵**作為文字換行。
    ```
    ## 順續出現的動畫(有序清單)
    1. 第一點<!-- .element: class="fragment" data-fragment-index="1" -->
    2. 第二點<!-- .element: class="fragment" data-fragment-index="2" -->

    ## 順序出現的動畫(改為置中)
    1.第一點<!-- .element: class="fragment" data-fragment-index="1" -->  
    2.第二點<!-- .element: class="fragment" data-fragment-index="2" -->  
    ```
    ![](https://hackmd.io/_uploads/Bk6KTRC-j.png)


----

## 圖片輪播範例
- 參考[Reveal.js 的 圖片layout範例](https://revealjs.com/layout/)，以下有3張貓咪圖片，配合圖片淡出`fade-out`效果，可以依序顯示圖片。

    ```
    <div class="r-stack">
      <img class="fragment fade-out" data-fragment-index="0" src="https://placekitten.com/450/300" width="450" height="300">
      <img class="fragment current-visible" data-fragment-index="0" src="https://placekitten.com/300/450" width="300" height="450">
      <img class="fragment" src="https://placekitten.com/400/400" width="400" height="400">
    </div>
    ```
    ![](https://hackmd.io/_uploads/S1h40ACZj.png)


介紹至今的技巧已經可以稱您為HackMD達人了，明天還有更酷炫的技巧唷。

> 提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-16)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!
