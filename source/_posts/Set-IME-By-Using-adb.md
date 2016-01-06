---
title: Set IME By Using adb
date: 2016-01-06 23:38:56
tags:
- Skills
- Android
- Hacks
---
最近買了一個山寨行車記錄儀給老豆。把玩了一陣，發現是一個「深度開發」的Android。
所謂「深度開發」就是把系統設置刪得剩下兩三個，然後裝個自製的仿錘子Launcher，再將Home和Back做成浮動。
本來這種改動也沒影響到我。但老豆曰: 

> ## 要有手寫輸入

問題就來了。

安裝輸入法不是問題，附帶的軟件本來就有這個功能。
但問題是 **系統被閹得不似人形，沒法勾選啟用新裝的輸入法**

一翻搜索找到解決方法：**用adb直接設置**
1. 用adb連接設備
    adb shell
2. 列出所有已安裝的輸入法
    ime list -a
3. 勾選想要的輸入法
    ime set com.baidu_spec-1.service/.baiduIME
    
###### 大功告成！

> 本篇無圖，因爲懶
