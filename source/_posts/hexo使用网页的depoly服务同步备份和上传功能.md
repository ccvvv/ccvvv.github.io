title: hexo使用网页的depoly服务同步备份和上传功能
author: John Doe
date: 2024-02-19 20:34:13
tags:
---
### 我的hexo目录在git下有两个分支。一个是 master分支。该分支内容就是hexo部署生成后的静态页面上传内容。另一个是bf分支。该分支是hexo本体文件。本体文件的配置内容是生成静态页面后推送到master分支。使用的admin插件。可以网页编辑，还可以网页上运行自己提前设置好的命令。
## 在博客根目录建立 hexod.sh文件。将以下内容加进该文件
```
hexo g && hexo d
git add .
git commit -m"o"
git push --set-upstream origin bf
```
