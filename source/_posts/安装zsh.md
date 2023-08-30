title: archlinux安装zsh
author: John Doe
date: 2023-08-27 05:16:49
tags:
---
### 安装zsh框架
```
pacman -S zsh
```
#### 安装zsh
```
git clone https://github.com/robbyrussell/oh-my-zsh
```
#### 运行安装程序
```
sh /root/oh-my-zsh/tools/install.sh
```

### 以下参考自 [点这个](http://t.csdn.cn/NoEvL)

### 代码高亮插件zsh-syntax-highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

### 自动建议插件zsh-autosuggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### 自动补全插件zsh-completions
```
git clone https://github.com/zsh-users/zsh-completions $ZSH_CUSTOM/plugins/zsh-completions
```

### 自动补全需要加此行代码
```
[ -z "`grep "autoload -U compinit && compinit" ~/.zshrc`" ] && echo "autoload -U compinit && compinit" >> ~/.zshrc
```
### 插件写入zsh配置文件
```
sed -i '/^plugins=/c\plugins=(git z zsh-syntax-highlighting zsh-autosuggestions zsh-completions)' ~/.zshrc
```
### 重载配置
```
source ~/.zshrc
```
---
如果使用git命令报错“Failed to connect to github.com port 443: Timed out”，使用如下命令
```
git config --global --unset http.proxy
git config --global --unset https.proxy
```
git clone https://github.com/robbyrussell/oh-my-zsh