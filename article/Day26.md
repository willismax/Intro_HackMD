---
author: Willis Chen
image: https://hackmd.io/_uploads/B1-u_uJZs.png
GA: G-CH7FZ71WRC
---

# Day 26 : HackMD API 來用 Python 串接吧

[![hackmd-github-sync-badge](https://hackmd.io/qRCTaNxJTxawRv3rkQFaTA/badge)](https://hackmd.io/qRCTaNxJTxawRv3rkQFaTA)



[![Yes](https://img.youtube.com/vi/s0ype_Q5mvs/0.jpg)](https://www.youtube.com/watch?v=s0ype_Q5mvs)




## [HackMD API](https://hackmd.io/@docs/HackMD_API_Book)
- 目前僅付費者可用，需在設定建立API Token。
- API每月有 2000 個呼叫的配額，速率限製為每 5 分鐘 100 個呼叫。
- 官方的[HackMD API BOOK](https://hackmd.io/@docs/HackMD_API_Book)持續徵求案例，有興趣可以解決Use Case或貢獻，像我也貢獻[用API批次修改文章權限(PyHackMD)](https://hackmd.io/@wiimax/ByK86oNJs)。
    - [HackMD User API](https://hackmd.io/@hackmd-api/user-api)
    - [User Notes API](https://hackmd.io/@hackmd-api/user-notes-api)
    - [Teams API](https://hackmd.io/@hackmd-api/teams-api)
    - [Team Notes API](https://hackmd.io/@hackmd-api/team-notes-api)

## [PyHackMD](https://github.com/GoatWang/PyHackMD)
- 由使用者順手建立的 Python 操作 HackMD API 套件。
- 將各種操作 API 的 CRUD 功能包成 Python 可用的介面，感恩。


## [PyHackMD 使用案例](https://github.com/GoatWang/PyHackMD)

- 安裝[Python](https://www.python.org/downloads/)
- 安裝PyHackMD
    ```
    !pip install PyHackMD
    ```
- 取得文章列表(以下案例皆在 [![](https://hackmd.io/_uploads/Bkg2FGifj.png)](https://colab.research.google.com/gist/willismax/eefb5ebe70b4e2c24ba6a6780e49fd62/pyhackmd.ipynb) 
執行)
    ```python
    from PyHackMD import API

    api = API(HACKMD_API_TOKEN)
    data = api.get_note_list()
    pprint(len(data))
    pprint(data[0]) #觀察第一筆資料
    ```
    ![](https://hackmd.io/_uploads/rJ0WULVyo.png)

- 以DataFrame取得前5筆資料
    ```python
    from PyHackMD import API
    import pandas as pd

    api = API(HACKMD_API_TOKEN)
    data = api.get_note_list()
    df = pd.DataFrame(data)
    df.head()
    ```
    ![](https://hackmd.io/_uploads/HyYBLU41s.png)

-  取得編輯權限非owner的筆記，並且全改成owner
    ```python
    from PyHackMD import API
    from pprint import pprint
    import time
    api = API(HACKMD_API_TOKEN)

    data = api.get_note_list()

    for note in data:
        if note['writePermission'] != 'owner':
            print(note['id'], note['title'], note['writePermission'])
            time.sleep(1)
            api.update_note( note_id=note['id'], write_permission = "owner")
            time.sleep(1)
            _ = api.get_note(note_id=note['id'])
            print(_['id'], _['title'], _['writePermission'])
    ```
    ![](https://hackmd.io/_uploads/rJGlshNJs.png)


- 刪除名稱未定義，內容為空的筆記
    ```python
    from PyHackMD import API
    from pprint import pprint
    import time
    api = API(HACKMD_API_TOKEN)

    data = api.get_note_list()
    for note in data:
        if (note['title'] == 'Untitled') :
            print(note)
            _ = api.get_note(note_id = note['id'])
            if _["content"] == "": 
                print(_['id'], _['title'], _["content"])
                api.delete_note(_['id'])
    ```

    ![](https://hackmd.io/_uploads/rkRJjDEJi.png)
    ![](https://hackmd.io/_uploads/r1DQowNks.png)

以上也貢獻在官方API use case - [用API批次修改文章權限(PyHackMD)](/i7dUe9PeRA2o8R9ngrAnaw)，另因為迴圈查找的關係，注意您的 API 請求數量有每月2000 個請求、每 5 分鐘 100 個請求限制。

> 分享[今日簡報](https://hackmd.io/@wiimax/intro-hackmd-26)，以及至今已公開的[所有簡報](https://hackmd.io/@wiimax/intro-hackmd-slides)，供您一次瀏覽!