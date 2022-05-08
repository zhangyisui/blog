---
title: vbs简单应用
categories: 技术
tags: 技术
abbrlink: aac567fd
date:
---
vbs的较为有趣的一个应用,可以在后台偷偷定时结束某个进程<!--more-->

新建TXT，后缀改成.VBS 代码如下：

do
set bag=getobject("winmgmts:\\.\root\cimv2")
set pipe=bag.execquery("select * from win32_process where name='QQ.exe'")
for each i in pipe
i.terminate()
next
wscript.sleep 1000
loop

每1000毫秒检测一次是否运行了QQ.exe这样一个程序
在运行的话则会自动后台关闭程序且毫无痕迹

1000毫秒和QQ.exe可以改成你需要的任何时间和任何你需要结束的进程
如果是系统是64位的就把Win32改成Win64

把建立的VBS存放在这个文件夹
C:\ProgramData\Microsoft\Windows\Start Menu\Programs\StartUp
即可实现开机自启动
想要解除进入资源管理器找到VBS进程结束运行即可

经过测试可能并不稳定,出问题请自行探索

深夜更新且一天两更,其实是之前攒的没发
