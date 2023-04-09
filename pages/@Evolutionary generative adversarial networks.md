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
- tags:: [[/reading]], [[待读]], [[暂时无用]], [[📒]]
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
- [[Notes]]
	- # 注释 
	   (2023/4/9 下午3:31:53)
	  
	  “If the data distribution and the generated distribution do not substantially overlap (usually at the beginning of training), the generator gradients can point to more or less random directions or even result in the vanishing gradient issue. GANs also suffer from mode collapse,” (Wang 等, 2019, p. 1) GAN网络会出现的问题
	  
	  “GANs also suffer from mode collapse,” (Wang 等, 2019, p. 1)
	  
	  “For example, although measuring Kullback-Leibler divergence largely eliminates the vanishing gradient issue, it easily results in mode collapse [24, 1]. Likewise, Wasserstein distance greatly improves training stability but can have non-convergent limit cycles near equilibrium [21].” (Wang 等, 2019, p. 2) 使用不同的目标函数或者说距离会出现各自的优缺点