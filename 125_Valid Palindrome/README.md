# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 125_Valid Palindrome（验证回文串）
## 问题描述与输入输出
给定一个字符串，验证它是否是回文串，只考虑字母和数字字符，可以忽略字母的大小写。

说明：本题中，我们将空字符串定义为有效的回文串。

### 问题示例

	示例1：
	输入：
	"A man, a plan, a canal: Panama"
	输出：
	true


	示例2：
	输入：
	"race a car"
	输出：false
		


函数输入与输出：
* 输入：
	* char* s: 待判断的字符串的指针

* 输出：
	* bool : 是否是回文串。

## 思路			
### 常规
	
	start记录当前第一个需要判断的有效字符，end记录当前最后一个需要判断的有效字符
	while( start < end )
		(1)如果start下标下的字符不是有效字符且start < end，则start++，直到找到有效字符
		(2)如果end下标下的字符不是有效字符且start < end，则end--，直到找到有效字符
		(3)注意此时有可能start等于end而且该位置上是无效字符，此时就可以返回true了
		(4)否则如果start下标下的字符和end下标下的字符都是数字则判断他们是否相等，如果是字母则判断他们是否相差32，如果不是则返回false,如果是则start++, end--
	返回true	
	
## 拓展与思考：
### 拓展
暂无扩展想法。
### 思考
本题思路较为常规，注意while循环中的第四步，如果你单单判断相差32就错了，比如数字0和字符P就相差了32。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
