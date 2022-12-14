tags:: [[分类]], [[对抗样本]], [[已阅读]], [[强化学习]], [[重要]]
date:: [[Dec 8th, 2020]]
extra:: arXiv: 2012.04353
title:: @Reinforcement Based Learning on Classification Task Could Yield Better Generalization and Adversarial Accuracy
item-type:: [[journalArticle]]
access-date:: 2022-04-03T11:59:47Z
rights:: ⭐⭐⭐⭐⭐
original-title:: Reinforcement Based Learning on Classification Task Could Yield Better Generalization and Adversarial Accuracy
language:: en
url:: http://arxiv.org/abs/2012.04353
publication-title:: arXiv:2012.04353 [cs]
authors:: [[Shashi Kant Gupta]]
links:: [Local library](zotero://select/library/items/FL8GB2DR), [Web library](https://www.zotero.org/users/8746250/items/FL8GB2DR)

- [[Abstract]]
	- Deep Learning has become interestingly popular in computer vision, mostly attaining near or above human-level performance in various vision tasks. But recent work has also demonstrated that these deep neural networks are very vulnerable to adversarial examples (adversarial examples - inputs to a model which are naturally similar to original data but fools the model in classifying it into a wrong class). Humans are very robust against such perturbations; one possible reason could be that humans do not learn to classify based on an error between "target label" and "predicted label" but possibly due to reinforcements that they receive on their predictions. In this work, we proposed a novel method to train deep learning models on an image classiﬁcation task. We used a reward-based optimization function, similar to the vanilla policy gradient method used in reinforcement learning, to train our model instead of conventional cross-entropy loss. An empirical evaluation on the cifar10 dataset showed that our method learns a more robust classiﬁer than the same model architecture trained using cross-entropy loss function (on adversarial training). At the same time, our method shows a better generalization with the difference in test accuracy and train accuracy < 2% for most of the time compared to the cross-entropy one, whose difference most of the time remains > 2%.
- [[Attachments]]
	- [Gupta - 2020 - Reinforcement Based Learning on Classification Tas.pdf](zotero://select/library/items/VFD6M74L) {{zotero-imported-file VFD6M74L, "Gupta - 2020 - Reinforcement Based Learning on Classification Tas.pdf"}}
- #强化学习 #分类 #对抗样本
- 这篇文章主要是利用强化学习的理念来训练卷积网络，但是由于其实最后分类精度并没有原模型精度好，所以作者为了使模型精度高于卷积网络，挑选了对抗数据这一个方面来写。最后的结果确实高于原模型，所以这种方式也是值得借鉴的。
  id:: 6251880d-b4df-48a8-b89d-778a5af1304d
- 对抗数据指的是在原图片上加上一种干扰之后，该图片虽然在肉眼上看和原图片相同，但是卷积网络却会分类错误的一种现象。
- 该文章与强化学习结合的一个内容就是修改损失函数，引入了强化学习中的奖励机制，将交叉熵函数修改成了$$\sum_t^B{-\frac{1}{B}log(P(a_t|s_t))*R_t}$$
- 本文中的强化学习的三元组设置则是
	- 1. 状态：输入的图片
	  2. 行为：预测的标签
	  3. 奖励：如果预测标签与真实标签相同，则奖励 +1，如果与真实标签不同，则奖励-1
- 无论是从卷积网络的设置，还是强化学习三元组的设计来看，都是一个很简单的设计。本文最大的创新点应该就是引入强化学习到对抗数据分类中，并修改了一个损失函数。
	- 本文也提到一个内容就是这个架构是否可以应用到不平衡分类网络上，来提高分类精度。
	- LATER  将架构应用到不平衡分类，是否可以提升分类精度 #TODO
	  :LOGBOOK:
	  CLOCK: [2022-04-10 Sun 17:33:40]--[2022-04-10 Sun 17:33:41] =>  00:00:01
	  :END: