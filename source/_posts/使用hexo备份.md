---
title: 使用hexo在git的备用
tags:
  - git
  - hexo安装及简单配置
categories:
  - hexo
date: 2019-05-10 20:14:36
---

#### 创建新文件夹
```
mkdir blog
```
#### 进入文件夹
```
cd blog
```
---
### 配置git
#### git 初始化
```
git init
```
#### git关联远程库
```
git remote add origin git@github.com:ccvvv/ccvvv.github.io.git
```
#### git创建并切换分支
```
git checkout -b bf
```
#### 拉取远程分支
```
git pull origin bf
```
#### 安装hexo
```
npm install hexo  -g
npm install hexo --save
```
