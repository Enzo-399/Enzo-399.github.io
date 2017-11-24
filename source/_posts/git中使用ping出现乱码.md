---
title: git 中使用 ping 出现乱码
date: 2017-11-24 14:45:41
tags: [Git,乱码]
categories: Git
---

----
因为校园网的问题，每次连上之后都要用 ping 试一下是不是连上了，以前都是默认用得 win + R 打开 CMD 来 ping，今天突发奇想想用 git 试一下，结果就出现了下面的情况：<br>
![1](http://wx2.sinaimg.cn/mw690/005KFv1Tgy1flt7m0cqsyj30n70d5gm2.jpg) 
然后就去百度了一波，最后发现是编码的问题，按下面的步骤改一下就好了。
### 1、在 git 窗口鼠标右键，选择 options 选项
![2](http://wx1.sinaimg.cn/mw690/005KFv1Tgy1flt7m0sn79j30mr0cx3z3.jpg)
### 2、选中 Text ，修改 Character set 为 GBK 即可。我的之前是 UTF-8 格式。
![3](http://wx1.sinaimg.cn/mw690/005KFv1Tgy1flt7m17z6fj30au091mxc.jpg)
<br>更改之后分别点击 Apply 和 Save 即可：<br>
![4](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flt7m1kdc4j30au0913yo.jpg)
### 3、再试一下 ping ：
![5](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flt7m23qfaj30n70d5wfn.jpg)

-----
