---
title: "windows软件清单"
date: 2020-10-21T17:40:47+08:00
lastmod: 2020-10-21T17:40:47+08:00
draft: false #true，除非使用 --buildDrafts 参数，否则不会发布文章
keywords: []
description: ""
tags: # 标签 [ "标签1", "标签2", "标签3" ]
- ceshi
categories:   # 分类
# - hugo
- windows
author: "guzz"
---

> windows正在用及备用软件


<!--more-->

## 浏览器
1. edge
2. firefox

## 工具

   
1. notepad3(PORTABLE)
2. EmEditor
3. WPS/office
4. bandizip
5. 天若ocr
6. Everything
7. PotPlayer64
8.  wiztree

```
notepad3替换

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

notepad3还原

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

   1. idea
   2. git
   3. Go
   4. gradle
   5. hugo
   6. maven
   7. mobaterm
   8. vscode
   9. mysql8
   10. nodejs
   11. openjdk11
   12. pgsql


## 其他

1. tim
2. clash for windows
3. 火绒
4. 微信


## windows设置
1. 开启h-v/wsl2
2. 