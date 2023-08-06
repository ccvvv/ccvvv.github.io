title: hexoo
author: John Doe
date: 2023-08-06 05:28:34
tags:
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
npm install hexo-cli -g
```
#### 新建文件夹用作博客目录
```
mkdir blog
```
### hexo 初始化 创建新目录
```
hexo init blog
```
#### 进入blog操作
cd blog

#### 安装hexo-git
```
npm install --save hexo-deployer-git
```
#### 添加 _config.yml的远程库信息
```


type: git
repo:  git@github.com:ccvvv/ccvvv.github.io.git
branch: master
```