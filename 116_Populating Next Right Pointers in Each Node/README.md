# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 116_Populating Next Right Pointers in Each Node（填充同一层的兄弟节点）
## 问题描述与输入输出
给定一个二叉树

	struct TreeLinkNode {
	  TreeLinkNode *left;
	  TreeLinkNode *right;
	  TreeLinkNode *next;
	}

填充它的每个 next 指针，让这个指针指向其下一个右侧节点。
如果找不到下一个右侧节点，则将 next 指针设置为 NULL。
初始状态下，所有 next 指针都被设置为 NULL。

说明:

* 你只能使用额外常数空间。
* 使用递归解题也符合要求，本题中递归程序占用的栈空间不算做额外的空间复杂度。
* 你可以假设它是一个完美二叉树（即所有叶子节点都在同一层，每个父节点都有两个子节点）。


### 问题示例

	示例1：
	给定完美二叉树，
	输入：
		 1
	   /  \
	  2    3
	 / \  / \
	4  5  6  7
	输出：
		1 -> NULL
	   /  \
	  2 -> 3 -> NULL
	 / \  / \
	4->5->6->7 -> NULL
	

函数输入与输出：
* 输入：
	* struct TreeLinkNode *root：给定的二叉树头结点指针

* 输出：
	* void : 原地修改

## 思路			
### 双指针从上到下、从左到右遍历法

	如果没有next指针，想要利用双指针遍历整个树是不可能的。但是有了next指针，一切变得不一样了。
	从上到下（充分利用上层调整后的结果），从左到右一步步解决问题。
	p_level_bigin记录本层的最左边结点指针，p_level_travese记录本层的遍历节点指针
	比如：
		1
	   /  \
	  2    3
	 / \  / \
	4  5  6  7
	先遍历第一层：
		1 -> NULL
	   /  \
	  2    3
	 / \  / \
	4  5  6  7
	遍历第二层：
		1  -> NULL
	   /  \
	  2 -> 3 -> NULL
	 / \  / \
	4  5  6  7
	遍历第三层：
		1  -> NULL
	   /  \
	  2 -> 3 -> NULL
	 / \  / \
	4->5->6->7 -> NULL
				 				 	
## 拓展与思考：
### 拓展
本题很有意思，如果树具有这样的结果，层序遍历就太简单了。如果给定的数不是完美二叉树呢？
### 思考
本题有了next指针，我们可以从上到下一步一步解决问题，充分利用了next指针。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
