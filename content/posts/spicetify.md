---
title: "Spicetify | 自訂化Spotify"
date: 2023-03-17T23:08:46+08:00
draft: false
tags: ["spotify", "spicetify"]
author: "憨憨"
description: "讓自己的Spotify更有特色"
cover:
    image: "https://i.imgur.com/oASRCsq.png"
---
 ![](https://i.imgur.com/oASRCsq.png)
 ![](https://hackmd.io/_uploads/BJxYQfrHh.png)
## 什麼是Spicetify
Spicetify是一個能自訂化Spotify，支援Windows, MacOS和Linux的命令列工具(Command-line tool)
## 如何安裝
### Windows
1. 開啟終端機(PoweShell)
![](https://i.imgur.com/qgsSzTD.png)
2.  輸入以下指令安裝Spicetify


Spicetify CLI
```shell
iwr -useb https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.ps1 | iex
```
Spicetify Marketplace(能直接在Spotify裡安裝並管理插件)
```shell
iwr -useb https://raw.githubusercontent.com/spicetify/spicetify-marketplace/main/resources/install.ps1 | iex 
```
(如果Spicetify沒有啟動的話，再繼續輸入`Spicetify apply`即可)
### MacOS
1. 開啟終端機
![](https://hackmd.io/_uploads/BJtZb3Hr3.png)
2. 輸入以下指令安裝Spicetify

Spicetify CLI
```shell
curl -fsSL https://raw.githubusercontent.com/spicetify/spicetify-cli/master/install.sh | sh
```

```shell
curl -fsSL https://raw.githubusercontent.com/spicetify/spicetify-marketplace/main/resources/install.sh | sh
```
(如果Spicetify沒有啟動的話，再繼續輸入`Spicetify apply`即可)
## 解除安裝
### Windows 
在終端機(PowerShell)輸入下指令
```shell=
spicetify restore
rmdir -r -fo $env:APPDATA\spicetify
rmdir -r -fo $env:LOCALAPPDATA\spicetify
```
### MacOS
```shell=
spicetify restore
rm -rf ~/.spicetify
rm -rf ~/.config/spicetify
```

# 引用資料及相關連結
[Spicetify官網](https://spicetify.app/)
[GitHub Repository](https://github.com/spicetify/spicetify-cli)
