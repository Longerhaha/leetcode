# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 206_Reverse Linked List（反转链表）
## 问题描述与输入输出
反转一个单链表。

进阶:

你可以迭代或递归地反转链表。你能否用两种方法解决这道题？

### 问题样例

	示例1：
	输入: 1->2->3->4->5->NULL
	输出: 5->4->3->2->1->NULL
	

函数输入与输出：
* 输入：
	* struct ListNode* head：链表头结点指针

* 输出：struct ListNode* 反转后的头节点指针

## 思路			
### 三指针迭代反转链表法

	while( cur不为空 )
		cur的下一个节点指向pre
		调整pre、cur、next指针整体往后移动一个
						
					 				 	
## 拓展与思考：
### 拓展
按组反转链表，如92题，
### 思考
此题较为常规，明日把递归代码一起写了。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
