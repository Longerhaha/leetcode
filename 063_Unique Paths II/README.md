# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 063_Unique Paths II（不同路径II）
## 问题描述与输入输出
一个机器人位于一个 m x n 网格的左上角 （起始点在下图中标记为“Start” ）。

机器人每次只能向下或者向右移动一步。机器人试图达到网格的右下角（在下图中标记为“Finish”）。

现在考虑网格中有障碍物。那么从左上角到右下角将会有多少条不同的路径？

网格中的障碍物和空位置分别用 1 和 0 来表示。
### 问题案例

	示例1
	输入:
	[
	  [0,0,0],
	  [0,1,0],
	  [0,0,0]
	]
	输出: 2
	解释:
	3x3 网格的正中间有一个障碍物。
	从左上角到右下角一共有 2 条不同的路径：
	1. 向右 -> 向右 -> 向下 -> 向下
	2. 向下 -> 向下 -> 向右 -> 向右

函数输入与输出：
* 输入：
	* int** obstacleGrid: 障碍物二维矩阵的头结点指针
	* int obstacleGridRowSize：网格的二维数据的行数
	* int obstacleGridColSize：网格的二维数据的列数
	
* 输出：机器人从起点到终点的不同路径总数。

## 思路			
### 动态规划

	每次只能向下或者向右移动一步，由于有障碍物，需要考虑障碍物
	dp[i][j] = obstacleGrid[i][j]==1?0:(dp[i-1][j]*(1-obstacleGrid[i-1][j])+dp[i][j-1]*(1-obstacleGrid[i][j-1]));		
					 				 	
## 拓展与思考：
### 拓展
动态规划方法解这类问题非常有效！
### 思考
如果你会动态规划，这道题在62题[不同路径上](https://leetcode-cn.com/problems/unique-paths/description/)稍微拐个弯就行了。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
