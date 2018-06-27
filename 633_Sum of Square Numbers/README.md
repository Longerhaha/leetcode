# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 633_Sum of Square Numbers（平方数之和）
## 问题描述与输入输出
### 问题描述

给定一个非负整数 c ，你要判断是否存在两个整数 a 和 b，使得 a^2 + b^2 = c。

### 问题示例

	示例1：
	输入: 5
	输出: True
	解释: 1 * 1 + 2 * 2 = 5
	
	示例2：
	输入: 3
	输出: False
	
### 函数输入与输出：
* 输入：
	* int c: 非负整数c
	
* 输出：
	* bool：是否存在两个整数 a 和 b，使得 a^2 + b^2 = c。

## 思路			
### 双下标法
	去除背景，本题其实就是两数之和。
	下标start从0开始，end从sqrt（c）开始。
	在while(start < end)循环内，若start*start+end*end < c，说明数不够大，则start++，以此增大数据
								若start*start+end*end > c，说明数够大了，则end--， 以此减小数据
								若start*start+end*end == c，直接返回true
	跳出循环后，此时start==end， 直接返回(2*start*start == c) 的结果。
## 拓展与思考：
### 拓展
如果题目要求是三个平方数之和？甚至是四个平方数之和？怎么做？其实就是三数之和、四数之和的变形。
### 思考
这个去除背景后退化为两数之和。两数、三数、四数之和这些基本的问题还是很有用的。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
