# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 001_two sum(两数之和)
## 问题描述与输入输出

给定一个整数数组和一个目标值，找出数组中和为目标值的两个数。你可以假设每个输入只对应一种答案，且同样的元素不能被重复利用。

比如：
* 输入：给定 nums = [2, 7, 11, 15], target = 9
* 输出：因为 nums[0] + nums[1] = 2 + 7 = 9，所以返回 [0, 1]
 
## 思路			
由于题目每个输入只对应一种答案，所以这道题较为简单，直接做两层循环查找即可。*（代码里面找到后没有跳出循环，有心人可以进一步优化）*

## 拓展与思考：
* 拓展：最常规的也是最好用的。
* 思考：这种题目较为常规，最为基础。申请内存空间的时候最好memset一下，以及未用的内存空间最好释放掉，避免变成野指针。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！