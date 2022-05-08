---
title: python库安装
comments: true
tags:
  - 技术
  - python
categories: python
abbrlink: 82d6e617
date:
updated:
---
简单介绍一下python库安装
无废话<!--more-->
一剑破万法

例：

``` python
pip install wheel # 库名
```

其中whell是库的名字
装什么库就改成什么
在[这里](https://pypi.org/)发现，寻找和发布库

有些库通过以上方法可能无法安装
这时可以使用下载whl包使用wheel安装的方式安装
首先安装wheel库(如例)
然后在[这里](https://www.lfd.uci.edu/~gohlke/pythonlibs/)找到自己要安装的库的安装包下载
（ctrl+f调用浏览器搜索
然后在命令行中使用

``` python
pip install D:\download\wordcloud-1.8.1-cp38-cp38-win_amd64.whl # 文件路径
```

只要如上面将包名改为文件路径即可
记得不要更改安装包文件的名字
可能导致安装失败
