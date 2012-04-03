---
layout: post
title: "Octopress体会"
date: 2012-04-03 22:51
comments: true
categories: 
---
Octopress是一个基于Jekyll的静态站点生成程序，集成了一些插件，内建了几种站点的部署
用gitpages尤其方便。

在项目根目录`rake -T`查看当前支持的命令，就像以前通过make来了解一个C项目的脉络，阅读
Rakefile也可以让你了解这个程序的布局，流程，组成等一些细节。

通过`rake setup_github_pages[repo]`设置好与gitpages的连接之后，只需简单的
使用`rake new_post[title] `和`rake gen_deploy`就能将博客发布到gitpage上。
如果要先在本地审查的话，可以先用`rake generate`再`rake preview`会在本地的4000端口开一个服务器，当检查完毕
确认之后再`rake deploy`上传即可

项目默认在根目录下是source分支，同步到git的source分支，在_deploy下是master分支，
将生成的静态站点上传到远程项目的master分支用于显示。

sass和source/_includes/下的custom目录都是用来自定义的。当`rake install[theme]`新主题
时，使用`rake update_source[theme]`和`rake update_style[theme]`会拷贝回这些自定义的内容直接应用到新主题。

项目所支持的rake command都是管理master分支的，source分支需要自己手动push。

如果要在另一台机器上写博客，可以先`git clone -b source git@github.com:name/name.github.com.git`
再`rake setup_github_pages[repo]`即可。
