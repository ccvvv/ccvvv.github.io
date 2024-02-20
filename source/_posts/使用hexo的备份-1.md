title: 使用hexo的备份
author: John Doe
date: 2023-08-19 05:05:00
tags:
---
### 创建blog
```
mkdir blog
```


### 在blog文件内初始化git
```
git init 
```
### 关联远程库
```
git remote add origin git@github.com:ccvvv/ccvvv.github.io.git
```
### 切换分支bf 并pull下来
```
git checkout -b bf
```
```
git pull origin bf
```
### 安装hexo
```
npm install hexo-cli -g
```
### 安装hexo模块
```
rm -rf node_modules && npm install --force
```