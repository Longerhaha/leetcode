# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 077_Combinations（组合）
## 问题描述与输入输出
给定两个整数 n 和 k，返回 1 ... n 中所有可能的 k 个数的组合。

### 问题案例

	示例1：
	输入: n = 4, k = 2
	输出:
	[
	  [2,4],
	  [3,4],
	  [2,3],
	  [1,2],
	  [1,3],
	  [1,4],
	]
	

函数输入与输出：
* 输入：
	* int n: 输入的数据为1,2,...,n
	* int k: k个数进行组合
	* int** columnSizes：columnSizes是一个指向一维数组的指针
	* int* returnSize：返回的数据的行数
	
* 输出：
	* int**：组合后的二维数据的二维指针。

## 思路			
### 带有剪枝的深度优先遍历

	1.首先计算C（n，k），注意计算对称性。
	2.申请需要的空间。
	3.深度递归求解
	    深度递归void combine_dfs(int** ans, int* nums, int n, int k, int* p_cnt_ans, int high, int pre_size)
		ans是组合结果二维数据的指针
		nums是包含待组合数据的数组头结点指针
		n是包含待组合数据的数组的长度
		k是从n个里面选取k个数进行组合
		p_cnt_ans记录组合个数的指针
		high是递归时的深度，最高层为0层，往下不断递加
		pre_size是上一层递归的数的大小
		比如本题(有剪枝)：
		
		high=0:     1           2            3
		            |           |            |
		         -------     -------      -------
		         |  |  |        |  |            |
		high=1:  2  3  4        3  4            4
		
		      剪枝：下一级递归从上一级的数据+1，递归到上一层递归最大递归数据加1
		high=k时：
		      直接复制数据
			
## 拓展与思考：
### 拓展
组合类的问题还有很多，如[组合总和](https://leetcode-cn.com/problems/combination-sum/description/),[组合总和II](https://leetcode-cn.com/problems/combination-sum-ii/description/).
### 思考
组合类的问题很多，都可以用回溯法来做，本题带有剪枝。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
