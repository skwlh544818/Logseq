tags:: [[/unread]], [[⛔ No DOI found]], [[已阅读]], [[重要]]
title:: @Generative Adversarial Nets
pages:: 9
item-type:: [[journalArticle]]
rights:: ⭐⭐⭐⭐⭐
original-title:: Generative Adversarial Nets
language:: en
authors:: [[Ian Goodfellow]], [[Jean Pouget-Abadie]], [[Mehdi Mirza]], [[Bing Xu]], [[David Warde-Farley]], [[Sherjil Ozair]], [[Aaron Courville]], [[Yoshua Bengio]]
links:: [Local library](zotero://select/library/items/4VKWL8QI), [Web library](https://www.zotero.org/users/8746250/items/4VKWL8QI)

- [[Attachments]]
	- [simpread-生成对抗网络——原理解释和数学推导 - 黄钢的部落格 _ Canary Blog.md](zotero://select/library/items/C9UF3JIW) {{zotero-imported-file C9UF3JIW, "simpread-生成对抗网络——原理解释和数学推导 - 黄钢的部落格 _ Canary Blog.md"}}
	- [Goodfellow 等。 - Generative Adversarial Nets.pdf](zotero://select/library/items/EE9CJ7ST) {{zotero-imported-file EE9CJ7ST, "Goodfellow 等。 - Generative Adversarial Nets.pdf"}}
- 本文构建了一个生成模型GAN来学习训练数据的分布，是一个无监督学习算法。在此之前有VAE等生成模型为相关工作，作者重点介绍了与PM可预测性最小化算法的不同。
	- 本文提出的GAN与其他的生成模型的一个主要区别在于，GAN无需使用马尔科夫链以及展开的近似推理来近似极大似然函数
	  id:: 622def79-110d-4a45-a41c-f6756efe9606
- GAN一共训练两个网络，一个是生成网络G，和判别网络D
	- 生成网络G：从足够简单的噪声分布（所熟知的分布比如正态分布等）中采样数据$z$作为输入，使用MLP作为网络，最后输出为与训练数据$x$同源的图片
	- 判别器D：可以看成是一个二分类网络，生成网络生成的数据为0，训练数据为1。同样使用MLP网络，输入为一半生成数据一半训练数据，最后输出是训练数据的概率（0~1）。
	- 生成器G的目的是产生出使判别器D分辨不出的图像，判别器D的目的是尽力分别出生成数据以及训练数据。相当于玩最大最小游戏，两者达到纳什平衡
- 需要优化的价值函数
	- $$\mathop{min}\limits_{G} \mathop{max}\limits_D V(D,G)=E_{x\sim P_{data}(x)}[logD(x)]+E_{z\sim P_z(z)}[log(1-D(G(z)))]$$
- 该价值函数可以优化成KL散度，进而优化成JS散度，表明$P_{data}$和$P_G$之间的差别，具体的推导可以看这个[这个链接]()