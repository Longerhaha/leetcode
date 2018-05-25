# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 011_container with most water(盛最多水的容器)
## 问题描述与输入输出
	
### 问题描述
给定 n 个非负整数 a1，a2，...，an，每个数代表坐标中的一个点 (i, ai) 。画 n 条垂直线，使得垂直线i的
两个端点分别为 (i, ai) 和 (i, 0)。找出其中的两条线，使得它们与 x 轴共同构成的容器可以容纳最多的水。
### 问题案例
	示例1
	输入: [1 1] 
	输出: 1

	
### 输入与输出

* 输入：
	* int* height		存储输入高度数组的头指针
	* int heightSize	输入高度数组的长度
	
* 输出: int 盛最多的水的体积

## 思路			
使用两个指针，一个指针left，一个指针right，算出当前的体积area，每次左指针指向的高度若是比右指针指向
的高度低，则左指针向前一步，否则右指针向前一步，左右指针相等的时候则停止。在每次比较过程中，先算出
当前的area，并与先前最大体积maxArea比较。整个算法时间复杂度为O（n），空间复杂度为O（1），比暴力搜索法
（时间复杂度O（n^2））好很多。
## 拓展与思考：
### 拓展
把输出改成输出可以容纳最多的水的容器的位置，则在做比较体积的时候需要记录位置。本题可以与42题接雨水一起
总个总结，对此类问题会有更深刻的认识。
### 思考
本题使用了两个指针，把时间复杂度降了一个量级。19题删除倒数第n个的链表节点也使用了两个指针（进阶方法），
可见以后使用两个指针也是一个思路，说不定可以降低一个量级的时间复杂度呢！
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！