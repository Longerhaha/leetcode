# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 024_Swap Nodes in Pairs（两个一组交换链表中的节点）
## 问题描述与输入输出

### 问题描述

给定一个链表，两两交换其中相邻的节点，并返回交换后的链表。

你的算法只能使用常数的额外空间。

你不能只是单纯的改变节点内部的值，而是需要实际的进行节点交换。

### 问题案例

	示例1：
	给定 1->2->3->4, 你应该返回 2->1->4->3.

## 思路			

	该题等效于2个一组反转链表
	1. 建立空头节点，方便处理。
	2. 初始化上一个反转链表的尾巴与下一个反转链表的头
	3. 2个一组反转链表
	4. 释放空头结点的内存并返回head
	
	反转链表：
	K个一组反转链表
	K个一组也适用2个一组
	pre_reversed_tail记录上一个已反转链表的尾巴
	nextGroupHead记录下一组待反转链表的头（可能反转也可能不反转）
	
	ret指向该反转链表反转后的尾巴，即该反转链表的头
	pre指向反转链表的第一个节点
	cur指向反转链表的第二个节点
	next指向反转链表的第三个节点
	
	反转规则：当next不是下一个反转链表的头，则反转cur所指向的节点，即cur->next = pre，然后整体又移一个节点，直到next与nextGroupHead相等。
	
	例子：  tmpHead(临时空头节点)  -> 1 -> 2 -> 3 -> 4
			pre_reversed_tail=tmpHead，因为是两个一组反转，所以nextGroupHead为第三个节点的指针，即数据3的指针。
			tmpHead(临时空头节点)  -> 1   ->   2   ->   3   ->   4
									pre      cur      next
			1、next与nextGroupHead相等，直接跳出大循环
			2、tmpHead  -> 1   ->   2   ->   3   ->   4 
	
						  pre  <-  cur <-|   next  <-|
                           |             |           |
						   --------------|------------
			  pre_reversed_tail-----------
            第一次反转后变成：
                tmpHead  -> 2   ->   1   ->   3   ->   4  
			继续反转3,4：
				tmpHead  -> 2   ->   1   ->   4   ->   3  
 
	
## 拓展与思考：
### 拓展
如果按照浙江大学陈越老师数据结构课里面的反转链表给出的数据结构，你如何做反转链表？

    结构如下：
	struct ListNode {
		int address;
		int val;
		int next_address;
	};
	
### 思考
本题使用于K个一组翻转。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
