---
title: "開始建立你的第一個 .net core網站啦!"
date: 2020-07-17T21:19:06+08:00
draft: false
tags: ["asp.net Core"]
---

介紹完基本環境的安裝之後，接下來就要介紹如何快速地建立一個專案啦，透過 .net core CLI 中提供的指令，可以很快速建立預設專案的指令，像是 MVC、Rozor Page、Web API或者Win Form都可以快速建立，所以我們不需要手動一行一行Key,這樣我還不累死XD，那接下來就來看看要怎麼操作啦。

關於指令參考可以看看微軟官網的說明哦([連結](https://docs.microsoft.com/zh-tw/dotnet/core/tools/dotnet-new#web-options))

## <font color=#008000>※</font> 建立專案
要建立專案的時候，我通常會先建立一個新資料夾來放我的程式，假設我放程式的路徑是在D槽的Program(這個是我自己建立的資料夾)，我會用終端機的指令來新增，因為比較快XD

<font color=yellow>◎</font> Windwos 可以使用 PowerShell來下指令哦，如果不知道的人，可以直接在你電腦的 ***開始*** 那邊搜尋就找得到囉

以下提供參考，斜線的不用複製
```powershell
cd D:\Program   //移動到D:\Program資料夾
md newProject   //建立新資料夾
cd newProject   //移動到目前目錄底下的newProject資料夾
```
以上就把要放專案的位置設定好啦，當然你也可以用介面的操作，把資料夾建好，然後再用 cd 指令移至資料夾底下，像是這樣

```powershell
cd D:\Program\newProject   //這樣就直接移動到要建立專案的地方囉
```

接下來就來新增一個網頁啦，先用一個基本的，輸入以下指令
```powershell
dotnet new web
```

接下來會出現以下訊息，代表安裝完囉!這裡不用操作 看一下就好XD

```powershell
$ dotnet new web
Getting ready...
The template "ASP.NET Core Empty" was created successfully.

Processing post-creation actions...
Running 'dotnet restore' on D:\Program\FirstdotnetCore\FirstdotnetCore.csproj...
  ▒▒▒b▒P▒_▒n▒٭쪺▒M▒▒...
  ▒w▒٭▒ D:\Program\FirstdotnetCore\FirstdotnetCore.csproj (142 ms ▒▒)▒C

Restore succeeded.

```

接下來只要打開你的資料夾就會發現一堆檔案囉!是不是超級快

![dotnewweb](https://i.imgur.com/J89FEBu.jpg)

## <font color=#008000>※</font> 開啟你的專案

再來要怎麼開啟專案呢，因為你目前就在此目錄，所以只要輸入以下指令

```powershell
code .
```
就會自動開啟你的vsCode啦!

左邊的位置預設就是你目錄的位置哦!這樣就可以開始編輯你的網頁囉

![code .](https://i.imgur.com/8TyL4n3.jpg)

然後為什麼我的右下角會出現 Debug Missing的提示呢，因為我有裝C#的Extension 如果遇到專案是需要Debug的就會跳出提示

## <font color=#008000>※</font> 要怎麼安裝C# Extension 呢?

只要移動到Extensions 並搜尋 C# 然後找到星星那個按下Install就會安裝了!

啊!抱歉，我的是已經安裝好了，所以沒有Install，但你們那邊會看到，放心按下去就對了
![dotnewweb](https://i.imgur.com/YDZcyIG.jpg)

接下來如果有跳出提示視窗就選擇"Yes"就對了XD

他就會自動幫你建立Debug的環境囉!

## <font color=#008000>※</font> 開啟網站

建立好Debug環境後，接下來只要按**F5**就會建立開始執行你的第一個網頁囉!

然後因為預設會把你的連線設定在Https 所以進去網頁的時候會有這個畫面

![localpage](https://i.imgur.com/hizj9L5.jpg)

這是因為你的本機端沒有憑證的關係才會出現這個

如果懶得設定本機憑證的話，只要點選 "<font color=#008000>進階</font>" -> "<font color=#008000>繼續前往 localhost 網站 (不安全)</font>" 


但覺得不安全訊息不好看的話，可以用指令建立你的憑證

```powershell
dotnet dev-certs https --trust
```
輸入完後會詢問你是否要安裝憑證，這時候點選"是"就會自動安裝了。

![InstallCertificate](https://i.imgur.com/jrwaDIM.jpg)

這時候再開啟網站，就會出現憑證囉!

![InstallCertificate](https://i.imgur.com/s1tr7CD.jpg)

好啦!終於把基礎的網站建立打完了，這樣是不是對開發網站又更了解一些了

接下來如果我有空的話會再介紹一些網頁的知識，讓你一步步把你理想中的網站建立完成哦!敬啟期待