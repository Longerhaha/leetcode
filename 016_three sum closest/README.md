# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 016_three sum closest(最接近的三数之和)
## 问题描述与输入输出

### 问题描述

给定一个包括 n 个整数的数组 nums 和 一个目标值 target。找出 nums 中的三个整数，
使得它们的和与 target 最接近。返回这三个数的和。假定每组输入只存在唯一答案。

### 问题案例

	例如，给定数组 nums = [-1，2，1，-4], 和 target = 1.

	与 target 最接近的三个数的和为 2. (-1 + 2 + 1 = 2).
 
## 思路			
本题思路沿用三数之和中的三下标搜索法（i,j,k），算出当前和是最接近则更新最近和，并且根据当前的和与target的和的大小更新
内层迭代的下标j与k。时间复杂度为O（n^2）+O（nlogn）。

## 拓展与思考：
### 拓展
如果题目要求的是下标而且还是非重复多解，那么就稍微加点难度了，可参考前面的[两数之和](https://github.com/Longerhaha/leetcode/tree/master/001_two%20sum)与
[三数之和](https://github.com/Longerhaha/leetcode/tree/master/015_three%20sum)。
### 思考
三下标搜索法在本题非常好用，哈希表在本题则失效，个人感觉三下标搜索法使用范围更广一点。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
