# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 064_Minimum Path Sum（最小路径和）
## 问题描述与输入输出
给定一个包含非负整数的 m x n 网格，请找出一条从左上角到右下角的路径，使得路径上的数字总和为最小。

说明：每次只能向下或者向右移动一步。


### 问题案例

	示例1
	输入:
	[
	  [1,3,1],
	  [1,5,1],
	  [4,2,1]
	]
	输出: 7
	解释: 因为路径 1→3→1→1→1 的总和最小。

函数输入与输出：
* 输入：
	* int** grid：网格的二维数据的头结点指针
	* int gridRowSize：网格的二维数据的行数
	* int gridColSize：网格的二维数据的列数
	
* 输出：int 网格[0][0]至[gridRowSize-1][gridColSize-1]的最小路径和

## 思路			
### 动态规划

	每次只能向下或者向右移动一步
	dp[i][j] = min(dp[i-1][j], dp[i][j-1])+grid[i][j]				
					 				 	
## 拓展与思考：
### 拓展
本题限制了移动的方向，如果不限制方向呢？即上下左右甚至对角线都可以走，这样子如何dp的公式又会变成什么？
### 思考
如果你会动态规划，这道题应该很基础。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！