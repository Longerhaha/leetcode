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
### 朴素字符串匹配算法

对每个位置检测，检测从它开始到其之后nLen位置的数据，如果符合则返回该位置。
### [KMP算法](https://blog.csdn.net/v_july_v/article/details/7041827)
#### 1.求next数组

《next 数组》是《最大长度表》数据整体向右移1个单位，舍去溢出位置（超出数组的位置）并对缺失位置（数组第一个位置）补充-1

比如：最大长度表    0 0 0 0 1 2 3
      next 数组  -1 0 0 0 0 1 2
	  
求next数组思路
* k=next[j]
* 若 needle[k] == next[j]，则k=k+1，同时j往后走，注意要分needle[j]是否与needle[next[j]]相等去给needle[j]定值
* 若 needle[k] != next[j]，则递归next[k]去找最小匹配

#### 2.遍历haystack求是否匹配

使用i遍历haystack（不回溯），j遍历needle
* 在每个当前i和j判断是否匹配
	* 若不匹配根据next指针调整j(j=next[j])，
	* 若匹配则判断是否是最大匹配

## 拓展与思考：
### 拓展
此题朴素字符串匹配算法简单易懂，KMP算法相对较难，需要仔细去思考一下，思考完就觉得不是那么难了。此外还有BM与Sunday算法。
### 思考
KMP算法时间复杂度是O（n+m），但是需要预处理。朴素字符串匹配算法时间复杂度为O((n-m+1)m)，复杂度相对较高，不需要预处理。

# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
