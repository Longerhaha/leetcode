# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 028_Implement strStr()(实现strStr())
## 问题描述与输入输出
	
### 问题描述
实现 strStr() 函数。

给定一个 haystack 字符串和一个 needle 字符串，在 haystack 字符串中找出 needle 字符串出现的第一个位置 (从0开始)。

如果不存在，则返回  -1。

当 needle 是空字符串时，我们应当返回什么值呢？这是一个在面试中很好的问题。

对于本题而言，当 needle 是空字符串时我们应当返回 0 。这与C语言的 strstr() 以及 Java的 indexOf() 定义相符。

### 问题案例
	
	示例1
	输入: haystack = "hello", needle = "ll"
	输出: 2
	
	示例2
	输入: haystack = "aaaaa", needle = "bba"
	输出: -1
		
### 输入与输出
* 输入：
	* char* haystack:haystack 字符串的头指针
	* char* needle:needle 字符串的头指针
	
* 输出：int ：在 haystack 字符串中找出 needle 字符串出现的第一个位置

## 思路			
### 字符串处理实现strStr()

对每个位置检测，检测从它开始到其之后nLen位置的数据，如果符合则返回该位置。

## 拓展与思考：
### 拓展
此题较为简单，可以查看JAVA、C、Python源码比较一下自己写的函数。
### 思考
此题的解法较为简单，对复杂度也没要求。

# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
