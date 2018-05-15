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
1. 动态规划:lp代表i与j字符是否存在回文路，使用该方法时间复杂度为O（n^2），空间复杂度为O（n）。

	状态方程如下：
	i=j时，lp[i][j]=1。
	i=j-1时，lp[i][j] = (d[i] == d[j])                    
	j-i>1时，d[i] == d[j]) && (lp[i+1,j-1])         
					
2. [Manacher算法](https://articles.leetcode.com/longest-palindromic-substring-part-ii/)
	该算法只能处理奇数个的字符串，但经过预处理之后既能处理奇数个也能处理偶数个。预处理也很简单，直接在头尾以及两个字符的中间插入'#'字符即可。
该算法充分利用了回文的对称性，平均时间复杂度为O（n），空间复杂度为O（n），最坏情况比如“aaaaaaaaaa”这种复杂度是O（n^2）。

## 拓展与思考：
### 拓展
	比如找DNA中的对称基因。
### 思考
	动态规划算法在leetcode上面没有pass，因为输入1000个重复字符的时候超出时间限制了，Manacher算法过了，显然Manacher算法更优（从平均复杂度以及最差复杂度）。当然还有其他办法，可参考[小鹅鹅的博客](https://blog.csdn.net/asd136912/article/details/78987624)
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
