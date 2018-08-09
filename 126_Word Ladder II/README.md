# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 127_Word Ladder（单词接龙）
## 问题描述与输入输出
给定两个单词（beginWord 和 endWord）和一个字典，找到从 beginWord 到 endWord 的最短转换序列的长度。转换需遵循如下规则：

1. 每次转换只能改变一个字母。
2. 转换过程中的中间单词必须是字典中的单词。

_说明_：
* 如果不存在这样的转换序列，返回 0。
* 所有单词具有相同的长度。
* 所有单词只由小写字母组成。
* 字典中不存在重复的单词。
* 你可以假设 beginWord 和 endWord 是非空的，且二者不相同。


### 问题示例

	示例1：
	输入：
	beginWord = "hit",
	endWord = "cog",
	wordList = ["hot","dot","dog","lot","log","cog"]
	输出：
	5
	解释：
	一个最短转换序列是 "hit" -> "hot" -> "dot" -> "dog" -> "cog",
    返回它的长度 5。


	示例2：
	输入：
	beginWord = "hit",
	endWord = "cog",
	wordList = ["hot","dot","dog","lot","log"]
	输出：
	0
	解释：
	endWord "cog" 不在字典中，所以无法进行转换。
		


函数输入与输出：
* 输入：
	* char* beginWord: 开始词的字符串指针
	* char* endWord: 结束词的字符串指针
	* char** wordList: 单词列表的二级指针，其指向的每个元素都指向一个字符串
	* int wordListSize：单词列表的长度

* 输出：
	* int : 从 beginWord 到 endWord 的最短转换序列的长度。

## 思路			
### 基于邻接矩阵的Dijkstra算法（权重全部为1)
	
	1.基于规则构造图的邻接矩阵
	2.根据Dijkstra算法算出beginWord 到 每个wordList的最短路径
	3.如果存在endWord，找出endWord 在 wordList的位置，并返回对于位置的最短距离与路径
	该方法被测试样例卡住了，因为wordList很大的时候，内存会超出限制	
	
### 基于邻接表的Dijkstra算法（权重全部为1）

	1.基于规则构造图的邻接表
	2.根据Dijkstra算法算出beginWord 到 每个wordList的最短路径
	3.如果存在endWord，找出endWord 在 wordList的位置，并返回对于位置的最短距离与路径
	该方法被测试样例卡住了，因为wordList很大的时候，因为超时而无法通过
	
### 基于队列的BFS
	
	1. 初始化队列
	2. beginWord进队
	3. while( 队列不空 )
		    节点V出队;
			如果节点V的str与endWord一样则返回深度;
			对V所有的邻接点W,其深度加1后进队
	4. 出循环代码没有endWord于是返回0
	
	
## 拓展与思考：
### 拓展
如果要你把所有能达到beginWord的路径保存下来该怎么做？
### 思考
本题很有意思，最重要的是问题的建模，题目看似无图却胜似右图，利用图建模后用图的基本方法就可以解决该问题了。
	  
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
