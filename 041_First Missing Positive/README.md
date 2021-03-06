# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 041_First Missing Positive(缺失的第一个正数)
## 问题描述与输入输出
	
### 问题描述
给定一个未排序的整数数组，找出其中没有出现的最小的正整数。

_你的算法的时间复杂度应为O(n)，并且只能使用常数级别的空间_。
### 问题案例
	
	示例1 
	输入: [1,2,0]
	输出: 3
	
	示例2
	输入: [3,4,-1,1]
	输出: 2
	
	示例3
	输入: [7,8,9,11,12]
	输出: 1
	
### 输入与输出

* 输入：
	* int* nums:输入的未排序的整数数组
	* int numsSize:输入的未排序的整数数组的长度
* 输出:
	* int：缺失的第一个正数

## 思路			

### [规则存放](https://blog.csdn.net/Jaster_wisdom/article/details/80660467)

    必须说这个思路太巧了，我是想过排序和哈希，都没满足题目的要求。
	思路就是：nums[i]存放正数i+1。
	1、你需要从i=0到numsSize-1遍历，若当前的位置的值大于0小于等于numsSize且nums[nums[i]-1]的位置不是i，
	    则交换nums[i]与nums[(nums[i]-1)]。注意交换后仍需判断该位置是否是符合规则的。
	2、然后从头开始根据规则（nums[i]存放正数i+1）寻找最小缺失的正数，比如第一个步骤调整后的数据为[1 -1 3 4]，你就知道第一个缺失的正数是2。
	
	下面给大家举例：
	比如输入[3 4 -1 1]
		第一次判断第一个位置i=0, 此位置的值是3，因此交换3与-1，变为[-1 4 3 1],此时继续判断第一个数，其是-1，跳出while循环，i+1
		第二次判断第二个位置i=1，此位置的值是4，因此交换4与1，变为[-1 1 3 4],此时继续判断第二个数，其是1，交换-1与1，变换[1 -1 3 4]，继续判断第一个数，其是-1，跳出while循环，i+1
		第三次判断第三个位置i=2，刚好是3，跳出while循环，i+1
		第四次判断第三个位置i=3，刚好是4，跳出while循环并跳出for循环      
		一轮后的结果是[1 -1 3 4]，于是缺失的最小正数是2
		如果在第二次判断时没有继续判断，即while改成if，则结果将会是[-1 1 3 4]，缺失的最小正数是1，结果错误
		

## 拓展与思考：
### 拓展
个人觉得本题的思路还是比较巧的，但是适用的解题范围较窄。暂时无拓展想法。
### 思考
本题思路巧妙，若不是从网上找到如此巧妙的答案，我都想不到算法的时间复杂度应为O(n)，并且只能使用常数级别的空间的解决方案。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
