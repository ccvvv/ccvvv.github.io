title: Cataclysm-DDA
author: John Doe
date: 2023-08-30 18:55:28
tags:
---
## 准备工作
### [游戏下载主页](https://cataclysmdda.org/releases/)
### [游戏主页](https://github.com/CleverRaven/Cataclysm-DDA)
### [编译指导](https://www.github.com/CleverRaven/Cataclysm-DDA/blob/master/COMPILING.md)
### [make相关参数](https://www.github.com/CleverRaven/Cataclysm-DDA/blob/master/Makefile)
###  下载游戏
首先克隆下来 depth就是浅拷贝，它只会拷贝最后一次提交，而不是所有的提交记录。
```
git clone -b master --depth=1 https://github.com/CleverRaven/Cataclysm-DDA
```
###  下载编译所需
```
ccache   clang astyle
```
### 下载游戏依赖
#### 基于Arch的依赖：

重要：gcc-libs  glibc  zlib  bzip2 astyle
可选： gettext           
终端界面： ncurses
图形界面：sdl2，sdl2_image，sdl2_ttf，sdl2_mixer，freetype2
#### 基于debian的依赖：
运行下面的命令以安装依赖
```
sudo apt-get install libncurses5-dev libncursesw5-dev build-essential astyle gettext
```
###  编译
然后进入下载的游戏主目录，运行下面命令编译游戏：
```
make -j8 CLANG=1 CCACHE=1 RELEASE=1 LANGUAGES=zh_CN
```
### 小问题
如果游戏目录下lang文件里没有mo文件。你需要进入 Cataclysm-DDA/lang 目录下，运行编译脚本：
``` 
./compile_mo.sh
```
# 就可以愉快的玩游戏了！
---
P1:gettext-用于本地化支持;如果你打算只使用英语，你可以跳过它。
P2:astyle 是makefile文件里所需要的。
P3:最新的游戏已经不需要lua了。
P4:想了解更多make的参数详情请阅读首页给出的网址。
P5:如果git clone下载速度过于感人。可以直接去该游戏的网址主页下载zip压缩包。