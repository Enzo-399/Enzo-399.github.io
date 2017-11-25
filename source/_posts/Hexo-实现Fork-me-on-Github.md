---
title: Hexo 实现 Fork me on Github
date: 2017-11-25 13:54:28
tags: [Hexo]
categories: [Hexo]
---
----
今天看一篇博客，他的右上角有一个Fork me on Github，点了一下就到了他的 gayhub 主页，就在网上搜了一下怎么实现，下面记录下来。
（Github 全球最大同性交友网站，程序员不可能不知道 /滑稽）
贴几张效果图：
<div style="float:left;margin:1px;width:24%;"><img src="https://camo.githubusercontent.com/82b228a3648bf44fc1163ef44c62fcc60081495e/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f7265645f6161303030302e706e67" ></div>

<div style="float:left;margin:1px;width:24%;"><img src="https://camo.githubusercontent.com/567c3a48d796e2fc06ea80409cc9dd82bf714434/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f6c6566745f6461726b626c75655f3132313632312e706e67" ></div>

<div style="float:left;margin:1px;width:24%;"><img src="https://camo.githubusercontent.com/38ef81f8aca64bb9a64448d0d70f1308ef5341ab/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f6461726b626c75655f3132313632312e706e67" ></div>

<div style="float:left;margin:1px;width:24%;"><img src="https://camo.githubusercontent.com/52760788cde945287fbb584134c4cbc2bc36f904/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769746875622f726962626f6e732f666f726b6d655f72696768745f77686974655f6666666666662e706e67"</div>
<div style="float:none;clear:both;">

</div>
### 1、[点我!点我!](https://github.com/blog/273-github-ribbons)在这里挑选自己喜欢的样式，并复制。
我复制的是这段：
>     <a href="https://github.com/you">     
		<img style="position: absolute; top: 0;
		left: 0; border: 0;" src="https://camo.githubusercontent.com/567c3a48d796e2fc0
		6ea80409cc9dd82bf714434/68747470733a2f2f73332e616d617a6f6e6177732e636f6d2f6769
		746875622f726962626f6e732f666f726b6d655f6c6566745f6461726b626c75655f3132313632
		312e706e67" alt="Fork me on GitHub" data-canonical-
		src="https://s3.amazonaws.com/github/ribbons/forkme_left_darkblue_121621.png">
	</a>
### 2、把复制的代码放在 `themes/hexo-theme-next/layout/_layout.swig`文件`<div class="headband"></div>`下面，并把 `href`中的 `https://github.com/you` 改成你的 Github 地址
![1](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flucmqbad3j30z40c5wfw.jpg)
### 3、重新部署你的博客就可以看到了
----