# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 135_Candy（分发糖果）
## 问题描述与输入输出
老师想给孩子们分发糖果，有 N 个孩子站成了一条直线，老师会根据每个孩子的表现，预先给他们评分。

你需要按照以下要求，帮助老师给这些孩子分发糖果：

* 每个孩子至少分配到 1 个糖果。
* 相邻的孩子中，评分高的孩子必须获得更多的糖果。

那么这样下来，老师至少需要准备多少颗糖果呢？


### 问题示例

	示例1：
	输入：
	[1,0,2]
	输出：
	5
	解释：
	你可以分别给这三个孩子分发 2、1、2 颗糖果。

	示例2：
	输入：
	[1,2,2]
	输出：
	4
	解释：
	你可以分别给这三个孩子分发 1、2、1 颗糖果。第三个孩子只得到 1 颗糖果，这已满足上述两个条件。


函数输入与输出：
* 输入：
	* int* ratings：评分数组的指针
	* int ratingsSize：评分数组的长度
* 输出：
	* int : 老师至少需要准备的糖果数目
	
## 思路			
### 正向、反向扫描法

	1.正向扫描一遍，如果右边的评分比左边高，那么右边的糖果数就比左边多一个，否则只给一个糖果
	2.反向扫描一遍，如果左边的评分比右边高，并且左边的糖果数比右边少，那么左边的糖果数应比右边多一
				 				 	
## 拓展与思考：
### 拓展
如果相邻的孩子中，评分高的孩子获得的糖果不少于相邻的孩子呢？
### 思考
本题思路较为难想，主要自己 没有遇见过之类的问题。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
