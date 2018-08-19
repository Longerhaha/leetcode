# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 148_Sort List（排序链表）
## 问题描述与输入输出
在 O(n log n) 时间复杂度和常数级空间复杂度下，对链表进行排序。

### 问题样例

	示例1：
	输入: 4->2->1->3
	输出: 1->2->3->4
	
	示例2：
	输入: -1->5->3->4->0
	输出: -1->0->3->4->5
	

函数输入与输出：
* 输入：
	* struct TreeNode* head：链表的头结点指针
* 输出：
	* struct TreeNode*: 排序后的链表的头结点指针

## 思路			
### 归并排序(O(n log n) 时间复杂度、常数级空间复杂度)

	1.快慢双指针法拆分前后链表
	2.递归前链表，递归后链表
	3.合并链表
	
### 堆排序(O(n log n) 时间复杂度、O(n)空间复杂度)

	1.堆初始化
	2.建立基于链表结构数据的堆
	3.一个个更新链表结构数据为堆中删除的数直至链表的尾巴
	
## 拓展与思考：
### 拓展
数组形式的归并排序的空间复杂度是O（n）还是O（1）？数组形式的堆排序的空间复杂度还是O（n）吗？
你可以使用快排解决这问题吗？快排对应的空间复杂度是多少？
### 思考
基于链表结构的归并排序可以实现常数级空间复杂度，这是由于链表的结构特性。基于数组结构的归并排序的空间复杂度是O（n），
由于其合并必须合并到一个temp数组中；数组形式的堆排序的空间复杂度还是O（n）。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！