tags:: [[/unread]], [[GNN]] 
date:: [[Sep 2nd, 2021]]
issn:: 2476-0757
archive-location:: 5 citation(s)
issue:: 9
doi:: 10.23915/distill.00033
title:: @A Gentle Introduction to Graph Neural Networks
pages:: e33
volume:: 6
item-type:: [[journalArticle]]
access-date:: 2022-03-11T07:13:56Z
rights:: ⭐⭐⭐⭐
original-title:: A Gentle Introduction to Graph Neural Networks
language:: en
url:: https://distill.pub/2021/gnn-intro
publication-title:: Distill
journal-abbreviation:: Distill
authors:: [[Benjamin Sanchez-Lengeling]], [[Emily Reif]], [[Adam Pearce]], [[Alexander B. Wiltschko]]
library-catalog:: distill.pub
links:: [Local library](zotero://select/library/items/QG539KZ2), [Web library](https://www.zotero.org/users/8746250/items/QG539KZ2)

- [[Abstract]]
	- What components are needed for building learning algorithms that leverage the structure and properties of graphs?
- [[Attachments]]
	- [Snapshot](https://distill.pub/2021/gnn-intro/) {{zotero-imported-file 4A67WFK3, "gnn-intro.html"}}
	- ![A Gentle Introduction to Graph Neural Networks.pdf](../assets/A_Gentle_Introduction_to_Graph_Neural_Networks_1647182508093_0.pdf)
	-
- 本文是对图卷积的介绍，首先说明了图这种数据结构的代码表达形式，有点，边，全局以及邻接矩阵四部分。
- 首先是将常见的数据结构表达成图结构，然后将除了邻接矩阵以外的点、边和全局信息输入MLP中得到最后的图结构进行分析
  id:: 622e084a-3c7b-4ec2-9d38-1a2fb60351f0
- 这种图卷积的一个前提是，不改变图的链接关系，只增强信息。在MLP中，这三种信息可以彼此进行连接，可以理解成池化层之类的
- #GNN #GCN
- DONE 一个问题，从一个图结构输入到网络中得到加强的图结构有什么用 [[Mar 15th, 2022]]
	- 这方面是我误解了，得到稳定的隐藏状态后，会对结点进行分类等操作，比如判断该结点是否为网络水军就是一个二分类问题，会在结点后面加上下游任务的输出，同样是一个MLP网络
- 可以学习的博客
  id:: 622e0ccc-0634-4d42-a8ad-713945377221
	- [[@从图(Graph)到图卷积(Graph Convolution)：漫谈图神经网络模型 (一) - SivilTaram - 博客园]]
	- [[@从图(Graph)到图卷积(Graph Convolution)：漫谈图神经网络模型 (二) - SivilTaram - 博客园]]
	- [[@从图(Graph)到图卷积(Graph Convolution)：漫谈图神经网络模型 (三) - SivilTaram - 博客园]]
-