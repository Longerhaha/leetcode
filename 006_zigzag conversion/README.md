# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 006_zigzag conversion(Z字形变换)
## 问题描述与输入输出
	
### 问题描述
将字符串 "PAYPALISHIRING" 以Z字形排列成给定的行数：
	
	P   A   H   N
	A P L S I I G
	Y   I   R

之后从左往右，逐行读取字符："PAHNAPLSIIGYIR"	
实现一个将字符串进行指定行数变换的函数:

	string convert(string s, int numRows);
	
	
### 问题案例
	示例1
	输入: s = "PAYPALISHIRING", numRows = 3
	输出: "PAHNAPLSIIGYIR"
	
	示例2
	输入: s = "PAYPALISHIRING", numRows = 4
	输出: "PINALSIGYAHRPI"
	解释:

	P     I    N
	A   L S  I G
	Y A   H R
	P     I
	
### 输入与输出

* 输入：
	char* s 	待转换的字符串头指针
	int numRows z字形排列的行数
	
* 输出: char* Z字形变换后的字符串头指针

## 思路			
本题主要抓住数据的分布特征，第一行和最后一行是个等差数列，差是2*numRows-2。其他行也有特征，详情见代码。
## 拓展与思考：
### 拓展
没有可以扩展的东西。
### 思考
本题主要抓住数据的分布特征。对于z字形排列的行数为1行、2行的稍加特殊处理就可以。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
