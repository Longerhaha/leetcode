# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 075_Set Colors（设置颜色）
## 问题描述与输入输出
给定一个包含红色、白色和蓝色，一共 n 个元素的数组，原地对它们进行排序，使得相同颜色的元素相邻，并按照红色、白色、蓝色顺序排列。

此题中，我们使用整数 0、 1 和 2 分别表示红色、白色和蓝色。

注意:
不能使用代码库中的排序函数来解决这道题。

* 每行中的整数从左到右按升序排列。
* 每行的第一个整数大于前一行的最后一个整数。

### 问题案例

	示例1：
	输入: [2,0,2,1,1,0]
	输出: [0,0,1,1,2,2]
	
进阶：

	* 一个直观的解决方案是使用计数排序的两趟扫描算法。首先，迭代计算出0、1 和 2 元素的个数，然后按照0、1、2的排序，重写当前数组。
	* 你能想出一个仅使用常数空间的一趟扫描算法吗？

函数输入与输出：
* 输入：
	* int* nums:输入的数据数组的头指针
	* int numsSize:输入数据数组的长度
	
* 输出：
	* void：在原地修改，无输出

## 思路			
### 两趟扫描算法（使用常数空间的两趟扫描）

	第一趟：记录0、1、2的个数
	第二趟：根据0、1、2的个数重写当前数组
	
### 一趟扫描算法（仅使用常数空间的一趟扫描）

    使用三个指针，i, j, k分别指向当前最后的0, 1, 2在数组中的位置。
			
## 拓展与思考：
### 拓展
在神经网络中，你训练完模型后，想要做预测。然后你希望把预测的结果（很大的量）分类，其分类结果很可能是杂乱无章的。
而你又想把不同分类结果放在不同的文件夹下，就可以使用这道题目的解决方案。
### 思考
本题限制不能使用代码库中的排序函数，如果你自己去实现qsort，其时间复杂度是O（nlog n），比本题复杂度O（n）高。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
