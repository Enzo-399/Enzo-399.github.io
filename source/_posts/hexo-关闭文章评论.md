---
title: Hexo 关闭文章评论
date: 2017-11-24 17:17:10
tags: [Hexo]
categories: Hexo
---
----
大家试想一种情况，今天突然想写一篇关于自己的博客，这时候却不想让别人评论，那该怎么办？

其实 Hexo 早就给我们想好了，实现起来很简单，只需要在头文件加上一行 `comments: false` 就可以了。

以本篇文章为例，用 `hexo n "hexo 关闭文章评论"`创建文章之后默认是

	---
	title: hexo 关闭文章评论
	date: 2017-11-24 17:17:10
	tags: 
	categories: 
	---
只需要在两个---中间任意位置添加 comments 就可以了

	---
	title: hexo 关闭文章评论
	date: 2017-11-24 17:17:10
	tags: 
	categories: 
	comments: false 			// :后面和false中间是有一个空格的
	---

----