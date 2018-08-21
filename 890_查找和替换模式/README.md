# leetcode
# stick to it everyday and you will be a good algorithm engineer!
## 890_查找和替换模式
## 问题描述与输入输出
### 问题描述

你有一个单词列表 words 和一个模式  pattern，你想知道 words 中的哪些单词与模式匹配。

如果存在字母的排列 p ，使得将模式中的每个字母 x 替换为 p(x) 之后，我们就得到了所需的单词，那么单词与模式是匹配的。

（回想一下，字母的排列是从字母到字母的双射：每个字母映射到另一个字母，没有两个字母映射到同一个字母。）

返回 words 中与给定模式匹配的单词列表。

你可以按任何顺序返回答案。

### 问题示例

	示例1：
	输入: 
	words = ["abc","deq","mee","aqq","dkd","ccc"], pattern = "abb"
	输出: 
	["mee","aqq"]
	解释：
	"mee" 与模式匹配，因为存在排列 {a -> m, b -> e, ...}。
	"ccc" 与模式不匹配，因为 {a -> c, b -> c, ...} 不是排列。
	因为 a 和 b 映射到同一个字母。
	
	
### 函数输入与输出：
* 输入：
	* char** words: 单词列表的二级指针
	* int wordsSize: 单词列表的长度
	* char* pattern: 模式单词的一级指针
	* int* returnSize：返回单词的长度
	
* 输出：
	* char**：返回单词数组的二级指针

## 思路			
### 双映射表

	for(输入的每个单词words[i] : word)
		dict1记录pattern到word的映射关系，dict2记录word到pattern的映射关系
		初始化为匹配
		for(pattern的每个字符pattern[i],word的每个字符word[i])
			if(dict1没有pattern[i]的映射且dict2没有word[i]的映射)
				记录映射关系
			else if(dict1的映射关系不是pattern[i]->word[i]或者dict2的映射关系不是word[i]->pattern[i])
				不匹配
		if(匹配)
			记录数据至输出列表
		

## 拓展与思考：
### 拓展
正则表达式。
### 思考
本题思路也较为简单，但是为了避免多映射一，需要使用两个映射关系，当然你也可以利用record记录字符是否出现过解决多映射一的问题。
# 希望我能在这一年坚持下来，每天都不放弃，每天都至少刷一道题，我相信我可以的！
