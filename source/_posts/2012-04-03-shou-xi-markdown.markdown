---
layout: post
title: "熟悉MarkDown"
date: 2012-04-03 15:40
comments: true
categories: 
---
Markdown是一种用来简化HTML撰写的语法，使用它能够快速的实现常用的HTML元素。
octopress默认使用这种格式。
##标题
两种方式
	First level
	============
	Second level
	--------------
或者
	# <h1>
	## <h2>
	...
	###### <h6>
会显示成这样：
First level
============
Second level
--------------
# h1
## h2
...
###### h6


	*强调*
	**strong**
like this:

*强调*
**strong**

##列表
	* 蜘蛛侠
	* 蝙蝠侠
	* 绿灯侠
	1. 邪恶博士
	1. 企鹅人
	1. 这个不知道
* 蜘蛛侠
* 蝙蝠侠
* 绿灯侠
- - - -
1. 邪恶博士
1. 企鹅人
1. 这个不知道

##链接
	这是一个[大美妞哦](http://meinv.com)
or
	我用了这个[东东][1]一次,[东东][1]两次，[东东][1]三次。。。
	[1]: http://dongdong.com
这是一个[大美妞哦](http://meinv.com)

or

我用了这个[东东][1]一次,[东东][1]两次，[东东][1]三次。。。
[1]: http://dongdong.com

##图片

	![Markdown](http://www.youapp.cn/data/attachment/forum/201204/01/112904r6kk06zepluql7k6.jpg)
like this:

![Markdown](http://www.youapp.cn/data/attachment/forum/201204/01/112904r6kk06zepluql7k6.jpg)

##代码
单行
	输入`mkdir dir`
输入`mkdir dir`

代码快直接缩进4空格或者一个tab









