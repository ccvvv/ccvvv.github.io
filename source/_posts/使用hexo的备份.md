title: arch设置
author: John Doe
date: 2023-08-19 05:18:07
tags:
---
### 添加清华源

```
echo "Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxarm/\$arch/\$repo" >/etc/pacman.d/mirrorlist
```
### 或者添加中科大源
```
echo "Server =https://mirrors.ustc.edu.cn/archlinuxarm/\$arch/\$repo" >/etc/pacman.d/mirrorlist
```

### 更新系统，安装一些常用软件
```
pacman -Syu
```
```
pacman -S vim clang git
```
### 更换中文环境

#### 使用vim將/etc/locale.conf内zh_CN.UTF-8的注释去掉
```

vim /etc/locale.conf
```
#### 使修改生效
```
locale-gen
```
#### 修改环境配置使其生效
```
echo "export LANG=zh_CN.UTF-8" >> /etc/locale.conf
```
### 安装中文man
```
pacman -S man-pages-zh_cn man-pages-zh_tw
```
### 删除软件的指令
#### 删除软件但保留依赖关系
```
pacman -R packname
```
#### 删除软件及没有被其他软件使用的依赖关系
```
pacman -Rs packname
``` 
#### 删除软件包和所有依赖关系
```
pacman -Rsc packname
```
 
