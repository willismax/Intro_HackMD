---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 28 : HackMD 客製佈景主題整理


[![Yes](https://img.youtube.com/vi/secZ4yhZmiQ/0.jpg)](https://www.youtube.com/watch?v=secZ4yhZmiQ)

- 您知道 HackMD 可以自製 CSS 模板，打造佈景主題嗎? 因為 HackMD 編輯內文時，可以透過`<style></style>`撰寫 CSS 模板，就可以打造自己風格的筆記樣式。
- 再加上 HackMD 可以透過 `{%hackmd noteid %}` 語法嵌入到不同的筆記裡，換言之，只要短短一行嵌入碼就可以改變您筆記的風格，達到如同個人部落格的效果。


## 在哪裡找主題?

- https://hackmd.io/@themes
- [官方說明](https://hackmd.io/c/tutorials-tw/https%3A%2F%2Fhackmd.io%2F%40docs%2Fhow-to-embed-note-2)
- 有意無意找到的網友版型
- 自製!!

## 主題介紹與範例

- Dark 佈景主題 
    - 在文件插入`{%hackmd BJrTq20hE %}`，來自@yukai、@MaxWu
    - 或`{%hackmd hackmd-dark-theme %}`，兩個效果不一樣，[DEMO](https://hackmd.io/@themes/dark-theme-preview)  
    ![](https://hackmd.io/_uploads/BJONuQ1Qi.png)

- Notion 佈景主題
    - `{%hackmd @themes/notion %}`，就會一副Notion樣，[DEMO](https://hackmd.io/@themes/demo-notion)  
    ![](https://hackmd.io/_uploads/Bk5IF7JQo.png)

- OrangeHeart 佈景主題 
    - `{%hackmd @themes/orangeheart %}`，[DEMO](https://hackmd.io/@themes/demo-orangeheart)  
    ![](https://hackmd.io/_uploads/BkgoK7Jmi.png)

- Dracula 佈景主題 
    - `{%hackmd @themes/dracula %}`，[DEMO](https://hackmd.io/@themes/demo-dracula)  
      ![](https://hackmd.io/_uploads/B1Os1Ey7j.png)

- Conversational 對話式佈景主題
    - `{%hackmd @yukai/conversational-theme %}`，[DEMO](https://hackmd.io/@yukai/conversational-theme-demo)
      ![](https://hackmd.io/_uploads/r1zmeE17j.png =550x)
    - 使用方法：
        - 文件插入 `{%hackmd @yukai/conversational-theme %}` 
        - 以 `---` 分隔線來區隔不同人的對話，分隔線後第一個段落會被當成講者。 
        - 兩行`---`+`---`分隔之後就不會變成對話。
        ![](https://hackmd.io/_uploads/B1qEeEJ7i.png)

- Medium 佈景主題
    - `{% hackmd @yukai/medium-theme %}` [DEMO](https://hackmd.io/@wiimax/rJUC9QJ7j)  
      ![](https://hackmd.io/_uploads/BJRuj7kms.png)

- 中文直書的主題
    - `{%hackmd SkPurArK4 %}` [DEMO](https://hackmd.io/hackmd-vertical-writing-theme?both)
    - 此主題僅供「預覽模式」看到最終成果，不能編輯+預覽喔~
      ![](https://hackmd.io/_uploads/BJMgkVy7o.png)


- [毛毛的前端筆記](https://hackmd.io/@JohnsonMao/Front-end):
    - [theme-Wood-Fired 原始碼](https://hackmd.io/EyHCJVyqSiWm6v9GjqDOZA?both)  
    - [theme-Night-Sidebar 原始碼](https://hackmd.io/dxywSXJPTUKkdVq4tJdIaQ?both)

- 如果要客製版型，可以參考上述的模板修改 CSS 樣式，可以玩得很開心唷!

> 分享[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-28)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!