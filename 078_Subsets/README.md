# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 078_Subsets（子集）
## 问题描述与输入输出
给定一组不含重复元素的整数数组 nums，返回该数组所有可能的子集（幂集）。

说明：解集不能包含重复的子集。

### 问题案例

	示例1：
	输入: nums = [1,2,3]
	输出:
	[
	  [3],
	  [1],
	  [2],
	  [1,2,3],
	  [1,3],
	  [2,3],
	  [1,2],
	  []
	]
	

函数输入与输出：
* 输入：
	* int* nums: 输入的数组数据
	* int numsSize:输入的数组数据的长度
	* int** columnSizes：columnSizes是一个指向一维数组指针的指针
	* int* returnSize：返回的子集的行数
	
* 输出：
	* int**：子集(二维数据)的二维指针。

## 思路			
### 基于子集树的回溯法

	函数名：void subsets_backTrack(int** data, const int* nums, const int numsSize, int** columnSizes, int* data_num, int* set, int depth)
	函数输入：	
		data是所有子集的二维指针
		nums是指向输入的数组的指针
		numsSize是输入的数组的长度
		columnSizes是一个指向各个组合的长度（数组形式）二维指针，也就是*columnSizes指向各个组合的长度（数组形式）二维指针
		data_num是当前寻找的是第几个组合
		set是遍历的子集集合的指针
		depth是遍历的深度
	
	函数流程：
		深度depth与numsSize相等时，此时根据set里面记录的内容(1代表有，0代表无)，复制数据
		否则记录set，并左右递归子集。
		
	例子：比如输入nums = [1,2]:
	则回溯的set分别是[0,0],[0,1],[1,0],[1,1]。
	递归结束后则子集是[0], [2], [1], [1, 2]
			
## 拓展与思考：
### 拓展
尝试有重复输入数据的[子集树II](https://leetcode-cn.com/problems/subsets-ii/description/)。
### 思考
回溯法很常用，主要包括排列数与子集树形式的两种回溯方式。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
