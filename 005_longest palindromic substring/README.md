# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 005_longest palindromic substring(最长回文子串)
## 问题描述与输入输出
	
### 问题描述
给定一个字符串 s，找到 s 中最长的回文子串。你可以假设 s 的最大长度为1000。

### 问题案例
	输入: "babad"
	输出: "bab"
	注意: "aba"也是一个有效答案。
	
	输入: "cbbd"
	输出: "bb"
	
### 输入与输出

* 输入：char* s:输入的数组头指针
* 输出: char* 最长回文子串的头指针

## 思路			
1. 动态规划:lp代表i与j字符是否存在回文路，使用该方法时间复杂度为O（n^2），空间复杂度为O（n）。状态方程如下

								1                           i=j
		lp[i][j] =        (d[i] == d[j])                    i=j-1
					(d[i] == d[j]) && (lp[i+1,j-1])         j-i>1 
					
2. [Manacher算法](https://www.cnblogs.com/Stay-Hungry-Stay-Foolish/p/7622496.html)（明日总结与写出代码）

## 拓展与思考：
### 拓展

### 思考

        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
