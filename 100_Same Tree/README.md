# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 100_Same Tree（相同的树）
## 问题描述与输入输出
给定两个二叉树，编写一个函数来检验它们是否相同。

如果两个树在结构上相同，并且节点具有相同的值，则认为它们是相同的。

### 问题示例

	示例1：
	输入:      1         1
	          / \       / \
	         2   3     2   3

			[1,2,3],   [1,2,3]
	输出: true
	
	示例2：
	输入:      1          1
	          /           \
	         2             2
			[1,2],     [1,null,2]
	输出: false
	
	示例3：
	输入:       1         1
	           / \       / \
	          2   1     1   2
	        [1,2,1],   [1,1,2]
	输出: false

函数输入与输出：
* 输入：
	* struct TreeNode* p：树p的根节点指针
	* struct TreeNode* q: 树q的根节点指针
* 输出：
	* bool: 是否是相同的树

## 思路			
### 常规

	p空,q空,返回真
	p空q不空、q空p不空、二者都不空但是值不同返回假值
	否则就看他们左子树与右子树是不是都是相同的树
				 				 	
## 拓展与思考：
### 拓展
如果让你判断是不是同构的树，该怎么做？判断同构相对麻烦，不过也不难。
### 思考
根据性质即可验证是否是相同的树，代码也很简单。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！