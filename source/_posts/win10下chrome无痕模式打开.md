---
title: win10下chrome无痕模式打开
date: 2020-05-25 09:27:46
tags:windows
---

[TOC]

# chrome桌面图标默认使用无痕模式打开

 		桌面图标默认使用无痕模式这个教程最多，具体修改方式如下：

​         鼠标右键点击chrome的桌面快捷方式，选择属性，打开后，选择快捷方式属性，然后修改目标栏的值，

在`C:\Program Files (x86)\Google\Chrome\Application\chrome.exe`后面添加 -incognito

# chrome任务栏默认使用无痕模式打开

​		这个修改的教程就相对较少了，修改方式如下：

​		打开`C:\Users\XXXX\AppData\Roaming\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar`路径，在下面找到chrome的快捷图标，修改方式与chrome桌面桌面图标修改方式相同：右键chrome图标，选择属性，打开后，选择快捷方式属性，然后修改目标栏的值，在`C:\Program Files (x86)\Google\Chrome\Application\chrome.exe`后面添加` -incognito`

# chrome外部链接默认使用无痕模式打开

​		1、按下`Win+R`键，在打开的运行对话框中输入`regedit`,然后回车开发系统注册表；

​		2、按照顺序展开注册表`HKEY_CLASSES_ROOT\ChromeHTML\shell\open\command`,在右侧的内容中，双击“默认”，弹出编辑字符串。在“数值数据”一栏中后面添加 `--incognito`参数。例如：`"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" -- "%1"`修改为`"C:\Program Files (x86)\Google\Chrome\Application\chrome.exe" --incognito -- "%1"`





*注意：如果`C:\Program Files (x86)\Google\Chrome\Application\chrome.exe`被引号引起来，在在引号后面添加`-incognito`。另外`-incognito`前面有一个空格*