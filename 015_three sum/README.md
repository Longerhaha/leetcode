# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 015_three sum(三数之和)
## 问题描述与输入输出

### 问题描述

给定一个包含 n 个整数的数组 nums，判断 nums 中是否存在三个元素 a，b，c ，使得 a + b + c = 0 ？找出所有满足条件且不重复的三元组。

### 问题案例

	例如, 给定数组 nums = [-1, 0, 1, 2, -1, -4]，

	满足要求的三元组集合为：
	[
	  [-1, 0, 1],
	  [-1, -1, 2]
	]
 
## 思路			
* _暴力搜索法_  太暴力了，算法复杂度为O（n^3）。
* _哈希搜索法_  先排序，然后全部送进去哈希表。二重遍历i和j，再判断第三个数是否在hash表内，算法复杂度O（n^2）+O(nlogn),
其中O(n^2)是两次遍历，O(nlogn)是排序。需要注意的是，哈希表在判断重复的三元组上稍微麻烦了一点，而且空间复杂度高，建议还是使用三下标法。
* _三下标法_    先排序，外层一个i下标遍历，内层两个指针配合遍历（j=i+1,k=len-1）。算法复杂度O（n^2）+O(nlogn),
其中O(n^2)是两次遍历，O(nlogn)是排序。相比于哈希搜索法，三下标在判断重复的三元组较为简单。

## 拓展与思考：
### 拓展
二数之和、三数之和、三数最近和、四数之和，这系列的题目非常锻炼了你对数据结构的认识，建议好好总结，说不定就是你以后的面试题目。
	
### 思考
三下标法其实就是二下标（指针）法的进一步扩展，在两数之和这道题目上，由于双下标需要排序，时间复杂度为（O(nlogn)）弱于哈希搜索的
O（n）。但在多数之和（>=3）其优势就特别明显了，而且其空间复杂度是O（1）。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
