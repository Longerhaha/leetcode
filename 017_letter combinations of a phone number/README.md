# leetcode
# stick to it everyday and your will be a good algorithm engineer!
## 017_letter combinations of a phone number(电话号码的字母组合)
## 问题描述与输入输出

### 问题描述

给定一个仅包含数字 2-9 的字符串，返回所有它能表示的字母组合。

给出数字到字母的映射如下（与电话按键相同）。注意 1 不对应任何字母。

	2 "abc"
	3 "def"
	4 "ghi"
	5 "jkl"
	6 "mno"
	7 "pqrs"
	8 "tuv"
	9 "wxyz"

### 问题案例

	输入："23"
	输出：["ad", "ae", "af", "bd", "be", "bf", "cd", "ce", "cf"].
	尽管上面的答案是按字典序排列的，但是你可以任意选择答案输出的顺序。
 
## 思路			
### 循环
深度优先遍历（代码简洁）或者循环（代码较多）都可以做。这里采用循环，相对较快，因为len_result可能很大，深度优先遍历递归的代价太大
	
	len_result记录输出的长度
	record[i]记录第i+1个数字对应的字母个数可能性（3或者4）
	num_circle是分成的大部分数
	times_circle是第i次的大部分数里面的次部分数。
	从头到尾遍历数字
    比如输入"23"：
    输出长度为9
    (1)首先遍历2，record[0]=3,也就是9行的第一个字符分成3部分，num_circle=3，times_circle=3,num_circle的每个部分的字符一样
    num_circle=1        times_circle = 0   ['a',未知]
						times_circle = 1   ['a',未知]
						times_circle = 2   ['a',未知]
	num_circle=2		times_circle = 0   ['b',未知]
						times_circle = 1   ['b',未知]
						times_circle = 2   ['b',未知]
    num_circle=3        times_circle = 0   ['c',未知]
						times_circle = 1   ['c',未知]
						times_circle = 2   ['c',未知]
    (2)其次遍历3，record[1]=3,num_circle=1, times_circle=9,也就是9行的第二个字符分成9部分，每隔3部分的字符一样，于是采用了j%record[i]
    num_circle=1        times_circle = 1   ['a', 'd']
						times_circle = 2   ['a', 'e']
						times_circle = 3   ['a', 'f']
						times_circle = 4   ['b', 'd']
						times_circle = 5   ['b', 'e']
						times_circle = 6   ['b', 'f']
						times_circle = 7   ['c', 'd']
						times_circle = 8   ['c', 'e']
						times_circle = 9   ['c', 'f'] 
    

## 拓展与思考：
### 拓展
[递归与循环](https://www.zhihu.com/question/20418254)。
### 思考
代码也可以修改为递归实现，但是在len_result较大的情况下，递归的代价很大。感兴趣的可以去试一下。
        
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
