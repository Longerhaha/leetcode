# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 137_Single Number II（只出现一次的数字 II）
## 问题描述与输入输出
给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现三次。找出那个只出现了一次的元素。

说明: 你的算法应该具有线性时间复杂度。 你可以不使用额外空间来实现

### 问题示例

	示例1：
	输入：
	[2,2,3,2]
	输出：3


	示例2：
	输入：
	[0,1,0,1,0,1,99]
	输出：
	99


函数输入与输出：
* 输入：
	* int* nums：指向输入数组的指针
	* int numsSize：输入数组的长度

* 输出：
	* int : 只出现了一次的元素

## 思路			
### 位计数法

	i = 0:数据的位宽-1
		掩码设置为1<<i
		在i位上，累加所有数据为1的个数。
		如果该位上的1的个数是3n1,则说明出现一次元素的该位上不是1，于是不需要对结果或上掩码，否则需要或上掩码。
		
### 基于位的卡诺图法
	
	位计数法的核心在于计算是否为3的倍数，那为什么不让当计数为3后则清零呢？基于位的卡诺图和位计满清除法的目地都是当计数满3后则清零。
	one的每位记录此次运算后的1的个数是否是1个，如果是则该位为1，否则该位为0
	two的每位记录此次运算后的1的个数是否是2个，如果是则该位为1，否则该位为0	
	one_pre记录上一次运算one的结果
	two_pre记录上一次运算two的结果
	(1)one每一位的计算与输入数据、one_pre、two_pre结果有关，真值表如下：
		(d代表无关项)
		*p_xbit       0 0 0 0 1 1 1 1
		one_pre_xbit  0 0 1 1 0 0 1 1
		two_pre_xbit  0 1 0 1 0 1 0 1
		one_xbit      0 0 1 d 1 0 0 d
	画出卡诺图后可以得到one的逻辑表达式
		one = (~*p & one_pre) | (*p & ~one_pre & ~two_pre);
	(2)two每一位的计算与输入数据、one_pre、two_pre结果有关，真值表如下：
		(d代表无关项)
		*p_xbit       0 0 0 0 1 1 1 1
		one_pre_xbit  0 0 1 1 0 0 1 1
		two_pre_xbit  0 1 0 1 0 1 0 1
		one_xbit      0 1 0 0 0 0 1 d
	画出卡诺图后可以得到two的逻辑表达式
		two = (*p & one_pre) | (~*p & ~one_pre & two_pre)
		
### [位计满清零法](https://blog.csdn.net/smile_watermelon/article/details/47748227)

	one的每位记录此次运算后的1的个数是否是1个，如果是则该位为1，否则该位为0
	two的每位记录此次运算后的1的个数是否是2个，如果是则该位为1，否则该位为0
	three的每位记录此次运算后的1的个数是否是3个，如果是则该位为1，否则该位为0
	注意每次上述三个值计算完毕后需要对one、two进行更新，因为three的某一位为1后，则需要对one和two的那一位清零（three不需要清零，
	因为这样子操作后，下一次操作在one和two的该位上肯定不会同时为1，所以下一次操作，three的该位经过逻辑运算后就为0了）
	
## 拓展与思考：
### 拓展
 (i)如果除了某个元素只出现一次以外，其余每个元素均出现奇次(5,7,...)，那该怎么做？思路与本题类似。
(ii)如果除了某个元素只出现2次以外，其余每个元素均出现3，那该怎么做？将结果除以2即可了。
### 思考
本题用位计满清零法比较好，因为一旦每个元素出现的个数较大时，逻辑表达式可能会很长，其次卡诺图法可能对于非电子行业的比较陌生。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！