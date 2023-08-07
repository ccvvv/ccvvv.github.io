title: hexoo
author: John Doe
date: 2023-08-06 05:28:34
tags:
---
#### 安装依赖。npm已经包含nodejs
```
pacman -S  npm
```
#### 配置npm国内源 两个选择
```
npm config set registry http://registry.npm.taobao.org/
npm config set registry http://mirrors.cloud.tencent.com/npm/
```
#### 安装hexo
[官方文档](https://github.com/hexojs/hexo)
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
```
cd blog
```
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
#### 添加next主题文件的最新版本
[相关网址](https://github.com/theme-next/hexo-theme-next/blob/master/docs/INSTALLATION.md)
```
mkdir themes/next
curl -s https://api.github.com/repos/theme-next/hexo-theme-next/releases/latest | grep tarball_url | cut -d '"' -f 4 | wget -i - -O- | tar -zx -C themes/next --strip-components=1
```
#### 添加admin插件
[插件网址](https://github.com/jaredly/hexo-admin)
```
cd blog
npm install --save hexo-admin
hexo s
open http://localhost:4000/admin/
```
##### 添加admin的网页在线提交功能
###### [原网址](https://github.com/jaredly/hexo-admin/issues/70)
进入博客根目录，添加脚本文件

```
echo "hexo d" > hexod.sh
chmod a+x hexod.sh
```
修改blog的配置文件

```
echo "admin:
  deployCommand: './hexod.sh'" >> _config.yml
```
### 或者另一种方案 hexo-hey
### 但是它只能提供在线编辑无法提交，并不方便
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
http://localhost:4000/admin/admin
```