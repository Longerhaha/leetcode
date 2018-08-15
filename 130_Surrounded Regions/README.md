# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 130_Surrounded Regions（围绕的区域）
## 问题描述与输入输出
给定一个二维的矩阵，包含 'X' 和 'O'（字母 O）。

找到所有被 'X' 围绕的区域，并将这些区域里所有的 'O' 用 'X' 填充。


### 问题示例

	示例1：
	输入：
	X X X X
	X O O X
	X X O X
	X O X X
	输出：
	X X X X
	X X X X
	X X X X
	X O X X
	解释：
	被围绕的区间不会存在于边界上，换句话说，任何边界上的 'O' 都不会被填充为 'X'。 
	任何不在边界上，或不与边界上的 'O' 相连的 'O' 最终都会被填充为 'X'。
	如果两个元素在水平或垂直方向相邻，则称它们是“相连”的。


函数输入与输出：
* 输入：
	* char** board：输入区域矩阵的二级指针
	* int boardRowSize: 矩阵的行数
	* int boardColSize：矩阵的列数

* 输出：
	* void : 原地修改。

## 思路			
### BFS

	1. 队列初始化
    2. 边界BFS遍历，如果与边界'O'相邻的'O'标记为'*'
    3. 遍历board，将所有'O'修改为'X'、'*'修改为'O'
				 				 	
## 拓展与思考：
### 拓展
暂时没有想法？
### 思考
本题BFS需要从边界出发，否则如果你从内圈出发则你可能做了很多无用功。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
