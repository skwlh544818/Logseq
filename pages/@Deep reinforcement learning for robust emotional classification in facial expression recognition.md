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
- 本文主要是使用策略强化学习来清除有噪声的人脸图像情感识别数据集。整体的框架分为两部分，一部分为图像选择模块，也就是策略强化学习网络，一部分为图像情感识别模块，也就是卷积网络。先预训练图像情感识别模块，然后将图片在第一个卷积层和池化层后的特征作为当前图片的一个状态，输入策略强化学习中决策是否保留该图片。对于决策的奖励会放在最后的