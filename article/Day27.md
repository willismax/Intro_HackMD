---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 27 : HackMD API 打造 LINE-BOT 賴爸特助 on Fly

[![hackmd-github-sync-badge](https://hackmd.io/r47voaIJS4iJ2VlZ_lXKdQ/badge)](https://hackmd.io/r47voaIJS4iJ2VlZ_lXKdQ)


[![Yes](https://img.youtube.com/vi/IXEn4PCr5P4/0.jpg)](https://www.youtube.com/watch?v=IXEn4PCr5P4)


## 用 "HackMD 賴爸特助"可以解決什麼問題
- 隨手筆記的需求
- 從不同APP分享連結的蒐集去處
- 不用再經手別的生產力工具，直接歸一到最熟悉的HackMD


## 建立 "HackMD 賴爸特助" 的流程
- 首先要有 [HackMD API](https://hackmd.io/@hackmd-api/developer-portal) ，目前為付費版的功能。
- 在 [LINE Developers](https://developers.line.biz/zh-hant/) 創一個專屬 Channel，取得Token等資訊與訊息設定。
- 在 Fly.io 創立雲端服務、建立好開發連線環境。
- Fork 我的[GitHub HackMD LINE bot on fly 程式碼](https://github.com/willismax/hackmd-line-bot-on-fly)，修改為您準備部屬在 Fly.io 的 LINE BOT 程式。
- 將您 Fly.io 的連結 `https://[APP Name].fly.io/callback`填入您LINE Channel 的 Webhook。
- 感動! 成功!。


## "HackMD 賴爸特助" 功能需求
- 標示`@靈感`為開頭的文字，將作為一個獨立的靈感筆記。
  ![](https://hackmd.io/_uploads/r1Vo7wRzo.png)

- 標示`@TODO`為開頭的文字，將寫入一個連續的的代辦清單。
  ![](https://hackmd.io/_uploads/HJHbEDAfo.png)

- 無上述標示的文字，將寫入一個連續附加的在暫存筆記。也就是從別的文章分享的超連結都直接灌到此暫存筆記。
  ![](https://hackmd.io/_uploads/HJbQNvRzi.png)

- 如果要整理筆記，用電腦編輯整理即可。



## 如何建立 LINE bot 
- 可以參考本人2年前寫的鐵人賽文章 [Day 12 : 以本機招喚 3 星鸚鵡 LINE Chat Bot - 1 (串起你的 LINE Message API )](https://ithelp.ithome.com.tw/articles/10234877)，在我的系列文 [用Line聊天機器人串起多媒體系統 ](https://ithelp.ithome.com.tw/users/20121130/ironman/3131) 多數程式都還可以用，只是部署環境改成 fly.io。

- 重要的是在 [LINE Developers](https://developers.line.biz/zh-hant/)
 登入您的 LINE 帳號，建立 Provider 以及所屬 Channel， Channel 名稱就是您的 LINE bot 名稱，管理方式如同 [LINE 官方帳號](https://tw.linebiz.com/login/)。

- 用程式控制的聊天機器人需要以下3個參數，請保管好勿外流。
  在此範例程式中，需要將 Channel 查到的以下參數填入`config.py`檔案。
    ```
    CHANNEL_ACCESS_TOKEN = ''
    CHANNEL_SECRET = ''
    LINE_USER_ID = ''
    ```

## 如何在 Fly.io 創立與部署服務

### 本機 Clone [Fly.io](http://fly.io/) 的 Python 示範專案。

-   前提是電腦需要[安裝git](https://git-scm.com/downloads)，安裝好在終端機使用git指令(git cli)，以下環境以windows示範，也請注意，這段文章說的是以 Fly.io 的範例程式做示範，與本篇文章要完成的 "HackMD 賴爸特助" 不一樣的程式，待您部署好範例再改即可。
    ```
    git clone https://github.com/fly-apps/python-hellofly-flask
    ```
    
-   進入專案資料夾
    
    ```
    cd  .\python-hellofly-flask\
    ```
    
-   安裝該專案所需的外部套件
    ```
    python -m pip install -r requirements.txt
    ```
    
-   如果要在本機進行開發測試，可以設置環境變數`FLASK_APP`，目的是指定主程式的執行檔，對此專案而言主程式為`hellofly.py`，經指定後`flask run`指定就是跑主程式，而且要結合 [Ngrok](https://ngrok.com/)建立臨時通道，對您來說太複雜的話可以跳過，只是各種測試就必須等待部署後。
    
    ```
    //設置環境變數
    export FLASK_APP=hellofly.py   #linux
    set FLASK_APP=hellofly.py   #windows
    ```
    
    ```
    //日後啟動flask的指令
    flask run
    ```
    
    !! 如果用環境變數都跑不出來，退而求其次，在`hellofly.py`最後加入:
    
    ```
    if __name__ == '__main__':
        app.run(debug=True)
    ```
    
    啟動flask指令改為`python hello.py`，請注意，[這不是flask現在建議的啟用方式](https://www.maxlist.xyz/2020/04/30/flask-helloworld/)，本方法只適用於本機測試。

### 使用`fly ctl` 指令工具完成部署

Fly.io 最方便部署服務的方式是使用終端機指令工具`flyctl`，可以讓本機直接部署。延續官方範例繼續流程。

-   [安裝flyctl](https://fly.io/docs/getting-started/installing-flyctl/)  
    PowerShell
    
    ```
    iwr https://fly.io/install.ps1 -useb | iex
    ```
    Mac
    ```
    brew install flyctl #MAC
    ```
    
    Linux
    
    ```
    curl -L https://fly.io/install.sh | sh #LINUX
    ```
    
-   [用 flyctl 登入 fly.io](https://fly.io/docs/getting-started/log-in-to-fly/)
    
    ```
    flyctl auth login
    ```
    
-   啟動一個 fly App 專案，執行 `flyctl launch`
    
    ```
    flyctl launch
    ```
    
-   選擇伺服器區域，最近的區域有香港、東京可選。
    
-   修改程式，這邊在範例專案中特別提醒，`Procfile`檔案為設定連線服務用，與您的主程式檔名務必相符，也就是原本為`web: gunicorn server:app`記得改成`web: gunicorn hellofly:app`，這原理跟部署在 Heroku 是一樣的。
    
    ```
    # file name: Procfile
    
    web: gunicorn hellofly:app  
                  ^^^^^^^^
    ```
    
-   檢查完程式後，一鍵佈署。
    ```
    flyctl deploy
    ```
    
-   查看佈署，其中`hostname`就是網址了，可以用`flyctl status`確認狀態、用`flyctl open`開啟 APP、用`flyctl logs`確認有無 BUG。
    
    ```
    flyctl status    
    ```
    ```
    flyctl open
    ```
    ```
    flyctl logs
    ```
    
-   如果需要[設定secrets](https://fly.io/docs/reference/secrets/)
    
    ```
    flyctl secrets set DATABASE_URL= ....
    ```
    
    取消 secrets
    
    ```
    flyctl secrets unset DATABASE_URL= ....
    ```
    
    列出 secrets list
    
    ```
    flyctl secrets list
    ```


## `HackMD 賴爸特助`[程式碼在此](https://github.com/willismax/hackmd-line-bot-on-fly)
>https://github.com/willismax/hackmd-line-bot-on-fly
- 可以對照您上述部署完成的`python-hellofly-flask`程式碼進行修改，填入對應的參數到`config.py`、修改`app.py`、`requestments.txt`等檔案，修正文執行`flyctl deploy`部署即可。請注意，`*.toml`請用您自己的，該檔案是由 `flyctl launch` 產生，為了您的專案部屬所需的檔案，用範例檔會出錯唷。
- 也請記得補上 HackMD API token 與筆記ID相關資訊:
    ```
    HACKMD_API_TOKEN = ''
    TODO_NOTE_ID = '' #  paste your fixed TODO note id, len == 22
    TEMP_NOTE_ID = '' # paste your fixed TEMP note id, len == 22
    ```

- 上述有問題的話就耐心看`flyctl logs`，我常作的方式是開兩個終端機，一個執行操作、一個看 log 。

- 部署完成後，記得把您的 fly.io 專屬服務網址貼入 LINE Channel 的 Webhook ，網址應為 `https://[APP Name].fly.io/callback` ，特別是 `*/callback` 記得填，並且設定開啟 Webhook。
- 如果都測試成功的話，恭喜您完成自己專屬的`HackMD 賴爸特助囉` ! 如您成功的話也讓我知道吧 !

> 分享[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-27)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!