# leetcode
# stick to it everyday and you will be a good algorithm engineer!
## 153_Find Minimun in Rotated Sorted Array（寻找旋转排序数组中的最小值）
## 问题描述与输入输出
假设按照升序排序的数组在预先未知的某个点上进行了旋转。

( 例如，数组 [0,1,2,4,5,6,7] 可能变为 [4,5,6,7,0,1,2] )。

请找出其中最小的元素。

你可以假设数组中不存在重复元素。

### 问题样例

	示例1：
	输入: 
	[3,4,5,1,2]
	输出: 
	1
	
	示例2：
	输入:
	[4,5,6,7,0,1,2]
	输出: 
	1
	

函数输入与输出：
* 输入：
	* int* nums：旋转排序数组的一级指针
	* int numsSize：旋转排序数组的长度
* 输出：
	* int: 旋转排序数组的最小值

## 思路			
### 二分查找

	start记录数组的起点，end记录数组的终点
	while( start < end && nums[start] > nums[end]) //保证是有旋转过的
		mid = (start + end)/2;
		if(nums[start] <= nums[mid])
            start = mid + 1;
        else
            end = mid;
	return nums[start];
	
	
## 拓展与思考：
### 拓展
如果数据有重复呢？
### 思考
基于链表结构的归并排序可以实现常数级空间复杂度，这是由于链表的结构特性。基于数组结构的归并排序的空间复杂度是O（n），
由于其合并必须合并到一个temp数组中；数组形式的堆排序的空间复杂度还是O（n）。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
