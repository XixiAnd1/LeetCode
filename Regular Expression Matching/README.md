#第十题
##Regular Expression Matching

正则表达式匹配

###版本1
没有想到解决办法，想到了使用回溯，但是没有想清楚具体如何实现，弄了一下放弃了，估计自己真做出来得花几天。于是直接看了答案，发现好简单，从前往后一个个匹配即可。当初想的太复杂了，前后各种匹配，反而不知道该如何实现了。
在网上找的这个版本，实现出来效率很低，再查查有什么更好的办法

###版本2
http://blog.csdn.net/linhuanmars/article/details/21145563
在上面的博客里，看到了使用动态规划的解法，其实本质上与递归是相同的，难点就在于如何找到它的状态转移方程。
该博客的文字解释中有误：   
	文字解释中的，所有p[j+1] == '*'的判断，都该改成p[j] == '*',如此才和代码中的结果一致。最初这个错误耽误了我三个小时，才彻底搞明白。使用该解法之后，速度立刻提升到了最快。