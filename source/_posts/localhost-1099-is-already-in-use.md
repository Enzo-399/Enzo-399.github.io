---
title: 'localhost:1099 is already in use'
date: 2017-11-25 15:34:59
tags: [Tomcat,端口占用]
categories: Tomcat
---
----
前两天写 Javaweb 的时候，项目刚开始编译，发现有问题就把它强制结束了，改完问题再次运行的时候，就出现了下面的情况：
![1](http://wx3.sinaimg.cn/mw690/005KFv1Tgy1flue30llenj308v0243yh.jpg)
下面给出此问题的解决办法。
### 1、打开`CMD`，并输入 `netstat –ano`
（打开 CMD 快捷键为 `win + R` 在弹出的‘运行’窗口里面输入 `cmd`，win 键为键盘左下角一个 Windows 标志的键）
![2](http://wx2.sinaimg.cn/mw690/005KFv1Tgy1flue30zccxj30ii0cwaag.jpg)
### 2、端口被 PID (进程号) 为5300的程序占用，接下来我们找到这个进程把它结束就可以了
（你的PID可能跟我的不同）
### 3、接着在 cmd 下面输入 `tasklist` 找到 5300 号进程，可以看到是被 java.exe 占用了
（如果 tasklist 显示的太多可以用 `tasklist|findstr "5300"` 来代替）
![3](http://wx2.sinaimg.cn/mw690/005KFv1Tgy1flue31biy5j30ib03at8l.jpg)
### 4、快捷键 `Ctrl + Shift + Esc` 打开任务管理器，结束该进程即可
![4](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1flue31q6ivj30kz0im75k.jpg)
### 5、再次运行 Tomcat ，就不会提示 localhost:1099 is already in use 了
----