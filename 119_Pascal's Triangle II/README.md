# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 119_Pascal's Triangle II（杨辉三角 II）
## 问题描述与输入输出
给定一个非负索引 k，其中 k ≤ 33，返回杨辉三角的第 k 行。

__进阶__：
你可以优化你的算法到 O(k) 空间复杂度吗？
### 问题示例

	示例1：
	输入：
	3
	输出：
	[1,3,3,1]
	

函数输入与输出：
* 输入：
	* int rowIndex: 杨辉三角的第 rowIndex 行 
	* int* columnSizes: *columnSizes为第 rowIndex 行的个数
	
* 输出：
	* int* : 第 rowIndex 行杨辉三角的数据的指针。

## 思路			
### 数据暂存法

	优化到你的算法到 O(k) 空间复杂度
	意味这申请一片k长度的内存，只要算出每行后，将数据copy到改行，然后基于该片内存继续算下一行，如此反复直到最后一行。

	
## 拓展与思考：
### 拓展
暂无想法
### 思考
本题通过数据暂存可以实现O(k) 空间复杂度。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
