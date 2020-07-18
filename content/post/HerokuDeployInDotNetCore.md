---
title: "將dotnet Core 程式 部署到 Herku"
date: 2020-07-18T15:17:31+08:00
draft: false
tags: [
    "asp.net Core",
    "Heroku"
]
---

這裡來記錄一下，我是如何將寫好的網站部署到Heroku的，以下就開始教學啦

## <font color=#008000>※</font> 在Heroku建立新的App

進入到Heroku頁面後([連結](https://dashboard.heroku.com/apps))，在右上角點選 "New" -> "Create New App" 來建立一個新的站台

![HerokuCreateApp](https://i.imgur.com/Bn14XuB.jpg)

進去之後輸入站台名稱(這個只能輸入小寫哦)，區域的話我是選擇預設，之後就可以按Create App 建立站台囉

![CreateAppPage](https://i.imgur.com/lQB5C5E.jpg)

接下來就可以切換到指令來將程式上版上去囉!

這邊我是使用PowerShell 來上版，但要使用指令前，要先去下載 Heroku 的 CLI，這樣才能透過你的終端機來上版哦([下載網址](https://devcenter.heroku.com/articles/heroku-cli))

## <font color=#008000>※</font> 基本指令設定

先將你的位置設定到你程式的資料

```powershell
cd yourPath   //yourPath改成你的資料夾路徑
```
接下來就會開始使用到Heroku的指令囉

首先輸入以下指令，先登入你的Heroku

```powershell
heroku login
```

然後會出現一串文字，是告訴你 按 ***任何一個按鈕*** 打開網頁 或 按 ***q*** 離開

![HerokuPressKey](https://i.imgur.com/tDkp47o.jpg)

隨便按一個鍵後，會自動幫你開啟一個網頁

<img src ="https://i.imgur.com/9ktSCrc.jpg" alt = "HerokuCommandLogin" style ="height: 300px;">

這裡只要點Log In就好了，登入完之後就可以回去終端機，繼續使用指令操作了

---
接下來還需要加入Buildpack，因為Heroku預設是不會建置dotnet core這個程式的，所以需要引入第三方撰寫的Buildpack才可以建置，不然最後丟上去會失敗，在這邊我是引用[這個網站](https://elements.heroku.com/buildpacks/jincod/dotnetcore-buildpack)的Buildpack

這個網址裡面提到只要輸入以下指令，-a xxxxx 是選擇你要設定的站台名稱，Heroku就會幫你設定好這個第三方套件了

```powershell
heroku buildpacks:set jincod/dotnetcore -a xxxxx
```

## <font color=#008000>※</font> 將程式發布到Heroku

環境設定好之後就是git的一些指令操囉啦!

Heroku有三種上版方式可以使用，參考下圖

![HerokuDeployMethod](https://i.imgur.com/ai82mGb.jpg)

這次我是使用Heroku來將程式發佈上去

首先跟一般Git一樣建立一個新的儲存庫

```powershell
git init
```
接下來將你的儲存庫連接到你的Heroku站台， xxxxx 是你站台的名稱

```powershell
heroku git:remote -a xxxxx
```

最後就是每次更新程式都需要做的動作，也就是把現有程式丟到Heroku，有以下幾個指令

* 第一個是將資料加入索引
* Commit的話，是將資料提交上去並在 雙引號內輸入提交資訊
* 第三個就是把目前的程式退送到 Heroku啦!

```powershell
git add .
git commit -am "提交資訊"
git push heroku master
```

當這三個動作執行完後，Heroku就會自動把你的網站環境設定好

等它跑完之後，接下來就可以回到後台，如果有看到Build Succeeded的話就代表程式建置成功囉!

![DeploySucceeded](https://i.imgur.com/93hpZgI.jpg)

接下來就可以去點 "Open App" 去看你的網站了!

![OpenApp](https://i.imgur.com/b5xa29N.jpg)

這樣就成功把你的網站發佈到Heroku囉!

![WebDisPlay](https://i.imgur.com/UU0PzMY.jpg)