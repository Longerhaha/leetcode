# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 858_螺旋矩阵 III
## 问题描述与输入输出
### 问题描述

在 R 行 C 列的矩阵上，我们从 (r0, c0) 面朝东面开始

这里，网格的西北角位于第一行第一列，网格的东南角位于最后一行最后一列。

现在，我们以顺时针按螺旋状行走，访问此网格中的每个位置。

每当我们移动到网格的边界之外时，我们会继续在网格之外行走（但稍后可能会返回到网格边界）。

最终，我们到过网格的所有 R * C 个空间。

按照访问顺序返回表示网格位置的坐标列表。

### 问题示例

	示例1：
	输入: 
	R = 1, C = 4, r0 = 0, c0 = 0
	输出: 
	[[0,0],[0,1],[0,2],[0,3]]
	
	示例2：
	输入: 
	R = 5, C = 6, r0 = 1, c0 = 4
	输出: 
	[[1,4],[1,5],[2,5],[2,4],[2,3],[1,3],[0,3],[0,4],[0,5],[3,5],[3,4],[3,3],[3,2],[2,2],[1,2],[0,2],[4,5],[4,4],[4,3],[4,2],[4,1],[3,1],[2,1],[1,1],[0,1],[4,0],[3,0],[2,0],[1,0],[0,0]]
	
### 函数输入与输出：
* 输入：
	* int R: 网格的行数
	* int C: 网格的列数
	* int r0：起始点的行坐标
	* int c0：起始点的纵坐标
	* int** columnSizes：*columnSizes 是指向返回长度数组的一级指针，columnSizes是二级指针。
	* int* returnSize：*returnSize是网格的点数目
	
* 输出：
	* 无

## 思路			
### 找规律法

	分成四组，如下：
	        第四组
		  | - -
	第三组|   | 第一组
		  - - | 第一组   	
		第二组
	然后找规律逐个击破。
	
	
	
## 拓展与思考：
### 拓展
暂无想法。
### 思考
本题相比于螺旋矩阵I和螺旋矩阵II更灵活了，需要加入边界有效判断。
		  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
