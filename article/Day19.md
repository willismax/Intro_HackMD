---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 19 : HackMD 內建嵌入筆記指令

[![hackmd-github-sync-badge](https://hackmd.io/18sNgzrnSqKbT5AiwCmKnA/badge)](https://hackmd.io/18sNgzrnSqKbT5AiwCmKnA)

[![Yes](https://img.youtube.com/vi/mt01yjpaM7M/0.jpg)](https://www.youtube.com/watch?v=mt01yjpaM7M)


本篇主要介紹如何使用HackMD的`{}`嵌入功能，提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-19)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽，另外本篇請配合服用[DEMO連結](https://hackmd.io/8I6h0XrKTUyZC0YAtOnleA)，實際體驗與比較`{}`、`<iframe>` 二者差異!


## 輸入`{}`會出現嵌入選項
![](https://hackmd.io/_uploads/BJx4TGxfi.png)


## 可嵌入類型DEMO
- PDF
- Figma
- Gist
- Speakerdeck
- Slidesure
- Vimeo
- Youtube



## `{}`嵌入與`<iframe>`嵌入比較
- 建議直接到HackMD介面了解，如[DEMO連結](https://hackmd.io/8I6h0XrKTUyZC0YAtOnleA)。

### Adobe 的 Figma 
- 把Figma可分享的連結取代`{%figma figmaurl %}`的`figmaurl`。
- `{%figma%}`可以正常顯示，`<iframe>`拒絕連線。

    ```
    https://www.figma.com/file/PNxLYmeFKvZz9G7DEwnI0o/Untitled?node-id=0%3A1

    {%figma https://www.figma.com/file/PNxLYmeFKvZz9G7DEwnI0o/Untitled?node-id=0%3A1 %}
    ```


### Gist
- 把Gist ID取代`{%gist gistid %}`的`gistid`。
- `{%gist%}`可以正常顯示，`<iframe>`拒絕連線。
    ```
    https://gist.github.com/willismax/2838f065f9b29099ea48a46afafb2216

    {%gist 
      2838f065f9b29099ea48a46afafb2216 
      %}
    ```


### PDF
- 把PDF網址代入`{%pdf pdfurl %}`的`pdfurl`。
- `{%pdf%}`、`<iframe>`皆可連線。
    ```
    https://doggy8088.github.io/A-Whirlwind-Tour-of-Python-zh-tw/

    {%pdf 
      https://doggy8088.github.io/A-Whirlwind-Tour-of-Python-zh-tw/ 
      %}
    ```


### Youtube

- 把 Youtube ID取代`{%youtube youtubeid %}`的`youtubeid`。
- `{%gist%}`可以正常顯示，`<iframe>`拒絕連線。
    ```
    https://www.youtube.com/watch?v=GOP4G21aNIg
    {%youtube 
      GOP4G21aNIg 
      %}
    ```


### HackMD

- 把編輯模式或分享連結的Note ID代入`{%hackmd noteid %}`的`noteid`。
- 編輯模式網址與分享模式網址，在`{%hackmd%}`都一樣，只會是網頁瀏覽的呈現。
- `<iframe>`可以隨著模式設定，分享為簡報、書本、預覽、編輯模式。
    ```
    //分享連結
    https://hackmd.io/@wiimax/intro-hackmd-17
    - {%hackmd /@wiimax/intro-hackmd-017 %}

    //編輯連結
    https://hackmd.io/i0LbXWybTTapFgAPEZbO9w
    - {%hackmd /@wiimax/i0LbXWybTTapFgAPEZbO9w %}
    ```
- 嵌入 `{HackMD}` 注意事項 
    - 不要嘗試貼自己本身的連結，無窮迴圈會拖累效能。
    - `<iframe>`才可以呈現想要分享的樣子(簡報、預覽、書本等)



## 小結
`{}`與`<iframe>`最大差異
- `{}`嵌入有優化
- `<iframe>`嵌入，部分JS失效
- `<iframe>`嵌入非常占用記憶體資源


> 提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-19)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!

