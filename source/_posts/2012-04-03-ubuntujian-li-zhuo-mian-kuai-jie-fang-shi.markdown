---
layout: post
title: "ubuntu建立桌面快捷方式"
date: 2012-04-03 11:22
comments: true
categories: 
---
今天下载了sublime text2这个编辑器，想在桌面放一个快捷方式方便启动。一开始
用了
	ln -s /opt/Sublime/sunlime_text ～/桌面/sublime_text #注意要用绝对路径，路径中的空格要转义
建立了一个软链接放在桌面，满足了需求但是很图标很丑陋。

于是换用第二种方法，使用启动器。在桌面建立一个文件名为sublime.desktop，编辑内容为：

	[Desktop Entry]
	Version=1.0
	Type=Application
	Name=sublime
	Exec=/opt/Sublime/sublime_text
	Icon=/opt/Sublime/Icon/256*256/sublime_text.png

使用了sublime自带的图标，之后可能需要再设置一下运行权限。
这样桌面就有了一个美观的快捷启动方式。
