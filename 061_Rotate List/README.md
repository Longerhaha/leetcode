# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 061_Rotate List（旋转链表）
## 问题描述与输入输出
给定一个链表，旋转链表，将链表每个节点向右移动 k 个位置，其中 k 是非负数。

### 问题样例

	示例1：
	输入: 1->2->3->4->5->NULL, k = 2
	输出: 4->5->1->2->3->NULL
	解释:
	向右旋转 1 步: 5->1->2->3->4->NULL
	向右旋转 2 步: 4->5->1->2->3->NULL
	
	示例2：
	输入: 0->1->2->NULL, k = 4
	输出: 2->0->1->NULL
	解释:
	向右旋转 1 步: 2->0->1->NULL
	向右旋转 2 步: 1->2->0->NULL
	向右旋转 3 步: 0->1->2->NULL
	向右旋转 4 步: 2->0->1->NULL

函数输入与输出：
* 输入：
	* struct ListNode* head：链表头结点指针
	* int k：进行k次旋转

* 输出：struct ListNode* 旋转k次后的头节点指针

## 思路			
### 基于单次旋转的k次旋转链表

	先求链表的长度len。
	然后旋转k%len次链表（避免做没有意义的旋转，因为len的倍数旋转与原链表一样）。
						
					 				 	
## 拓展与思考：
### 拓展
此题相对于[k个一组翻转链表](https://leetcode-cn.com/problems/reverse-nodes-in-k-group/description/)较为简单。
### 思考
注意避免做没有意义的旋转，因为len的倍数旋转与原链表一样。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
