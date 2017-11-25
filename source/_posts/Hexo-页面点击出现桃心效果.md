---
title: Hexo 页面点击出现桃心效果
date: 2017-11-25 10:15:48
tags: [Hexo,Next]
categories: Hexo
---
----
有没有发现我的页面任意位置点击都会出现像下图一样的小心心，下面是具体的实现方法。
<center>
![1](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flu6sde7bwj303i04t742.jpg)
</center>
### 1、新建一个 `love.js` 文件并将其放到 Next 主题的 `source/js/src` 文件夹下
（具体目录`themes/hexo-theme-next/source/js/src`，hexo-theme-next为我放 Next 主题的文件夹）
![2](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flu6sdrgjfj30li0a7t9k.jpg)
### 2、将下面这段代码复制到 `love.js` 里面
```JavaScript
! function(e, t, a) {
	function n() {
		c(".heart{width: 10px;height: 10px;position: fixed;background: #f00;transform: rotate(45deg);-webkit-transform: rotate(45deg);-moz-transform: rotate(45deg);}.heart:after,.heart:before{content: '';width: inherit;height: inherit;background: inherit;border-radius: 50%;-webkit-border-radius: 50%;-moz-border-radius: 50%;position: fixed;}.heart:after{top: -5px;}.heart:before{left: -5px;}"), o(), r()
	}

	function r() {
		for (var e = 0; e < d.length; e++) d[e].alpha <= 0 ? (t.body.removeChild(d[e].el), d.splice(e, 1)) : (d[e].y--, d[e].scale += .004, d[e].alpha -= .013, d[e].el.style.cssText = "left:" + d[e].x + "px;top:" + d[e].y + "px;opacity:" + d[e].alpha + ";transform:scale(" + d[e].scale + "," + d[e].scale + ") rotate(45deg);background:" + d[e].color + ";z-index:99999");
		requestAnimationFrame(r)
	}

	function o() {
		var t = "function" == typeof e.onclick && e.onclick;
		e.onclick = function(e) {
			t && t(), i(e)
		}
	}

	function i(e) {
		var a = t.createElement("div");
		a.className = "heart", d.push({
			el: a,
			x: e.clientX - 5,
			y: e.clientY - 5,
			scale: 1,
			alpha: 1,
			color: s()
		}), t.body.appendChild(a)
	}

	function c(e) {
		var a = t.createElement("style");
		a.type = "text/css";
		try {
			a.appendChild(t.createTextNode(e))
		} catch (t) {
			a.styleSheet.cssText = e
		}
		t.getElementsByTagName("head")[0].appendChild(a)
	}

	function s() {
		return "rgb(" + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + "," + ~~(255 * Math.random()) + ")"
	}
	var d = [];
	e.requestAnimationFrame = function() {
		return e.requestAnimationFrame || e.webkitRequestAnimationFrame || e.mozRequestAnimationFrame || e.oRequestAnimationFrame || e.msRequestAnimationFrame || function(e) {
			setTimeout(e, 1e3 / 60)
		}
	}(), n()
}(window, document);
```
### 3、然后打开 `/themes/hexo-theme-next/layout/_layout.swig` 文件，在其末尾添加下面这段代码
	<!-- 页面点击小红心 -->
	<script type="text/javascript" src="/js/src/love.js"></script>
![3](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flu6vwv9ldj30tl0iudhe.jpg)
### 4、重新部署博客你就会发现你的博客像我的一样酷炫了
----