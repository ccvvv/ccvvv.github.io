title: termux相关设置
author: John Doe
date: 2023-08-06 20:40:38
tags:
---

### termux国内源
```
sed -i 's@^\(deb.*stable main\)$@#\1\ndeb https://mirrors.tuna.tsinghua.edu.cn/termux/apt/termux-main stable main@' $PREFIX/etc/apt/sources.list&& apt update && apt upgrade
```
### 安装proot-distro及相关指令
```
pkg install proot-distro
proot-distro install archlinux
proot-distro remove  archlinux
```
#### 將启动指令添加到环境配置自动打开archlinux
```
echo "proot-distro login archlinux" >> .bashrc
```
### 备份系统及还原系统
#### 获取访问文件权限
```
termux-setup-storage 
```
#### 备份及还原相关指令
##### 备份
```
proot-distro backup archlinux --output /data/data/com.termux/files/home/storage/downloads/bf.tar.gz
```
##### 还原
```
proot-distro restore /data/data/com.termux/files/home/storage/downloads/bf.tar.gz
```


