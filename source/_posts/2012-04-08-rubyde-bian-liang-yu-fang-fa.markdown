---
layout: post
title: "ruby的变量与方法"
date: 2012-04-08 23:38
comments: true
categories: 
---
	calss foo
		def some_behavior_on(string)
			string.upcase #向另一个对象发送消息
		end
		
		def some_behavior
			another_behavior #隐式向自己发送消息,调用的额也是实例方法another_behavior
		end

		def another_behavior
		end

		def self_behavior
			self.another_behavior #显式向self自己发送消息,调用的是实例方法another_behavior
		end

		def self.bar
			fun #消息发送给类对象本身，即调用self.fun
		end

		def self.fun
		end
	end

###类方法和实例方法
以self.开头的是类方法，该方法属于这个类本身，接受这个方法消息的是类对象。 
其他的方法属于实例方法，属于该类的实例，接受消息的是该类实例。 
而在方法体中的self视情况代表不同的对象，类方法中代表类本身，实例方法中代
表该类实例本身，所以在隐式发送消息时就是发送给不同的对象。
