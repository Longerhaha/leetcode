# leetcode
# stick to it everyday and you will be a good algorithm engineer!
## 889_根据前序和后序遍历构造二叉树
## 问题描述与输入输出
### 问题描述

返回与给定的前序和后序遍历匹配的任何二叉树。

pre 和 post 遍历中的值是不同的正整数。

提示：

1 <= pre.length == post.length <= 30

pre[] 和 post[] 都是 1, 2, ..., pre.length 的排列

每个输入保证至少有一个答案。如果有多个答案，可以返回其中一个。
 

### 问题示例

	示例1：
	输入: 
	pre = [1,2,4,5,3,6,7], post = [4,5,2,6,7,3,1]
	输出: 
	[1,2,3,4,5,6,7]

### 函数输入与输出：
* 输入：
	* int* pre:  前序遍历树的结果的一级指针
	* int preSize: 前序遍历树的结果的长度
	* int* post: 后序遍历树的结果的一级指针
	* int postSize: 后序遍历树的结果的长度
	
* 输出：
	* struct TreeNode*：根据先序和后序遍历构建的树的根节点指针

## 思路			
### 一分为二，递归构建

	提示里面说的很清楚了，根据先序和后序遍历构建的树的可能性有很多种，这也是这道题不常见的原因。
	在这里我们以pre[1]为界限，然后一分为二递归构造树。
	伪代码如下：
	构建pre[0]的树
	if(preSize等于1)
		则pre[0]的树的左右子树都为NULL
	else
		找出pre[1]在post中的位置idx
		//由于此时至少有两个节点，所以可以放心的递归左子树，但是要注意右子树，因为此时右子树可能不存在
		pre[0]的树->left = constructFromPrePost(pre + 1, idx + 1, post, idx + 1);
		pre[0]的树->right = idx == preSize - 2 ? NULL : constructFromPrePost(pre + 1 + (idx + 1), preSize - (1 + (idx + 1)), post + (idx + 1), postSize - (1 + (idx + 1)));
	返回pre[0]的树
	

## 拓展与思考：
### 拓展
从中序和先序遍历构造树、从中序和后序遍历构造树相对较为容易，代码也好写。
### 思考
本题答案不唯一，所以需要自己设定一些规则，这样好做算法的推演。
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
