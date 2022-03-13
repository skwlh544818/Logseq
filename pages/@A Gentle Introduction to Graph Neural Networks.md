tags:: [[/unread]]
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
- 这种图卷积的一个前提是，不改变图的链接关系，只增强信息。在MLP中，这三种信息可以彼此进行连接，可以理解成池化层之类的
-
- TODO 一个问题，从一个图结构输入到网络中得到加强的图结构有什么用
-