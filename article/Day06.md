---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 06 : HackMD 的簡報模式

[![hackmd-github-sync-badge](https://hackmd.io/nx6vw5mDSMKMBD4ZZ1ILHQ/badge)](https://hackmd.io/nx6vw5mDSMKMBD4ZZ1ILHQ)


[![Yes](https://img.youtube.com/vi/edLu-B7hPNA/0.jpg)](https://www.youtube.com/watch?v=edLu-B7hPNA)

今日簡報[Day 06 : HackMD 的簡報模式](https://hackmd.io/@wiimax/intro-hackmd-06)

## 分享為簡報模式
點選右上方選擇簡報模式，即可透過網址分享簡報。
![](https://hackmd.io/_uploads/SySgC07aq.png)

## 設定YAML檔
YAML檔描述請至於編輯文件的頂端，以下為預覽模式會顯示簡報渲染結果，有頁碼。

```yaml
---
slideOptions:
  slideNumber: true
type: slide
---
```


## 簡報的心法
- 注意力應該在人的身上
- 圖文只是輔助
- 大字流 
    - 字體大、數量多、速度快
    - 參考[《高橋流簡報術》](https://www.books.com.tw/products/0010457745)


## 用雙欄對照做圖文比較

|雙欄對照|雙欄對照
|:-:|:-:
|A|B
|C|D


## 分隔線作為主、次順序
- 主標題切換: 3個減號```---```當分隔線
- 次標題切換: 4個減號```----```當次分隔線
- 播放時`Esc`可以展示全部簡報layout
- 請留意分隔線，每個分隔的上一行/下一行請留白，參考如下
    ```
    ---

    ### 每個分隔的
    ### 上一行/下一行
    ### 請留白

    ---
    ```

## 編輯內容一樣用MarkDown語法
- 每點最多容納46個字元，也就是23個中文字
- 排版不見得盡如人意，留意呈現出來的結果
- 盡量不要超過三點

## 簡報的圖文排版需要留意是否超出
- 可附加屬性改善，例如下方圖片加上 `=450x`參數改善

    ```
    ![](https://hackmd.io/_uploads/r1PRPax-j.jpg =450x)
    ```


## 插入程式碼
- 單行使用`Esc`按鍵下方的\` \`。
    `print("hello HackMD")`

- 多行程式碼使用` ``` ``` `顯示的結果。
    ```
    print("hello HackMD")
    ```
- 多行程式碼可以塞到滿出來，會在簡報裡用卷軸滾動呈現不跑版。

## 製作圖表
- 表格遠不如簡報軟體靈活

    |左欄|右欄|
    |:-:|:-:|
    |適合對照|也不適合太多文字|

- 可以透過表格呈現圖文對照感覺
    |![](https://hackmd.io/_uploads/SkwzjCmaq.png)|![](https://hackmd.io/_uploads/rkYQoAm65.png)|
    |:-:|:-:|
    |說明1|說明2|


- mermaid等語法渲染圖可以在簡報模式呈現
    ```mermaid
    pie

    title 工程師的一天

    "吃飯" : 10
    "睡覺" : 30
    "打咚咚" : 60
    ```
    

    ![](https://hackmd.io/_uploads/B1gzITVZs.png)

> 提供[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-06)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!


勇於挑戰影片介紹著實不易，如有口誤及用詞不當得罪之處還請海涵
![/images/emoticon/emoticon16.gif](/images/emoticon/emoticon16.gif)



