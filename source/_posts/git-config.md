---
title: git config
date: 2023-08-05 22:24:39
tags:
---
#### 初始化
```
git init
```
#### 设置邮箱用户名
```
git config --global user.email "178282609@qq.com"

git config --global user.name "ccvvv"
```
#### 添加密钥
```
 ssh-keygen -t ed25519 -C  "178282609@qq.com"
```
#### 显示出密钥内容
```
cat /root/.ssh/id_ed25519.pub
```

### 在后台启动 ssh 代理。
```
eval "$(ssh-agent -s)"
```
   ##  会输出> Agent pid 59566

### 将 SSH 私钥添加到 ssh-agent。 如果使用其他名称创建了密钥或要添加具有其他名称的现有密钥，请将命令中的 ided25519 替换为私钥文件的名称。
```
ssh-add ~/.ssh/id_ed25519
```

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
