# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 008_string to integern(字符串转整数)
## 问题描述与输入输出
	
### 问题描述
实现 atoi，将字符串转为整数。

在找到第一个非空字符之前，需要移除掉字符串中的空格字符。如果第一个非空字符是正号或负号，选取该符号，并将其与后面尽可能多的连续的数字组合起来，这部分字符即为整数的值。如果第一个非空字符是数字，则直接将其与之后连续的数字字符组合起来，形成整数。

字符串可以在形成整数的字符后面包括多余的字符，这些字符可以被忽略，它们对于函数没有影响。

当字符串中的第一个非空字符序列不是个有效的整数；或字符串为空；或字符串仅包含空白字符时，则不进行转换。

若函数不能执行有效的转换，返回 0。
	
假设我们的环境只能存储 32 位有符号整数，其数值范围是 [−2^31,  2^31 − 1]。如果数值超过可表示的范围，则返回  INT_MAX (2^31 − 1) 或 INT_MIN (−2^31) 。
### 问题案例
	示例1
	输入: "42"
	输出: 42
	
	示例2
	输入: "   -42"
	输出: -42
	解释: 第一个非空白字符为 '-', 它是一个负号。
    我们尽可能将负号与后面所有连续出现的数字组合起来，最后得到 -42 。

	示例3
	输入: "4193 with words"
	输出: 4193
	解释: 转换截止于数字 '3' ，因为它的下一个字符不为数字。
	
	示例4
	输入: "words and 987"
	输出: 0
	解释: 第一个非空字符是 'w', 但它不是数字或正、负号。
	因此无法执行有效的转换。
	
	示例5
	输入: "-91283472332"
	输出: -2147483648
	解释: 数字 "-91283472332" 超过 32 位有符号整数范围。 
	因此返回 INT_MIN (−231) 。
	
### 输入与输出

* 输入：char* str 待转换的字符串
	
* 输出: int 字符串转之后的整数

## 思路			
本题主要根据题目所提供的规则构造最后转换出来的整数。里面很多细节，大家好好把握。
## 拓展与思考：
### 拓展
根据一些规则把需要的东西提取出来。
### 思考
leetcode上面看起来越简单的题目，里面的细节问题越多，这也是锻炼一下大家对可能出现bug的预判以及对问题思考的全面性。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
