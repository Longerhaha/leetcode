# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 042_trapping rain water(接雨水)
## 问题描述与输入输出
	
### 问题描述
给定 n 个非负整数表示每个宽度为 1 的柱子的高度图，计算按此排列的柱子，下雨之后能接多少雨水。

### 问题案例
	比如：
	输入: [0,1,0,2,1,0,1,3,2,1,2,1]
	输出: 6 
### 输入与输出

* 输入：
	* int* height:输入的数组头指针
	* int heightSize:输入的数组大小
* 输出:能接的雨水的数目

## 思路			
假设这个数比下一个数大，那么他们之间所能容纳的雨水就是他们高度之差吗？答案是否定的，比如输入[2 1]，明显能接的雨水为0。
幸运的是我们只要加个前提（整个数组的最大值在这两个数的后面），那么该问题就是正确的。这就好比后面有一个墙壁，你比后面的人高，
你们就能贡献高度之差的雨水。所以首先花O(n)的时间复杂度去寻找最大值，然后兵分两路，墙左边的节点往墙方向算雨水，墙左边的节点往墙方向算雨水，然后加起来就可以了。

## 拓展与思考：
### 拓展
个人没有想到能在计算机某些数据结构或者算法能应用到的地方，网上搜了下也没相关应用资料。若有相关应用，还请不吝啬赐教。
### 思考
我的思路的时间复杂度是O(n)，空间复杂度O(1)。此外我还看了[wangyuquanliuli的专栏RSS订阅](https://blog.csdn.net/wangyuquanliuli/article/details/45742981)的思路。文中第三种思路和我一直，提到的第四种方法类似第三种思路，左右夹逼，每次选择小的那个指针向中间靠拢，此方法为O(n) 时间, O(1) 空间，但是要比方法三少遍历一遍。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
