# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 029_Divide Two Integers(两个数相除)
## 问题描述与输入输出
	
### 问题描述
给定两个整数，被除数 dividend 和除数 divisor。将两数相除，要求不使用乘法、除法和 mod 运算符。

返回被除数 dividend 除以除数 divisor 得到的商。

_说明_:

	被除数和除数均为 32 位有符号整数。
	除数不为 0。
	假设我们的环境只能存储 32 位有符号整数，其数值范围是 [−231,  231 − 1]。本题中，如果除法结果溢出，则返回 231 − 1。
	
### 问题示例
	
	示例1：
	输入: dividend = 10, divisor = 3
	输出: 3
	
	示例2：
	输入: dividend = 7, divisor = -3
	输出: -2
		
### 输入与输出
* 输入：
	* int dividend：输入的被除数
	* int divisor：输入的除数
	
* 输出：
	* int: 两数相除的结果

## 思路			
### 二分法

	next记录每次二分后，所残留的被除数
	while(next >= divisor)
		divisor的倍数分别是1,2,4,...2^n直至divisor*(2^n)大于dividend
		然后商加等于2^(n-1)，next等于dividend-2^(n-1)     
	
## 拓展与思考：
### 拓展
如果是浮点型数据的除法呢？稍微复杂一点。
### 思考
本题限制了不能使用乘法，像基于恢复余数、不恢复余数、泰勒计数、牛顿迭代方法都不可以用了。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
