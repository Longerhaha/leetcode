# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 107_Binary Tree Level Order Traversal II（二叉树的层次遍历 II）
## 问题描述与输入输出
给定一个二叉树，返回其节点值自底向上的层次遍历。 （即按从叶子节点所在层到根节点所在的层，逐层从左向右遍历）
### 问题示例

	示例1：
	输入：
	给定二叉树: [3,9,20,null,null,15,7],
	  3
	 / \
	9  20
      /  \
	 15   7
	输出:
	[
	  [15,7],
	  [9,20],
	  [3] 
	]
	

函数输入与输出：
* 输入：
	* struct TreeNode* root：二叉树的根节点指针
	* int** columnSizes：（*columnSizes）是指向数组的指针，也就是说columnSizes是二级指针
	* int* returnSize：*returnSize为二叉树的层数（深度）。
* 输出：
	* int**: 自底向上的层次遍历结果的二级指针

## 思路			

### 基于队列和BFS的反序存储层次遍历
	
	1.先获取树的高度
	2.[利用队列和BFS从高到低层次遍历](https://github.com/Longerhaha/leetcode/tree/master/102_Binary%20Tree%20Level%20Order%20Traversal)，反序存储。
	
		
## 拓展与思考：
### 拓展
如果让你从最底层锯齿形遍历最高层呢？与本题类似，利用[二叉树的锯齿形层次遍历](https://leetcode-cn.com/problems/binary-tree-zigzag-level-order-traversal/description/),然后反序存储。
### 思考
反序的思路是最简单的。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
