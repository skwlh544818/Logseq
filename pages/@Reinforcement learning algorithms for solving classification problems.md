tags:: [[/unread]], [[Accuracy]], [[Artificial neural networks]], [[Learning]], [[Markov processes]], [[Support vector machines]], [[Testing]], [[Training]], [[已阅读]], [[重要]]
date:: 2011-04
archive-location:: 29 citation(s)
conference-name:: 2011 IEEE Symposium on Adaptive Dynamic Programming and Reinforcement Learning (ADPRL)
proceedings-title:: 2011 IEEE Symposium on Adaptive Dynamic Programming and Reinforcement Learning (ADPRL)
extra:: ISSN: 2325-1867
doi:: 10.1109/ADPRL.2011.5967372
title:: @Reinforcement learning algorithms for solving classification problems
pages:: 91-96
item-type:: [[conferencePaper]]
rights:: ⭐⭐⭐⭐
original-title:: Reinforcement learning algorithms for solving classification problems
authors:: [[Marco A. Wiering]], [[Hado van Hasselt]], [[Auke-Dirk Pietersma]], [[Lambert Schomaker]]
links:: [Local library](zotero://select/library/items/W7FFCEDD), [Web library](https://www.zotero.org/users/8746250/items/W7FFCEDD)

- [[Abstract]]
	- We describe a new framework for applying reinforcement learning (RL) algorithms to solve classification tasks by letting an agent act on the inputs and learn value functions. This paper describes how classification problems can be modeled using classification Markov decision processes and introduces the Max-Min ACLA algorithm, an extension of the novel RL algorithm called actor-critic learning automaton (ACLA). Experiments are performed using 8 datasets from the UCI repository, where our RL method is combined with multi-layer perceptrons that serve as function approximators. The RL method is compared to conventional multi-layer perceptrons and support vector machines and the results show that our method slightly outperforms the multi-layer perceptron and performs equally well as the support vector machine. Finally, many possible extensions are described to our basic method, so that much future research can be done to make the proposed method even better.
- [[Attachments]]
	- [IEEE Xplore Abstract Record](https://ieeexplore.ieee.org/document/5967372) {{zotero-imported-file ENPY9S8A, "5967372.html"}}
	- [Wiering et al_2011_Reinforcement learning algorithms for solving classification problems.pdf](https://ieeexplore.ieee.org/stampPDF/getPDF.jsp?tp=&arnumber=5967372&ref=aHR0cHM6Ly9pZWVleHBsb3JlLmllZWUub3JnL2RvY3VtZW50LzU5NjczNzI=) {{zotero-imported-file S2QFJYEK, "Wiering et al_2011_Reinforcement learning algorithms for solving classification problems.pdf"}}
- #强化学习 #分类
- 本文是一个多智能体的图片分类算法，整体的算法并不算很好，但是它的扩展意义是很有意义的。本文为每个类别标签设计了一个智能体，然后将图片的像素特征排列成行，然后将长度再扩展两份，也就是最后的状态一共是$3*m$，第二个长度，初始全为0，为特征保留桶，第三个长度，初始为原始特征，为删除桶。设计的算法将其作为状态的表达，这个设计是符合马尔科夫过程的。为了减少开销时间，作者最后将状态的价值函数所得到的值，作为
-