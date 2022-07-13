---
title: 如何把bat文件固定至开始菜单
comments: true
tags:
  - 技术
categories: 技术
abbrlink: 4c53d122
date:
updated:
---
写了个bat，为了方便想把它固定到开始菜单里
一试方知，win10系统只允许可执行文件(exe)固定到开始菜单上，普通文件（包括bat脚本文件）是不能固定到开始菜单上的
查了查，有个很简单的办法如下：<!--more-->

右键选择新建快捷方式。

在文件路径输入框中，按照如下格式给出你想固定在开始菜单的bat文件的路径

cmd /c “bat文件路径”：此命令运行完批处理后窗口自动关闭；
cmd /k “bat文件路径”：此命令运行完批处理后窗口不会自动关闭；

而后点击“下一步”修改快捷方式名称。

这样的快捷方式就能直接右键固定到开始屏幕了
其实只不过是用cmd进行了一下中转
因为cmd是可执行文件
只能说Windows某些方面还是有点落后