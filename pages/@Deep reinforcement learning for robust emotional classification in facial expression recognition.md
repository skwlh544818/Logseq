tags:: [[分类]], [[噪声数据]], [[已阅读]], [[强化学习]], [[重要]]
date:: 09/2020
issn:: 09507051
extra:: ZSCC: 0000011
doi:: 10/gnq9rr
title:: @Deep reinforcement learning for robust emotional classification in facial expression recognition
pages:: 106172
volume:: 204
item-type:: [[journalArticle]]
access-date:: 2021-12-11T05:37:39Z
call-number:: 8.038
rights:: ⭐⭐⭐⭐
original-title:: Deep reinforcement learning for robust emotional classification in facial expression recognition
language:: en
url:: https://linkinghub.elsevier.com/retrieve/pii/S0950705120304081
publication-title:: Knowledge-Based Systems
journal-abbreviation:: Knowledge-Based Systems
authors:: [[Huadong Li]], [[Hua Xu]]
library-catalog:: 1
links:: [Local library](zotero://select/library/items/2MISUPF4), [Web library](https://www.zotero.org/users/8746250/items/2MISUPF4)

- [[Abstract]]
	- For emotion classification in facial expression recognition (FER), the performance of both traditional statistical methods and state-of-the-art deep learning methods are highly dependent on the quality of data. Traditional methods use image preprocessing (such as smoothing and segmentation) to improve image quality. However, the results still fail to meet the quality requirements of the emotion classifiers in FER. To address the above issues, this paper proposed a novel framework based on reinforcement learning for pre-selecting useful images(RLPS) for emotion classification in FER, which is made up of two modules: image selector and rough emotion classifier. Image selector is used to select useful images for emotion classification through reinforcement strategy and rough emotion classifier acts as a teacher to train image selector. Our framework improves classification performance by improving the quality of the dataset and can be applied to any classifier. Experiment results on RAF-DB, ExpW, and FER2013 datasets show that the proposed strategy achieves consistent improvements compared with the state-of-the-art emotion classification methods in FER.1 © 2020 Elsevier B.V. All rights reserved.
- [[Attachments]]
	- [Li 和 Xu - 2020 - Deep reinforcement learning for robust emotional c.pdf](zotero://select/library/items/T7YLI793) {{zotero-imported-file T7YLI793, "Li 和 Xu - 2020 - Deep reinforcement learning for robust emotional c.pdf"}}
- #分类 #强化学习 #噪声数据
- 本文主要是使用策略强化学习来清除有噪声的人脸图像情感识别数据集来提高分类精度的。整体的框架分为两部分，一部分为图像选择模块，也就是策略强化学习网络，一部分为图像情感识别模块，也就是卷积网络。先预训练图像情感识别模块，然后将图片在第一个卷积层和池化层后的特征作为当前图片的一个状态，输入策略强化学习中决策是否保留该图片。对于决策的奖励会放在最后，集体进行奖励评价。
- 这里提到的一个问题就是，图片的数据集是独立同分布的，并不符合强化学习的马尔可夫过程。这里解决的一个方法是将选择的图片集也输入到分类器中得到相同维度的特征，然后将当前图片特征与选择过的图片集的特征进行拼接，这样就符合马尔可夫过程了。其实对于其他强化学习的文章来说都没有关注这一点，只是强硬的使用强化学习罢了。
- 强化学习三元组：
	- 状态：已选择图片集的相同维度特征与当前图片特征拼接得到的特征就是当前图片的状态，这个状态与前一个状态也有联系。
	- 行为：只有两个行为，一个是保留，一个是删除
	- 奖励：奖励值是在数据集所有图片都被选择过后全部统一给予的。
	- $$R_i=P\{e_{true}|x_i\}-\frac{1}{n}\sum_{j=1}^{n}p\{e|x_j\}$$
	- $i$指的是被选择保留的图片
- 这个文章给的一个启发就是，前几篇文章都没有考虑马尔可夫决策过程的条件，其实不算真正意义上的强化学习。当然这篇文章也有个问题就是文章写的很糟糕。也提供一个思路就是强化学习可以用来处理噪声数据。