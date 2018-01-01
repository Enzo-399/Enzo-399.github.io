---
title: git用.gitignore忽略指定文件
date: 2017-12-31 20:38:11
tags: [gitignore]
categories: Git
---
----
这几天和小伙伴一起开发一个系统，用 Git 做版本管理工具，没用Github托管项目，用的码云，项目是他建的，他可能不太在意这方面的问题吧，Java 编译后的 .class 文件，项目生成的 war 包什么的都传上去了，最要命的是把连接数据库的配置文件也传了，像下图这样，里面直接账号密码都有
![](http://wx2.sinaimg.cn/mw690/005KFv1Tgy1fn0du81wjgj308l052mwx.jpg)我添加了一个.gitignore文件上去，搞完之后是这样：![](http://wx3.sinaimg.cn/mw690/005KFv1Tgy1fn0dwz5uzcj309905wa9x.jpg)这一篇主要讲忽略某个指定的文件，具体的.gitignore使用规则请[移步这里](/git用-gitignore详解%C2%83)

比如说你要忽略的文件叫 `jdbc.properties`在根目录下`src/main/resources`这个文件夹里面，只用在 .gitignore 文件里面加上这样一句 `/src/main/resources/jdbc.properties`这样就可以隐藏指定文件夹下的指定文件了。

----
