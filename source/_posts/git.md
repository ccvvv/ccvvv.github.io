title: git初始化并关联远程库
tags:
  - git
categories:
  - git汇总
date: 2019-04-21 22:44:00
---
#### 初始化
```
git init
```
#### 设置邮箱用户名
```
git config --global user.email "178282609@qq.com"

git config --global user.name "neoiso"
```
#### 添加密钥
```
ssh-keygen -t rsa -C '178282609@qq.com'
```
#### 显示出密钥内容
```
cat /root/.ssh/id_rsa.pub
```
添加到网页中。
### 然后两种方式来关联远程库
### 第一种，直接克隆远程库
```
git clone git@github.com:ccvvv.github.io.git
```
### 第二种，新建本地文件然后关联远程库
```
mkdir blog
cd blog
git init
git remote add origin git@github.com:ccvvv.github.io.git
```
