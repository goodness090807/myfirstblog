---
title: "開始使用ASP.net core"
date: 2020-07-09T21:31:24+08:00
draft: false
tags: [".net Core"]
---

這篇主要紀錄 .net core的安裝流程 方便自己換電腦的時候來重新安裝，那我們就開始來今天的教學吧

## <font color=#008000>※</font> 到官網下載 .net Core 3.1 ([載點](https://dotnet.microsoft.com/download))

## <font color=#008000>※</font> 開啟之後，按個安裝就完成囉

## <font color=#008000>※</font> 檢查版本
開啟你的終端機，輸入以下指令，只要有出現版本就算正確安裝完成囉(順帶一提，因為我比較習慣用GitBash，所以以下操作都是使用他)
```bash
dotnet --version
```

## <font color=#008000>※</font> 建立專案
要建立一個新專案的話，可以先在想要的位置新增一個資料夾，並把指令位置設定在此資料夾，假設我把資料夾設定在D:\Program\FirstdotnetCore\的路徑下

指令參考可以看看這篇哦(TODO Link 待補充)

接下來輸入以下指令
```bash
dotnet new web
```

接下來會出現以下訊息，代表安裝完囉!這裡不用操作 看一下就好XD

```bash
$ dotnet new web
Getting ready...
The template "ASP.NET Core Empty" was created successfully.

Processing post-creation actions...
Running 'dotnet restore' on D:\Program\FirstdotnetCore\FirstdotnetCore.csproj...
  ▒▒▒b▒P▒_▒n▒٭쪺▒M▒▒...
  ▒w▒٭▒ D:\Program\FirstdotnetCore\FirstdotnetCore.csproj (142 ms ▒▒)▒C

Restore succeeded.

```

接下來只要打開你的資料夾就會發現一堆檔案囉 (TODO Pic)

因為工作關係，寫文章速度有點慢啦!等我有空再把他補完!