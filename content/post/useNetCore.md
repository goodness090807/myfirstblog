---
title: "下載並安裝ASP.net core"
date: 2020-07-17T20:31:24+08:00
draft: false
tags: ["asp.net Core"]
---

這篇主要紀錄 .net core的安裝流程 方便自己換電腦的時候來重新安裝，那我們就開始來今天的教學吧

## <font color=#008000>※</font> 到官網下載 .net Core 3.1 ([載點](https://dotnet.microsoft.com/download))
我們要使用 ***.net core SDK*** 前，需要到官方網站下載 ***.net core SDK*** 這樣我們才能透過指令來控制我們的專案，如果是用visual studio的話還是可以透過介面去操作啦! 
![DownLoadSDK](https://i.imgur.com/jU2yFIO.jpg)

## <font color=#008000>※</font> 安裝
下載完後點開執行檔，按個安裝就完成囉，根本超快速XD
![Install](https://i.imgur.com/0ZD36lr.jpg)
## <font color=#008000>※</font> 檢查版本
安裝完後，開啟你的終端機，輸入以下指令，只要有出現版本就算正確安裝完成囉
```powershell
dotnet --version
```
結果圖：

![CheckVersion](https://i.imgur.com/jYAijQ1.jpg)

## <font color=#008000>※</font> 下載編輯器(IDE)
安裝完SDK之後當然就是要安裝我們的編輯器啦，這邊我比較常用以下兩個

* Visual Studio Code(簡稱vs Code) [下載連結](https://code.visualstudio.com/?wt.mc_id=vscom_downloads)
* Visual Studio 2019 [下載連結](https://visualstudio.microsoft.com/zh-hant/vs/)

---

***vs Code*** 的最大的優點就是免費、開源、跨平台，還有一堆Extension可以用，像是如果不習慣原本的開發快捷鍵也可以套用keymap來改成你習慣的，還有要使用我自己席官的語言，像是C# 都可以直接到Extensions去Install，根本超快速就把你的環境弄好了，真的很讚

----

***Visual Studio 2019*** 的話當然還是有一些市場，畢竟像我這種在工作的時候基本上公司都是用 .net framework 還有一些Web Form或是Win form來開發專案，所以很多介面式的操作還是比較會依賴他，因為我懶得去Google要怎麼在vs code 做到同樣功能XDD

---

這兩個的安裝方式也是很簡單，他的安裝介面也寫得很清晰

但是工作完有點懶，安裝方式等我有空再來好好介紹啦!

就這樣，這篇介紹完如何安裝 .net core SDK 和編輯器(IDE) 之後

這樣就可以開始使用你的 .net core 來撰寫網頁囉!

下一篇將開始介紹如何建立新專案
