# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 019_remove nth node from the end of list(删除链表的倒数第n个节点)
## 问题描述与输入输出
	
### 问题描述
给定一个链表，删除链表的倒数第 n 个节点，并且返回链表的头结点。

### 问题案例
	示例1
	给定一个链表: 1->2->3->4->5, 和 n = 2.
	当删除了倒数第二个节点后，链表变为 1->2->3->5.
	
	
### 输入与输出

* 输入：
	struct ListNode* head 链表的头节点指针
	int n                 链表的倒数第n个节点
	
* 输出: struct ListNode* 删除链表的倒数第n个节点后的链表头节点指针

## 思路			
### 常规
先求链表的长度，然后再删除第（len-n）个节点。
### 进阶
使用两个搜索指针search1,search2，其间隔n，search1搜索到尾巴节点后，则删除search2后的节点。_注意删除头节点指针的处理_。
## 拓展与思考：
### 拓展
可以了解下链表的相关扩展和知识。
### 思考
该题相比于删除第n个节点稍微转了一下脑筋，进阶的思路很有意思，相信在很多地方可以用到这样的想法。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！