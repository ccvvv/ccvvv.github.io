---
title: hexo安装及简单配置
tags:
  - hexo安装及简单配置
categories:
  - hexo
date: 2019-04-23 14:06:01
---

#### 安装依赖。npm已经包含nodejs
```
pacman -S  npm
```
#### 配置npm国内源
```
npm config set registry http://registry.npm.taobao.org/
```
#### 安装hexo
```
npm  install -g hexo-cli
```
#### 新建文件夹用作博客目录
```
mkdir blog
```
### hexo 初始化 “必须是空目录”
```
hexo init blog
```
#### 进入blog操作

#### 安装hexo-git
```
npm install --save hexo-deployer-git
```
#### 添加 _config.yml的远程库信息
```


type: git
repo: git@github.com:ccvvv/ccvvv.github.io.git
branch: master
```
