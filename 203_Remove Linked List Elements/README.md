# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 203_Remove Linked List Elements（删除链表中的节点）
## 问题描述与输入输出
删除链表中等于给定值 val 的所有节点。

### 问题样例

	示例1：
	输入: 
	1->2->6->3->4->5->6, val = 6
	输出:
	1->2->3->4->5
	

函数输入与输出：
* 输入：
	* struct ListNode* head：链表头结点指针
	* int val：待从链表中删除的节点的值

* 输出：struct ListNode*：删除节点val后的链表
## 思路			
### 常规法

	1.建立头空节点，方便操作
	2.遍历节点，tmp记录当前节点，next记录当前节点的后一个节点。
	  next一直往后一步直到next的值不为val，然后tmp指向该next。
						
					 				 	
## 拓展与思考：
### 拓展
暂无想法。
### 思考
此题较为常规，增加头空节点方便代码的书写。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
