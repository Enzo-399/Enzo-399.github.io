---
title: IDEA 新建 Servlet 报错
date: 2017-11-25 16:29:51
tags: [Tomcat,IDEA,Servlet]
categories: Tomcat
---
----
用 idea 新建了一个 servlet 结果报错，不能运行，也不能代码提示，然后经过一番操作才知道原来是 Tomcat 的 jar 包的依赖没有导入。
报错截图：
![1](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1fluflwe5e2j311y0lcq5q.jpg)
解决方法：
### 1、左上角 `File -> Project Settings` 打开项目的配置文件，也可以直接用快捷键 `Ctrl + Alt + Shift + S`
![2](http://wx3.sinaimg.cn/mw690/005KFv1Tgy1flufqjt9irj308h09et8t.jpg)
### 2、在 Modules 选项卡下的 Dependencies 选项下，右边有一个加号，具体看下图
![3](http://wx3.sinaimg.cn/mw690/005KFv1Tgy1fluflwuse6j310x0jkmyi.jpg)
### 3、选 Library 选项
![4](http://wx2.sinaimg.cn/mw690/005KFv1Tgy1fluflxfa6pj308005et8l.jpg)
### 4、选中下面的 Tomcat ，点 Add Selected
![5](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1fluflxqaa6j30f00e274b.jpg)
### 5、然后就可以看到 Tomcat 加入到 Dependencies 里面了，点 Apply ，OK 即可
![6](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flufly9pfwj310x0jkwfo.jpg)
### 6、如果还是不行，重启下 idea 就可以了
 ![7](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1fluflyos11j311y0lc0vh.jpg)

----