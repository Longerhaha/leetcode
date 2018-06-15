# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 092_Reverse Linked List II（反转链表II）
## 问题描述与输入输出
反转从位置 m 到 n 的链表。请使用一趟扫描完成反转。

### 问题样例

	示例1：
	输入: 1->2->3->4->5->NULL, m = 2, n = 4
	输出: 1->4->3->2->5->NULL
	

函数输入与输出：
* 输入：
	* struct ListNode* head：链表头结点指针
	* int m：反转部分从第m个节点开始
	* int n：反转部分在第n个节点结束

* 输出：struct ListNode* 反转后的头节点指针

## 思路			
### 一趟扫描反转

	1、记录反转部分链表的头（加入一个空头节点相对较容易操作）
	2、使用三个指针pre, cur, next反转
	3、待反转部分的未反转时头指向反转部分的后一个节点，反转部分的前一个节点指向该反转部分反转后的头。
						
					 				 	
## 拓展与思考：
### 拓展
此题相对于[k个一组翻转链表](https://leetcode-cn.com/problems/reverse-nodes-in-k-group/description/)较为简单。
### 思考
此题注意处理一些特殊情况即可。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
