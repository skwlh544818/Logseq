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
- 文章与