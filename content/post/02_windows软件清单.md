---
title: "windows软件清单"
date: 2020-10-21T17:40:47+08:00
lastmod: 2021-03-05
draft: false #true，除非使用 --buildDrafts 参数，否则不会发布文章
keywords: []
description: ""
tags: # 标签 [ "标签1", "标签2", "标签3" ]
- 软件
categories:   # 分类
# - hugo
- windows
author: "guzz"
---

> windows正在用及备用软件


<!--more-->

## 浏览器
- edge
- firefox

## 工具

   
- notepad3(PORTABLE)
- EmEditor
- WPS/office
- bandizip
- 天若ocr
- Everything
- PotPlayer64
-  wiztree

```bash

# notepad3替换

@echo off
cd /d "%~dp0"
echo.
echo 请确认是以管理员权限运行本批处理文件！!
echo.
pause
cd /d "%~dp0"
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\notepad.exe" /v "Debugger" /d "\"%~dp0Notepad3.exe\" /z" /f
cls
echo.
echo.
pause

# notepad3还原

@echo off
cd /d "%~dp0"
echo.
echo 请确认是以管理员权限运行本批处理文件！!
echo.
pause
cd /d "%~dp0"
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\notepad.exe" /v "Debugger" /d "\"%~dp0Notepad3.exe\" /z" /f
cls
echo.
echo.
pause






```


## 开发工具

- idea
- git
- Go
- gradle
- hugo
- maven
- mobaterm
- vscode
- mysql8
- nodejs
- openjdk11
- pgsql


## 其他

- tim
- clash for windows
- 火绒
- 微信


## windows设置

- 开启h-v/wsl2

  1. 在wsl2配置
  2. 配置防火墙 **!!!**
```bash
# wsl2 
export windows_host=`cat /etc/resolv.conf|grep nameserver|awk '{print $2}'`
export ALL_PROXY=socks5://$windows_host:10808
export HTTP_PROXY=$ALL_PROXY
export http_proxy=$ALL_PROXY
export HTTPS_PROXY=$ALL_PROXY
export https_proxy=$ALL_PROXY


```

