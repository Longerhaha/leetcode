# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 105_Construct Binary Tree from Preorder and Inorder Traversal（从前序与中序遍历序列构造二叉树）
## 问题描述与输入输出
根据一棵树的前序遍历与中序遍历构造二叉树。

_注意_:
你可以假设树中没有重复的元素。

### 问题示例

	示例1：
	输入：
	前序遍历 preorder = [3,9,20,15,7]
	中序遍历 inorder = [9,3,15,20,7]
	输出:
	    3
	   / \
	  9  20
		/  \
	   15   7
	

函数输入与输出：
* 输入：
	* int* preorder：前序遍历数组指针
	* int preorderSize: 前序遍历数组长度
	* int* inorder：中序遍历数组指针
	* int* inorderSize：中序遍历数组指针
* 输出：
	* struct TreeNode* buildTree: 构建的树的头结点指针

## 思路			
### 递归
	
	根据前序遍历第一个值在中序遍历的位置兵分两路，左右递归
	在查找位置的时候(int pos = 0)，for(; pos<inorderSize && inorder[pos]!=*preorder; pos++)
	pos等于0说明其没有左子树了，但是还可能有右子树，这时候需要根据preorderSize判断
	preorderSize为1说明没有右子树，否则递归右子树
		
## 拓展与思考：
### 拓展
如果让你从后续遍历数组与中序遍历数组构建树呢？
### 思考
本题较为常规。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
