# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 040_Combinations Sum II（组合总和II）
## 问题描述与输入输出
给定一个数组 candidates 和一个目标数 target ，找出 candidates 中所有可以使数字和为 target 的组合。

candidates 中的每个数字在每个组合中只能使用一次。

_说明_：

	1. 所有数字（包括 target）都是正整数。
	2. 解集不能包含重复的组合。 
	
### 问题案例

	示例1：
	输入: candidates = [10,1,2,7,6,1,5], target = 8,
	所求解集为:
	[
	  [1, 7],
	  [1, 2, 5],
	  [2, 6],
	  [1, 1, 6]
	]
	
	输入: candidates = [2,5,2,1,2], target = 5,
	所求解集为:
	[
	  [1,2,2],
	  [5]
	]

函数输入与输出：
* 输入：
	* int* candidates: 待组合的数据数组指针
	* int candidatesSize: 待组合的数据数组的长度
	* int target：组合的目标值
	* int** columnSizes：一个指向各个组合的长度（数组形式）的指针
	* int* returnSize：可以组合为target的组合总数
	
* 输出：
	* int**：可以无重复组合为target的二维数据的二维指针。

## 思路			
### 回溯算法

	本题属于寻找无重复子集的问题，使用遵循深度优先搜索的回溯算法
	函数形式：int combinationSum_dfs(int** ans_data, const int* candidates, const int candidatesSize, const int target, int** columnSizes, int* cmbnSum_num, int depth, const int dfs_idx)
	函数输入：
		ans_data：组合二维数据的二维指针
		candidates：组合的数据的一维指针
		candidatesSize：组合的数组数据的长度
		target：查找目标
		columnSizes：指向一维组合长度数组的指针
		cmbnSum_num：递归到第几个组合和为target
		dfs_idx：递归到第几个数
		depth：记录递归深度	
	函数返回：
		1代表candidates[i]可以以它为首找到一个组合，根据返回是否为1可以跳过重复数据。
	函数流程：
	(1)target小于0则说明无法组合，于是递归结束
	(2)target等于0说明可以找到这样的一个组合，于是记录长度，继续查找下一个可能的组合。注意要申请下一个节点的空间并复制上个组合内容，防止*cmbnSum_num  改变后导致之前递归的数据丢失
	(3)target大于0则继续递归，递归从数dfs_idx开始递归，直到candidatesSize-1，每次递归深度depth+1。如果此次可以递归成功，那么就要跳过当前重复的数字。
## 拓展与思考：
### 拓展
我一直认为回溯就是深度优先搜索，但我一直对这个表示怀疑。于是百度了下[回溯与DFS的区别](http://www.cnblogs.com/ganganloveu/p/4188131.html),可以好好看看。
### 思考
组合类的问题做了三大题（39,40，77题），可以自己好好总结一下了，我自己做了回溯与DFS的区别的一个word文件，有需要可以联系我。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
