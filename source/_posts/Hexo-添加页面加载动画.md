---
title: Hexo 添加页面加载动画
date: 2017-11-24 23:54:19
tags: [Hexo]
categories: Hexo
---
----
是不是感觉我右上角这个加载动画很好玩，什么？没看到！下面GIF给你机会再看一遍。
<img src="http://wx3.sinaimg.cn/large/005KFv1Tgy1fltmd5kq7sg30gy013dgi.gif"/>
下面我就一步步介绍怎么显示这个效果吧。
### 1、找到主题配置文件 `_config.yml` ,此文件位于 `/themes/hexo-theme-next`文件夹下。
（hexo-theme-next为我放 Next 主题的文件夹）
![1](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1fltnj7q782j30gt0fl3zu.jpg)
### 2、修改 `_config.yml`下`pace: false`改为`pace: true`就可以了。
![2](http://wx1.sinaimg.cn/mw690/005KFv1Tgy1fltnjau19tj30g90d3q3g.jpg)
### 3、如果你想试下别的样式，只需要把下面的任一行复制在`pace_theme:`后面即可。
	pace-theme-big-counter
	pace-theme-bounce 			// 这个是我用的
	pace-theme-barber-shop
	pace-theme-center-atom
	pace-theme-center-circle
	pace-theme-center-radar
	pace-theme-center-simple
	pace-theme-corner-indicator
	pace-theme-fill-left
	pace-theme-flash
	pace-theme-loading-bar
	pace-theme-mac-osx
	pace-theme-minimal	

----