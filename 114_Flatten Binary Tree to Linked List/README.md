# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 114_Flatten Binary Tree to Linked List（二叉树展开为链表）
## 问题描述与输入输出
给定一个二叉树，原地将它展开为链表。


### 问题示例

	示例1：
	输入：
	    1
	   / \
	  2   5
	 / \   \
	3   4   6
	输出：
	1
	 \
	  2
	   \
		3
		 \
		  4
		   \
			5
			 \
			  6



函数输入与输出：
* 输入：
	* struct TreeNode* root：二叉树的根节点指针

* 输出：
	* void : 原地修改指针

## 思路			
### DFS

	左递归、右递归，然后将当前root的right指向最左边的节点，做左边节点的右子树指向右子树。
				 				 	
## 拓展与思考：
### 拓展
暂无想法，非平衡树似乎用处不大。
### 思考
本题较为常规。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
