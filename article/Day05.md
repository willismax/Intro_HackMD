---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

[![Yes](https://img.youtube.com/vi/R72kNVUZdpg/0.jpg)](https://www.youtube.com/watch?v=R72kNVUZdpg)


# Day 05 : HackMD 與 MarkDown

## MarkDown前世今生
|![](https://i.imgur.com/K5IWBck.png)|![](https://i.imgur.com/hZ7kjYa.png)
|:-:|:-:
 - John Gruber 在 2004 年創造了 Markdown ，用以簡潔文字方案有效的轉為 HTML/XHTML


### MarkDown 為了簡化 HTML 而生
|MarkDown|HTML
|:-:|:-:
|# h1 | `<h1></h1>`
|- list | `<ul><li>Coffee</li></ul>`
|`![](圖片網址)` | `<img src="圖片網址">`
|`[](連結網址)` | `<a href="連結網址"></a>`


- [Markdown 語法說明](https://markdown.tw/)
- [Markdown -wiki](https://zh.wikipedia.org/wiki/Markdown)


### MarkDown語法無所不在
- HackMD也是以此語法為編輯基底，常用到的地方包含：
    - 編寫GitHub的`Readme.md`檔
    - 編寫Jupyter Notebook的文字描述
    - 技術部落格[Medium](https://medium.com/)
    - 筆記軟體Evernote等
    - Line的訊息也可以
    - iTHome鐵人賽!!!



### Markdown常用指令

# 標題H1 `#`
## 標題H2 `##`
### 標題H3 `###`
#### 標題H4 `####`



### 引用 `>`
> 在非洲，每過一分鐘，就有六十秒過去。[name=willismax]


### 清單 `-`、`1`
 - 無序清單：`*`、`+`、`-`
 - 有序清單：`1.`～`5.`
     - 不用在意數字的正確性，但最好從`1.`開始



### CheckBox

- [ ] 要做的事

`- [ ] 要做的事`


#### 縮排用4個空白或是1個`TAB`
- 第一排
    - 4個空白或1個tab縮排。
      第二行推齊可對齊。




#### 小數點
- `.`跟清單`1.`避免誤用，可以使用反斜線`\.`。
    - 如: `3.14`改為`3\.14


### 程式碼 - 單行
- 用一個鍵盤左方(Esc下方)的頓點符號包住

`print(Hello World)` 

### 程式碼 - 多行
- 多行程式用三個鍵盤左方(Esc下方)的頓點符號包住
- 可以選不同程式語言的高亮排版

```python=
print("hi")
```

```python
print("hi")
```

![](https://hackmd.io/_uploads/HJ0Kxnopc.png)



### HTML
`< >`可以產生HTML的效果
```
<div class="footer"> &copy; 2022 </div>  
```

<div class="footer"> &copy; 2022 </div>  



### 換行分隔線：
一行3個以上的下列符號皆可分隔
- `***`、`* * *`
- `---`、``---``
- `___`、`_ _ _`



### 超連結
- 使用`[連結名稱](網址)`，如`[markdown.tw](https://markdown.tw/)`，顯示結果為[我是超連結](https://markdown.tw/)


### 有alt說明的超連結
- 要游標移至超連結的說明，如`[markdown.tw](https://markdown.tw/ ' MarkDown中文教學')`
- 顯示結果為[滑我身上看看](https://markdown.tw/ ' MarkDown中文教學')



### 參考的連結
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"

```
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"
```

### 強調：以`*`或`_`包圍的文字

![](https://hackmd.io/_uploads/rJgdZ3jpc.png)

- 單個變斜體，如*斜體*、_斜體_
- 兩個變粗體，如**強調**、__強調__

## 圖片
`![Alt text](/path/to/img.jpg "Optional title")`

- 一般使用`![文字](連結)`即可使用
- 在HackMD貼上圖片，即在圖床上傳產生連結並顯示

  ![](https://i.imgur.com/rtaQxYP.png)
`![](https://i.imgur.com/rtaQxYP.png)
`

- 有調整尺寸的圖片
  ![](https://i.imgur.com/rtaQxYP.png =450x)
`![](https://i.imgur.com/rtaQxYP.png =450x)`

- 有調整尺寸、加上文字說明的圖片
![沒有圖的話會出現的文字](https://i.imgur.com/rtaQxYP.png "滑鼠游標在上方會顯示的提示文字" =450x)
`![如沒有圖的話會出現的文字](https://i.imgur.com/rtaQxYP.png =450x '如滑鼠游標在上方會顯示的提示文字')`



### 表格
- 預設靠左
    |編號|標題|說明|
    |-|-|-
    |1
- 表格-置中
    |編號|標題|說明|
    |:-:|:-:|:-:|
    |100|100|100

    ```
    |編號|標題|說明|
    |:-:|:-:|:-:|
    |100|100|100
    ```

- 表格-靠右
    |編號|標題|說明|
    |-:|-:|-:|
    |100|100|100

    ```
    |編號|標題|說明|
    |-:|-:|-:|
    |100|100|100
    ```

### MathJax
- 使用 **MathJax** 語法 來產生 *LaTeX* 數學表達式
- 符號表參見[此筆記](https://hackmd.io/@CynthiaChuang/Basic-LaTeX-Commands)[target=_blank]
$\sum_{i=1}^{n}(w_ix_i+b)$


## 更多參考教學
- [HackMD官方功能介紹](https://hackmd.io/features-tw?both)
- [官方進階功能](/c/tutorials-tw/%2Fs%2Ffeatures-tw)

## 小結
- 許多文書服務都有支援 MarkDown
- 饒過你排版的心思，專注在書寫上
- HackMD 共筆的重要功能，你得到他了!


以上會因為各種服務更新而有不同，為個人感受供參考。
勇於挑戰影片介紹著實不易，如有口誤及用詞不當得罪之處還請海涵
![/images/emoticon/emoticon16.gif](/images/emoticon/emoticon16.gif)