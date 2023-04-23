tags:: [[待读]], [[暂时无用]]
date:: 2019
archive-location:: 工程技术1区 Top
series-text:: 无
issue:: 6
series-title:: 无
doi:: 10.1109/TEVC.2019.2895748
title:: @Evolutionary generative adversarial networks
pages:: 921–934
volume:: 23
item-type:: [[journalArticle]]
call-number:: 16.497
rights:: 16.815
original-title:: Evolutionary generative adversarial networks
publication-title:: IEEE Transactions on Evolutionary Computation
archive:: Q1
journal-abbreviation:: Ieee T Evolut Comput
authors:: [[Chaoyue Wang]], [[Chang Xu]], [[Xin Yao]], [[Dacheng Tao]]
library-catalog:: 计算机：人工智能1区  计算机：理论方法1区
links:: [Local library](zotero://select/library/items/WT9XWB6B), [Web library](https://www.zotero.org/users/8746250/items/WT9XWB6B)

- [[Abstract]]
	- Generative adversarial networks (GANs) have been effective for learning generative models for real-world data. However, accompanied with the generative tasks becoming more and more challenging, existing GANs (GAN and its variants) tend to suffer from different training problems such as instability and mode collapse. In this paper, we propose a novel GAN framework called evolutionary GANs (E-GANs) for stable GAN training and improved generative performance. Unlike existing GANs, which employ a predefined adversarial objective function alternately training a generator and a discriminator, we evolve a population of generators to play the adversarial game with the discriminator. Different adversarial training objectives are employed as mutation operations and each individual (i.e., generator candidature) are updated based on these mutations. Then, we devise an evaluation mechanism to measure the quality and diversity of generated samples, such that only well-performing generator(s) are preserved and used for further training. In this way, E-GAN overcomes the limitations of an individual adversarial training objective and always preserves the well-performing offspring, contributing to progress in, and the success of GANs. Experiments on several datasets demonstrate that E-GAN achieves convincing generative performance and reduces the training problems inherent in existing GANs.
- [[Attachments]]
	- [Snapshot](https://ieeexplore.ieee.org/abstract/document/8627945/) {{zotero-imported-file 99JEF7ZP, "8627945.html"}}
	- [Full Text](https://arxiv.org/pdf/1803.00657) {{zotero-imported-file J8LIEAD8, "Wang 等 - 2019 - Evolutionary generative adversarial networks.pdf"}}
- 这个文章主要是将判别器和生成器分开作为环境和种群，在一次迭代中，判别器是固定不变的，对应的遗传算法的操作有三个：
- 1. 变异：主要是使用不同的的损失函数的梯度信息来进行变异操作，这里使用了三种变异操作
  2. 评估：使用的是多样性以及判别器得分的平均值之和作为评估分数，多样性是指负对数梯度信息
  3. 选择：对评估分数进行排序选择多个生成器作为父类
- 其余的操作并没有改进什么，重点应该在于这个变异的方式，这个可以很好的应用到进化强化学习的交叉和变异上