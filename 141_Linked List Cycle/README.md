# leetcode
# stick to it everyday and you will be a good algorithm engineer!
## 141_Linked List Cycle（环形链表）
## 问题描述与输入输出
给定一个链表，判断链表中是否有环。

进阶：
你能否不使用额外空间解决此题？

要求算法的时间复杂度为 O(n)。


### 问题示例

	示例1：
	输入：
	NULL
	输出：
	false
	
	示例2：
	输入：
	1
	输出：
	false
	
	示例2：
	输入：
	1->2->3->4->5---
	      ^        |
		  |		   |
           ---------
	输出：
	true
	

函数输入与输出：
* 输入：
	* int* nums: 输入数组的指针
	* int numsSize: 输入数组的长度


* 输出：
	* struct ListNode *head: 链表头结点指针

## 思路			
### 快慢双指针法
	
	如果输入为空或者输入的链表只有一个节点则返回空。
	如果链表多个（大于等于2）节点：
		p_fast每次跨越两个节点，p_slow跨越一个节点
		while( p_fast不为空 )
			如果p_fast下一个节点为NULL，则更新p_fast为NULL，否则更新为其后的第二个节点的指针
			p_slow更新为下一个节点指针
			if（ p_fast == p_slow）
				返回true（环形链表）
	    返回false（单向链表）

## 拓展与思考：
### 拓展
如果存在环形链表，你能找出环形链表的头和尾巴吗？
### 思考
本题p_fast每次跨越两个节点，p_slow跨越一个节点可以保证存在环形链表的时候，二者肯定会相遇（即指针相等）的。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
