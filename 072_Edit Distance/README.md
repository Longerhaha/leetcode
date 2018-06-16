# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 072_Edit Distance（编辑距离）
## 问题描述与输入输出
给定两个单词 word1 和 word2，计算出将 word1 转换成 word2 所使用的最少操作数 。

你可以对一个单词进行如下三种操作：

	1. 插入一个字符
	2. 删除一个字符
	3. 替换一个字符


### 问题案例

	示例1：
	输入: word1 = "horse", word2 = "ros"
	输出: 3
	解释: 
	horse -> rorse (将 'h' 替换为 'r')
	rorse -> rose (删除 'r')
	rose -> ros (删除 'e')
	
	示例2：
	输入: word1 = "intention", word2 = "execution"
	输出: 5
	解释: 
	intention -> inention (删除 't')
	inention -> enention (将 'i' 替换为 'e')
	enention -> exention (将 'n' 替换为 'x')
	exention -> exection (将 'n' 替换为 'c')
	exection -> execution (插入 'u')

函数输入与输出：
* 输入：
	* char* word1:单词 word1的指针
	* char* word2:单词 word2的指针
	
* 输出：
	* int：将 word1 转换成 word2 所使用的最少操作数

## 思路			
### 动态规划

	dp[i][j]代表word1[0, 1, ..., i-1]与word2[0, 1, ..., j-1]间转化需要的最小操作
	1、如果word1[i-1]与word2[j-1]相等
	dp[i][j] = dp[i-1][j-1]  
	2、如果word1[i-1]与word2[j-1]不相等 
	(1)若执行替换操作，则dp[i][j] = dp[i-1][j-1]+1
	(2)若执行删除操作，则dp[i][j] = dp[i-1][j]+1
	(3)若执行插入操作，则dp[i][j] = dp[i][j-1]+1    
	归纳即dp[i][j] = min(dp[i-1][j-1], dp[i-1][j], dp[i][j-1])+1			
					 				 	
## 拓展与思考：
### 拓展
暂时没有想法。
### 思考
字符串的题目很经常转化为动态规划问题。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
