---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 14. HackMD 設定 GA 沒什麼困難的

[![Yes](https://img.youtube.com/vi/IpgkQR9OXgg/0.jpg)](https://www.youtube.com/watch?v=IpgkQR9OXgg)

## [Google Analytics](https://analytics.google.com/)
- 知名的流量分析工具，透過嵌入專屬的追蹤碼，可以看到流量趨勢、分布、文章閱覽情形等視覺化圖表，能進一步了解網站的使用情形，也是SEO、行銷的工具。
  ![](https://hackmd.io/_uploads/HycoiSiZj.png =300x)
  ![](https://hackmd.io/_uploads/HJVVdSs-j.png)
  ![](https://hackmd.io/_uploads/SyL1cHjZj.png)
  ![](https://hackmd.io/_uploads/Hy9boHjbi.png)

- 可以免費使用，使用需先申請取得追蹤碼ID，您可以設定一個專門追蹤HackMD流量的ID。

## 在 HackMD 嵌入 GA 很簡單
- 只要在編輯區YAML檔加入`GA: [GA的ID]`即可，以下是我的GA，請改您自己的。
    ```
    ---
    GA: G-CH7FZ71WRC
    ---
    ```
- 也請留意編輯區的YAML都在第一行開始撰寫，以`---`包起來。

- 包起來就可以追蹤了，可以幫助您更了解HackMD文章的閱覽行為與使用情形，更多的運用您可以搜尋GA的相關教學。

在HackMD設定GA遠比自己網頁嵌入追蹤碼簡單，不妨大方地運用吧!