# 准备工作

\1.   查看数据

\2.   Excel 排序看了一下 有重复的，可以去重。有类似的，但不知道归类标准

# 方法

## 方法一

可以按照首字母排序去重，excel就可以实现，结果句式比较相似

| A brief autopsy  revealed no reason why the dead had been so badly dissected. |
| ------------------------------------------------------------ |
| A businessman with no business background  could not have been a good CEO. |
| A few days before the induction                              |
| A few years ago                                              |
| A fighter is someone who is not afraid to  take on the challenge. |
| A fighter is someone who is not afraid to  take on the world. |
| A file that can be used to commit such  crimes should be created. |
| A File that would give such a person a  perfect record of all the people he killed. |

## 方法二

可以选几个种子句子，比较余弦相似度，定义一个阈值，相似的放在一起。

## 方法三

\1.   首先定义为一个短文本分类问题

\2.   观察数据发现数据中没有label，也没有看出明显的特征。因此不考虑人工标注，考虑无监督的学习方式

 

\3.   考虑使用lda模型做主题模型 粗略的获取一些主题信息。

 

\4.   主题数量如何确定 聚类出主题 ，列用主题进行分类

\5.   Gensim doc2bow做特征转换成向量

 



|      |                                                              |
| ---- | ------------------------------------------------------------ |
|      | ![img](file:///C:/Users/15728/AppData/Local/Temp/msohtmlclip1/01/clip_image001.png) |

 程序在textTopic.ipynb当中，input为重复句子.txt,output为分类文件。 运行textTopic.ipynb会追加内容进文件，所以，测试得运行结果保存在了output文件夹中。

 