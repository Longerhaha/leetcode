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

	函数名：void subsets_backTrack(int** data, const int* nums, const int numsSize, int** columnSizes, int* data_num, int ele_num, int depth)
	函数输入：	
		data是所有子集的二维指针
		nums是指向输入的数组的指针
		numsSize是输入的数组的长度
		columnSizes是一个指向各个组合的长度（数组形式）二维指针，也就是*columnSizes指向各个组合的长度（数组形式）二维指针
		data_num是当前寻找的是第几个组合
		ele_num是当前子集包含的元素个数
		depth是遍历的深度
	
	函数流程：
		深度depth与numsSize相等时，此时记录本子集的长度到*columnSizes所指向的数组中，然后寻找下一个子集并拷贝上一个子集数据到下一个子集的数
		否则递归：
		（1）ele_num位置无子集元素，ele_num保持，深度depth加1，递归。
		（2）ele_num位置有子集元素为nums[depth]，ele_num加1，深度depth加1，递归。
		
	例子：比如输入nums = [1,2]:
	第1次递归ele_num=0，depth=0，ele_num位置无子集元素，ele_num保持，深度depth加1。
	第2次递归ele_num=0，depth=1，ele_num位置无子集元素，ele_num保持，深度depth加1。
	第3次递归ele_num=0，depth=2，depth==numsSize==2，递归结束，记录第1个子集为[]。
	回到第2次的递归，此时递归（1）结束，进行递归（2）
	第4次递归ele_num=0，depth=1，ele_num位置有子集元素[2]，ele_num+1，深度depth加1。
	第5次递归ele_num=1，depth=2，depth==numsSize==2，递归结束，记录第2个子集为[2]。
	回到第1次的递归，此时递归（1）结束，进行递归（2）
	第6次递归ele_num=0，depth=0，ele_num位置有子集元素[1]，ele_num+1，深度depth加1。
	第7次递归ele_num=1，depth=1，ele_num位置无子集元素，ele_num保持，深度depth加1。
	第8次递归ele_num=1，depth=2，depth==numsSize==2，递归结束，记录第3个子集为[1]。
	回到第7次的递归，此时递归（1）结束，进行递归（2）
	第9次递归ele_num=1，depth=1，ele_num位置有子集元素[2]，此时子集是[1,2],ele_num+1，深度depth加1。
	第10次递归ele_num=1，depth=2，depth==numsSize==2，递归结束，记录第4个子集为[1,2]。
	综上，子集是[[], [2], [1], [1,2]]
			
## 拓展与思考：
### 拓展
尝试有重复输入数据的[子集树II](https://leetcode-cn.com/problems/subsets-ii/description/)。
### 思考
回溯法很常用，主要包括排列数与子集树形式的两种回溯方式。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
