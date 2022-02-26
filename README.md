# 編輯紀錄


## 2022/1/31

>* **建立discord python Bot**
>
>* **將token, ping, random dice(本地圖片), Ame(網路圖片) 加入bot中**

- [x] 加入cog系統，以方便管理和更新(cog可以分類指令功能，亦可以reload, unload特定分類)  <<2022/2/1：已完成>>

- [ ] 預計下次分類成Entertain更詳細分類and Repl.it託管

_補充：上傳Github時記得更改資料夾名稱 以免洗掉紀錄_



## 2022/2/4

>* **成功在discord bot建立pixiv抓圖指令**
>
>* **成功建立基本功能 但尚未修復完全(如網頁error等條件等)**
>
>>之所以花那麼久時間 是因為卡在初始程式碼過於複雜 不易修復
>>
>>後來簡化後 便可以基本運作 但尚缺優化工作

- [ ] 預計下次作業優先優化pixiv系統 

- [ ] 有餘力將著手進行music bot

_補充：24hr託管似乎要花大量工程 預計全部程式碼告一段落 再著手進行_



## 2022/2/11

>* **增加 on_member_join 和 on_member_remove 訊息**
>
>>結果程式碼無論如何修改 都無法使終端機接收新成員的加入
>>
>>翻文許久才發現 程式碼前線 intents 尚未宣告加入 
>>
>>所以才會導致就算在 discord development 有開啟 SERVER MEMBERS INTENT 也無法偵測
>>
>>這次在 debug 上花了接近2小時 
>>
>>這提醒要先把先前條件設定好 不然無論怎麼優化 都無法達到預計結果
>>
>>也呈現出 debug 有待加強

- [ ] 加入訊息做設計優化 而不是只傳送文字提醒而已

_更正：先從discord api閱讀理解開始 有助於開發程式碼_



## 2022/2/16

>* **將上週的加入離開訊息單獨拉出來形成一個Cog 以方便日後維修**
>
>* **新增一個keyword偵測器 且將keyword list放置於json檔中 較為美觀且乾淨**
>
>>雖然目前可以偵測單一單字 但尚未能判斷句子是否有關鍵字
>>
>>理想狀態下 只要把鋸子切割並判斷即可 應該不難

_備註：pixiv優化似乎遇到困難 無法排除404錯誤回傳_

_不知能否從f12抓出錯誤_


## 2022/2/19

>* **優化關鍵字偵測到可以偵測句子內關鍵字**
>
>>基於某些指令在discord bot上有不同語法
>>
>>一樣花不少時間優化 看來熟悉discord bot api還是必須的
>>
>* **新增discord bot embed遷入訊息**
>
>>製作info導向Github網頁
>>
>>但因先前token在github上忘記刪除 
>>
>>所以把所有settings.json裡的token刪掉了


## 2022/2/20

>* **新增刪除文字行數**
>
>>方便在之後的spam重複傳遞訊息測試中清除版面
>
>* **新增Task.py執行Spam指令**
>* **新增set_channel指令 可以更換被刷平的平到ID**
>
>>希望下個版本加入datetime後 可以做成類鬧鐘設定
>>
>>每天固定一個時間傳送訊息

_備註：發現每一次丟token到Github時，Discord Bot都會自行更改一次token_

_下次丟備份時把token刪除 避免麻煩_


## 2022/2/26

>* **將Interval改寫成time_task**
>
>>修正為類鬧鐘模式 在指定時間傳送訊息
>>
>>修正為傳送文字一次 而不是在一分眾內傳送60次訊息
>
>* **新增time_set指令**
>
>>客製化鬧鐘提醒時間
>
>* **優化clear指令**
>
>>更人性化
>>
>>刪除訊息前 加入即將刪除訊息的提示 1秒鐘後連提示一併刪除 
>
>* **成功設置24hr託管**
>
>>配合Repl.it與UptimeRobot 成功託管
>>_(優先託管4.0版本 較為穩定_

