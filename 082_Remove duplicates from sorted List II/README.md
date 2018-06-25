# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 082_Remove duplicates from sorted List II(删除排序链表中的重复元素II)
## 问题描述与输入输出
### 问题描述
给定一个排序链表，删除所有含有重复数字的节点，只保留原始链表中__没有重复出现__的数字。

### 问题样例：

	示例1：
	输入: 1->2->3->3->4->4->5
	输出: 1->2->5
	
	示例2：
	输入: 1->1->1->2->3
	输出: 2->3

### 输入与输出
* 输入：
	* struct ListNode* head：有序链表的头指针。
* 输出
	* struct ListNode*：删去重复元素后的有序链表的头指针。


## 思路			
### 常规法

	1. 建立空头结点
	2. 若有重复元素，跳过重复元素，否则整体向右一个有效单元
	   跳过重复元素：
		(i) pre指向cur前一个元素，cur指向当前元素，next指向后一个元素
		(ii)当cur与next指向节点的值相同时，则移动next，保持pre与cur不变，知道next指向节点的值与cur指向的节点的值不一样（注意释放重复节点空间）。
			当cur与next指向节点的值不同时，整体向后移动一个单位
	3. 删除空头结点
	例1：空头节点->  1  ->  1  -> NULL
			pre     cur    next
		 cur->val == next->val,保持 pre与cur不变， next往后移动一个  
		    pre     cur           next
	     next等于NULL，跳出
         next等于NULL，意味着后面没有元素，pre指向NULL，跳出
		 输出[]       
	例2：空头节点 ->  1  ->  1  ->  2  -> NULL
			 pre    cur   next
		cur->val == next->val且后面有元素，保持 pre与cur不变， next往后移动一个  
		空头节点 ->  1  ->  1  ->  2  -> NULL
			pre     cur           next
		cur->val != next->val
		空头节点               ->  2  -> NULL 
			pre                  cur     next
		进入while大循环，此时next等于NULL，退出
		输出[2]
	
## 拓展与思考
### 拓展
淘宝系统将黄牛（比如地址一样）的数据从下单链表中删除掉，可以使用这种方法的实现。
### 思考
本题为了将重复元素赶尽杀绝，需要多使用一个指针，即使用三个指针。同时跳过重复元素过程中需要将节点内存释放掉。
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
