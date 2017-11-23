---
title: A+B for Input-Output Practice (VIII)
date: 2017-10-09 20:33:05
tags: '杭电ACM'
categories: ACM
---

Time Limit : 2000/1000ms (Java/Other)   
Memory Limit : 65536/32768K (Java/Other)  
Total Submission(s) : 262   
Accepted Submission(s) : 73  

### Problem Description 
Your task is to calculate the sum of some integers.&lt;br&gt;
  
### Input 
Input contains an integer N in the first line, and then N lines follow. Each line starts with a integer M, and then M integers follow in the same line. &lt;br&gt;

  

### Output
For each group of input integers you should output their sum in one line, and you must note that there is a blank line between outputs.&lt;br&gt;

  

### Sample Input

> 3  
> 4 1 2 3 4  
> 5 1 2 3 4 5  
> 3 1 2 3  

### Sample Output

> 10  
>   
> 15  
>   
> 6  
  
### Author
> lcy

  
示例代码：  

    #include<stdio.h>
    int main(){
	    // n 表示输入的个数
		// a 表示每个 n 对应的输入个数 
		// i 计数器 
		// b 加减运算的数字 
		// sum 和 
		int n,a,i,b,sum;
		scanf("%d",&n);
		for(i=1;i<=n;i++){
			scanf("%d",&a);
			sum=0;
			while(a){
				scanf("%d",&b);
				sum+=b;
				a--;
			}
			if(i!=n){  // 本题要点，要做到最后一个输出时没有换行 
				printf("%d\n\n",sum);
			}else{
				printf("%d\n",sum);
			}
		}
		return 0;
	}

###### *欢迎大家访问我的博客，有什么写的不对的地方请指出来。*
