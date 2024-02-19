title: hexo在termux下archlinuxarm下后台自动运行
author: John Doe
date: 2024-02-19 20:24:20
tags:
---
### npm安装pm2
```
npm install -g pm2
```
## 添加以下内容到 hexo根目录的run.js文件内
```
##添加如下内容:
const { exec } = require('child_process')
exec('hexo s',(error, stdout, stderr) => {
if(error){
        console.log('exec error: ${error}')
        return
}
console.log('stdout: ${stdout}');
console.log('stderr: ${stderr}');
})
```
## 将pm2的运行指令添加到.bash_profile。如果安装了zsh。就写进.zshrc内.
发现如果直接写入   pm2 start /home/o/blog/run.js
虽然提示运行成功，可是localhost的网页还是打不开。就只能cd到博客目录下再运行指令了。
```
cd blog
pm2 start run.js
cd ..
```