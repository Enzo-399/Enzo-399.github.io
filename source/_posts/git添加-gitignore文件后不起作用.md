---
title: git添加.gitignore文件后不起作用
date: 2018-01-01 17:28:10
tags: [gitignore]
categories: Git
---
-----
有些时候，你已经把整个项目都加入到了 GitHub 上面，然后又想加一个 .gitignore 文件让它下次再 push 的时候不要再上传某些文件，加了之后发现没有任何变化，这是因为你现在的所有文件处于`track`状态，所以要把文件改成 `Untracked`状态
> .gitignore 文件的用途：
> 
> 该文件只能作用于 Untracked Files，也就是那些从来没有被 Git 记录过的文件（自添加以后，从未 add 及 commit 过的文件）。
> 
> 如果文件曾经被 Git 记录过，那么.gitignore 就对它们完全无效。

##### 解决方法就是先把本地缓存删除（改变成未track状态），然后再提交：
	git rm -r --cached .     
	git add .
	git commit -m 'update .gitignore'

	注:-r 是删除文件夹及其子目录 
	   –cached 是删除暂存区里的文件而不删除工作区里的文件
	   相当于把所有暂存区里的文件删了，再加一遍


> 参考：
> 
[https://www.cnblogs.com/kevingrace/p/5690241.html](https://www.cnblogs.com/kevingrace/p/5690241.html)
[http://blog.csdn.net/qq_34590097/article/details/56284935](http://blog.csdn.net/qq_34590097/article/details/56284935)

----