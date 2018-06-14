# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 073_Set Matrix Zeroes（矩阵置0）
## 问题描述与输入输出
给定一个 m x n 的矩阵，如果一个元素为 0，则将其所在行和列的所有元素都设为 0。请使用原地算法。


### 问题案例

	示例1：
	输入: 
	[
	  [1,1,1],
	  [1,0,1],
	  [1,1,1]
	]
	输出: 
	[
	  [1,0,1],
	  [0,0,0],
	  [1,0,1]
	]
	
	示例2：
	输入: 
	[
	  [0,1,2,0],
	  [3,4,5,2],
	  [1,3,1,5]
	]
	输出: 
	[
	  [0,0,0,0],
	  [0,4,5,0],
	  [0,3,1,0]
	]

函数输入与输出：
* 输入：
	* int** matrix:矩阵的数据的二维指针
	* int matrixRowSize：矩阵数据的行
	* int matrixColSize：矩阵数据的列
	
* 输出：
	* void 无

## 思路			
### 额外空间复杂度为O（m+n）

	row_zero记录行是否有0
	clo_zero记录列是否有0
	根据row_zero行置0
	根据clo_zero列置0			
				
### 额外空间复杂度为O（1）	

	row_zero空间换成matrix的第一列空间,即matrix[0][0],matrix[1][0]....,matrix[matrixRowSize-1][0]（为0才置0，否则不动，即保持原数据）
	row_zero空间换成matrix的第一行空间,即matrix[0][0],matrix[0][1]....,matrix[0][matrixColSize-1]（为0才置0，否则不动，即保持原数据）
	根据row_zero行置0
	根据clo_zero列置0
			
## 拓展与思考：
### 拓展
暂无拓展想法。
### 思考
本题较为简单，在额外空间复杂度上有三种解决方法。额外空间复杂度为O（m+n）也容易想到，额外空间复杂度为O（1）也不难。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
