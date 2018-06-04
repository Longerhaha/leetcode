# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 031_next permutations(下一个排列)
## 问题描述与输入输出
	
### 问题描述
实现获取下一个排列的函数，算法需要将给定数字序列重新排列成字典序中下一个更大的排列。

如果不存在下一个更大的排列，则将数字重新排列成最小的排列（即升序排列）。

必须原地修改，只允许使用额外常数空间。



### 问题案例
	
	以下是一些例子，输入位于左侧列，其相应输出位于右侧列。
	1,2,3 → 1,3,2
	3,2,1 → 1,2,3
	1,1,5 → 1,5,1
		
### 输入与输出
* 输入：
	* int* nums：无重复数字的序列的头指针
	* numsSize：无重复数字的序列的个数
	
* 输出：void 必须原地修改，只允许使用额外常数空间

## 思路			
### 基于有条件交换的深度优先递归方法（回溯算法）

1. Find the largest index k such that nums[k] < nums[k + 1]. If no such index exists, the permutation is sorted in descending order,
just reverse it to ascending order and we are done. For example, the next permutation of [3, 2, 1] is [1, 2, 3].

步骤1 找到nums[k] < nums[k + 1]的最大k值。如果是-1，说明数据本身就是逆序了

2. Find the largest index l greater than k such that nums[k] < nums[l].

步骤2 找到最大的下标l使得nums[k] < nums[l]

3. Swap the value of nums[k] with that of nums[l].

步骤三 交换k与l

4. Reverse the sequence from nums[k + 1] up to and including the final element nums[nums.size() - 1].

步骤四 反转nums[k + 1]至nums[numsSize-1]

## 拓展与思考：
### 拓展
此题与全排列和全排列II相关，如果这题会了，全排列就简单了。
### 思考
此题的算法可以从回溯算法的全排列的叶子节点出发，稍微理解一下应该不难。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
