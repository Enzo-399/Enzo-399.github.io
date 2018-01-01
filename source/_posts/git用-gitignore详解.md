---
title: "git用.gitignore详解"
date: 2018-01-01 11:12:24
tags: [gitignore]
categories: Git
---
----
在 GitHub 上托管项目，一般最好建一个 .gitignore 文件，这不仅是一个好习惯，更可以减轻 GitHub 的服务器压力，也可以防止自己的私密信息泄露。
最简单的创建 .gitignore 文件的方法是，在 GitHub 上新建仓库的时候创建，也就是下图这里：
![](http://wx4.sinaimg.cn/mw690/005KFv1Tgy1fn16jvvuk1j30o00gmwf9.jpg)可以在它的下面选择或者搜索你所用到的语言，比如选我上面选的`Java`：
![](http://wx3.sinaimg.cn/mw690/005KFv1Tgy1fn16jw9f7lj309u0fdweo.jpg)
新建完成后，打开可以看到，它自动生成的代码：

    # Compiled class file
    *.class

    # Log file
    *.log

    # BlueJ files
    *.ctxt
	
     # Mobile Tools for Java (J2ME)
    .mtj.tmp/
	
    # Package Files #
    *.jar
    *.war
    *.ear
    *.zip
    *.tar.gz
    *.rar
##### 忽略文件的原则是：
>  1.忽略操作系统自动生成的文件，比如缩略图等；

>  2.忽略编译生成的中间文件、可执行文件等，也就是如果一个文件是通过另一个文件自动生成的，那自动生成的文件就没必要放进版本库，比如Java编译产生的.class文件
>  
>  3.忽略你自己的带有敏感信息的配置文件，比如存放口令的配置文件。
##### 配置语法：
	以斜杠“/”开头表示目录；
	以星号“*”通配多个字符；
	以问号“?”通配单个字符
	以方括号“[]”包含单个字符的匹配列表；
	以叹号“!”表示不忽略(跟踪)匹配到的文件或目录；

> 注：git 对于 .gitignore 配置文件是按行从上到下进行规则匹配的，意味着如果前面的规则匹配的范围更大，则后面的规则将不会生效；
##### 示例：
>
	1、folder/*
> 表示：忽略目录 folder 下的全部内容，不管是根目录下的 /folder/目录，还是某个子目录 /child/folder/ 下的目录，都会省略
>
 	2、/folder/*
> 表示：忽略根目录 /folder/ 下的全部内容，而某个子目录 /child/folder/ 下的目录不受影响
>
	3、/*
	!.gitignore
	!/folder/bin/
	!folder/src/
> 表示：忽略全部内容，但不忽略 .gitignore 文件、根目录 /fplder/bin/ 下的文件、所有目录 fplder/src/ 下的文件
>
	4、*.a
> 表示：忽略所有 .a 结尾的文件
> 	
	5、doc/*.txt
> 表示：会忽略 doc/notes.txt 但不包括 doc/server/arch.txt

----
如果项目已经上传到了 GitHub 上面，而没有加 .gitignore 文件怎么办呢？请[移步这里](/git添加-gitignore文件后不起作用)

> 参考：
>
> [https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013758404317281e54b6f5375640abbb11e67be4cd49e0000](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/0013758404317281e54b6f5375640abbb11e67be4cd49e0000)
> 
[https://www.cnblogs.com/kevingrace/p/5690241.html](https://www.cnblogs.com/kevingrace/p/5690241.html)

----