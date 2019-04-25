---
title: next主题设置汇总
tags:
  - next主题设置
categories:
  - hexo
date: 2019-04-25 11:08:02
---

#### 本地搜索
安装
```
npm install hexo-generator-searchdb --save
```
添加以下内容到“站点”配置文件_config.yml
```
search: 
  path: search.xml
  field: post 
  format: html 
  limit: 10000
```
修改“主题”配置文件
```
local_search: 
  enable: true
```
---
#### 设置禁止阅读全文
修改“主题”配置文件
```
auto_excerpt: 
  enable: true 
  length: 150    #length设定文章预览的文本长度。
```
---
### 以下是插件链接
#### [canvas_nest](https://github.com/theme-next/theme-next-canvas-nest/blob/master/README.md#step-1--go-to-next-dir)
```
git clone https://github.com/theme-next/theme-next-canvas-nest source/lib/canvas-nest
```
#### [canvas_three](https://github.com/theme-next/theme-next-three/blob/master/README.md)
```
git clone https://github.com/theme-next/theme-next-three source/lib/three
```
#### [canvas_ribbon](https://github.com/theme-next/theme-next-canvas-ribbon/blob/master/README.md#step-1--go-to-next-dir)
```
git clone https://github.com/theme-next/theme-next-canvas-ribbon source/lib/canvas-ribbon
```