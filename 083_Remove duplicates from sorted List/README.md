# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 083_Remove duplicates from sorted List(删除排序链表中的重复元素)
## 问题描述与输入输出
### 问题描述
给定一个排序链表，删除所有重复的元素，使得每个元素只出现一次。

### 问题样例：

	示例1：
	输入: 1->1->2
	输出: 1->2
	
	示例2：
	输入: 1->1->2->3->3
	输出: 1->2->3

### 输入与输出
* 输入：
	* struct ListNode* head：有序链表的头指针。
* 输出
	* struct ListNode*：删去重复元素后的有序链表的头指针。


## 思路			
### 常规法

	cur指向当前节点的指针
	pre指向之前节点的指针
	如果cur->val == pre->val则跳过该节点
	
## 拓展与思考
### 拓展
删除过程中，保留了重复元素的一个节点。如要要赶尽杀绝（比如淘宝天猫防黄牛系统），那么又要怎么做？快来试一下[删除排序链表中的重复元素 II](https://leetcode-cn.com/problems/remove-duplicates-from-sorted-list-ii/description/)。
### 思考
本题较为常规，但这里面有个细节值得思考。你把重复元素的节点空间释放掉了吗，如果你没有释放掉，那你的程序可是很危险的。
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
