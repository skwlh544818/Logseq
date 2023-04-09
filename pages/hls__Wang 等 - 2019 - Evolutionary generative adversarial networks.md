file-path:: file://D:\zotero/storage/J8LIEAD8/Wang 等 - 2019 - Evolutionary generative adversarial networks.pdf

-
- to suffer from training problems such as instability and mode collapse.
  hl-page:: 1
  ls-type:: annotation
  id:: 642c2a56-5519-4cc8-bb17-b9130ec7f117
  hl-color:: yellow
	- GAN网络的问题：不稳定以及模式崩溃
-
- for stable GAN training and improved generative performance.
  hl-page:: 1
  ls-type:: annotation
  id:: 642c2ab3-dfba-48be-b54d-622064be3c5e
  hl-color:: yellow
	- 进化GAN可以解决这个问题
- For example, although measuring Kullback-Leibler divergence largely eliminates the vanishing gradient issue, it easily results in mode collapse [ 24 , 1]. Likewise, Wasserstein distance greatly improves training stability but can have non-convergent limit cycles near equilibrium [21].
  ls-type:: annotation
  hl-page:: 2
  hl-color:: yellow
  id:: 64326a61-c553-45cc-9282-e7e928d5d886
	- 不同的损失函数或者说是两者分布的距离会带来不同的优缺点
- ifferent adversarial objective functions aim to minimize different distances between the generated distribution and the data distribution, leading to different mutations
  ls-type:: annotation
  hl-page:: 2
  hl-color:: yellow
  id:: 64326c55-d184-4ee6-b3d7-825423edd106
	- 这句话的意思应该是使用不同的损失函数计算梯度作为变异的操作。这个是不是可以应用到进化强化学习里面