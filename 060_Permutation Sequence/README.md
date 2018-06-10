# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 060_Permutation Sequence（第k个排列）
## 问题描述与输入输出
给出集合 [1,2,3,…,n]，其所有元素共有 n! 种排列。

按大小顺序列出所有排列情况，并一一标记，当 n = 3 时, 所有排列如下：

	"123"
	"132"
	"213"
	"231"
	"312"
	"321"
	
给定 n 和 k，返回第 k 个排列。

说明：

	给定 n 的范围是 [1, 9]。
	给定 k 的范围是[1,  n!]。

函数输入与输出：
* 输入：
	* int n：集合[1,2,3,…,n]
	* int k：第k个排列

	
* 输出：char* 第k个排列的字符串的首地址

## 思路			
### 基于位置字符判断的方法(JUDGE_CHARACTER) 

	//输入的k从低到到判断每个位置上的符号
	输入k，先求n-1的阶乘rank, 参与计算的是res = k-1，res_idx代表res除以阶乘后的整数部分
	for j = 0...n-2
		res_idx = res/rank;
		kth_permutation[j] = (char)(find(nums, n, res_idx+1)+'0');//find是查找当前未用到的第res_idx+1个字符
		res -= res_idx*rank;
		rank = rank/(n-1-j);//降阶
	kth_permutation[j] = (char)(find(nums, n, 1)+'0');//最后一个字符就是所有字符中未用到的那个字符	

### 基于下一个排列的方法
	先构造一个排列"123...n"，然后进行k-1次下一个排列即是第k个排列					
					 				 	
## 拓展与思考：
### 拓展
如果改成输入字符串指定且有可能有重复数据呢？上述两种方法依然是可行的。但是[基于交换的递归方法](https://github.com/Longerhaha/leetcode/tree/master/046_permutations)
是不可行的，你知道为什么吗？
### 思考
基于位置字符判断的方法时间复杂度为O（n*n）,基于下一个排列的方法时间复杂度为O（k*n），k=1~n!，明显前者在k较大的时候更快。
我在leetcode OJ平台上，前者是4ms，后者160ms。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
