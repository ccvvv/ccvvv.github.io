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
[官方文档](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
```
 ssh-keygen -t ed25519 -C  "178282609@qq.com"
```
#### 显示出密钥内容
```
cat /root/.ssh/id_ed25519.pub
```
#### 將内容添加到网页个人设置的sshkey



### 在后台启动 ssh 代理。
```
eval "$(ssh-agent -s)"
```
   ##  会输出> Agent pid 59566

### 将 SSH 私钥添加到 ssh-agent。 如果使用其他名称创建了密钥或要添加具有其他名称的现有密钥，请将命令中的 ided25519 替换为私钥文件的名称。
```
ssh-add ~/.ssh/id_ed25519
```
### 仓库地址备用
```
git@github.com:ccvvv/bf.git
git@github.com:ccvvv/ccvvv.github.io.git
```