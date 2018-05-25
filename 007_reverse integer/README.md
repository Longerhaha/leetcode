# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 007_reverse integer(反转整数)
## 问题描述与输入输出
	
### 问题描述
给定一个 32 位有符号整数，将整数中的数字进行反转。假设我们的环境只能存储 32 位有符号整数，
其数值范围是[−2^31,2^31−1]。根据这个假设，如果反转后的整数溢出，则返回 0。
	
### 问题案例
	示例1
	输入: 123
	输出: 321
	
	示例2
	输入: -123
	输出: -321
	
	示例3
	输入: 120
	输出: 21
	
### 输入与输出

* 输入：int x 需要反转的整数
* 输出: int 反转后的整数

## 思路			
反转较为简单，每次取剩下需要反转的数的最后一位，然后上一次结果*10+此次最后一位。需要注意的是
队数据溢出的处理。

（1）设置结果为long long类型，算完后直接比较是否溢出。

（2）每次算出结果后都/10与上次结果比较，如果溢出则结果不一样。

## 拓展与思考：
### 拓展
没有可以扩展的东西。
### 思考
本题主要处理溢出问题，其他都是常规问题。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！