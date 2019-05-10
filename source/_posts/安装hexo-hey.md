---
title: 安装hexo-hey
tags:
  - hexo-hey
categories:
  - hexo
date: 2019-05-10 20:24:43
---

#### 安装hexo-hey
```
npm install hexo-hey --save 
```
#### 添加以下内容到你的站点配置文件内
```
admin: 
  name:hexo 
  password: hey
  secret: hey hexo 
  expire: 60*1
```
#### 启动hexo-hey
```
hexo s
```
#### 打开网页
```
http://localhost:4000/admin 
```
