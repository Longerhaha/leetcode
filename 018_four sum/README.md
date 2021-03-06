# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 018_four sum(四数之和)
## 问题描述与输入输出

### 问题描述

给定一个包含 n 个整数的数组 nums 和一个目标值 target，判断 nums 中是否存在四个元素 a，b，c 和 d ，
使得 a + b + c + d 的值与 target 相等？找出所有满足条件且不重复的四元组。

### 问题案例

	给定数组 nums = [1, 0, -1, 0, -2, 2]，和 target = 0。

	满足要求的四元组集合为：
	[
	  [-1,  0, 0, 1],
	  [-2, -1, 1, 2],
	  [-2,  0, 0, 2]
	]
 
## 思路			
本题思路沿用三数之和中的三下标搜索法（i,j,k），并将其进化为四下标搜索法。增加的一个下标做最外层循环，由于三下标搜索的
时间复杂度为O（n^2）+O（nlogn），所以四下标搜索法的时间复杂度为O（n^3）+O（nlogn）。

## 拓展与思考：
### 拓展
思考一下最接近的四数之和，与最接近的三数之和一样的思路，就是最外层裹了最外层循环。
### 思考
这系列题目真的是很有意思，好好总结了下感觉收获很多。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
