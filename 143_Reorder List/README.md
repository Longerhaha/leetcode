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
### 三指针迭代法反转链表

	while( cur不为空 )
		cur的下一个节点指向pre
		调整pre、cur、next指针整体往后移动一个

### 递归法反转链表
	
	函数形式struct ListNode* reverseList_recurse(struct ListNode* head, struct ListNode** reverse_head){ /*代码块*/ }
	if(head的下一个节点为空)
		记录反转链表后的头结点（*reverse_head = head）
		返回当前节点
	else
		递归调用其下一个节点的链表反转，并获得其反转后的尾巴节点pre
		反转：pre->next = head;
		返回当前节点
						
					 				 	
## 拓展与思考：
### 拓展
按组反转链表，如92题，
### 思考
补充了递归代码。值得注意的是递归代码的运行时间比三指针迭代法短，我估计是测试样例里面搞的鬼。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
