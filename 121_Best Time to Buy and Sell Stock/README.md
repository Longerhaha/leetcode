# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 121_Best Time to Buy and Sell Stock（买卖股票的最佳时机）
## 问题描述与输入输出
给定一个数组，它的第 i 个元素是一支给定股票第 i 天的价格。

如果你最多只允许完成一笔交易（即买入和卖出一支股票），设计一个算法来计算你所能获取的最大利润。

注意你不能在买入股票前卖出股票。

### 问题示例

	示例1：
	输入：
	[7,1,5,3,6,4]
	输出：
	5
	解释：
	在第 2 天（股票价格 = 1）的时候买入，在第 5 天（股票价格 = 6）的时候卖出，最大利润 = 6-1 = 5 。
    注意利润不能是 7-1 = 6, 因为卖出价格需要大于买入价格。

	示例2：
	输入：
	[7,6,4,3,1]
	输出：
	0
	解释：
	在这种情况下, 没有交易完成, 所以最大利润为 0。

函数输入与输出：
* 输入：
	* int* prices: 指向价格数组的一级指针。
	* int pricesSize: 价格数组的个数。

* 输出：
	* int : 最大利润。

## 思路			
### 一次扫描

	1.初始化最小价格下标为0，最大利润为0
	2.从第二个价格开始扫描，如果价格比最小价格下标对应的价格小，则更新最小价格下标；
	如果当前价位与最小价格对于的价格的利润大于最大利润，则更新最大利润。
	
## 拓展与思考：
### 拓展
如果给定的不是三角形形式的数据呢？其次，如果让你求最大路径和呢？
### 思考
利用动态规划很简单的解决了该问题。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！