---
title: "hugo简单命令和部署"
date: 2020-10-21T16:22:22+08:00
draft: flase
---
> 记录hugo的操作流程

<!--more-->
# 新建文章

`hugo new post/xxx.md`  

启动服务器

`hugo server -D`  


## 用github page和actions自动部署

> .github\workflows\deploy.yml  
要发布到相同用户不同的仓库  
PERSONAL_TOKEN: Settings / Developer settings / Personal access tokens

```
name: Deploy Hugo

on:
  push:
    branches:
      - master

jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2  
        with:
          submodules: true

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: latest
          extended: true

      - name: Build
        run: hugo 

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          #deploy_key : ${{ secrets.GIT_TOKEN }}
          PERSONAL_TOKEN :  ${{ secrets.PERSONAL_TOKEN }}
          external_repository : XX/XX.github.io   
          PUBLISH_BRANCH: master
          PUBLISH_DIR: ./public

```
