file:: [Evolutionary Reinforcement Learning.pdf](file://D:\zotero/storage/D9RNX9BS/Evolutionary Reinforcement Learning.pdf)
file-path:: file://D:\zotero/storage/D9RNX9BS/Evolutionary Reinforcement Learning.pdf

- . In RL, EC is particularly useful for complex problems with numerous local optima and is suitable for problems without gradient information.
  ls-type:: annotation
  hl-page:: 6
  hl-color:: yellow
  id:: 6428208d-bdee-4690-b63f-4379b6710caf
	- EC对于具有众多局部最优解的复杂问题特别有用，并且适用于没有梯度信息的问题
- However, HPO for RL faces several challenges.
  ls-type:: annotation
  hl-page:: 6
  hl-color:: yellow
  id:: 64282758-a26d-40b4-b5c1-d420da3a1e5a
	- 1. 性能评估代价比较昂贵；
	  2. 搜索空间比较复杂，混合编码、高维度以及非凸性
	  3. 需要多个目标进行权衡。
- Nonetheless, the Darwinian evolutionary methods are inefficient since parameters are reinitialized in each generation, causing a loss of knowledge already acquired during previous generations.
  ls-type:: annotation
  hl-page:: 7
  hl-color:: yellow
  id:: 64282a2a-95e7-4006-a450-040de48098f6
	- 达尔文进化的缺点，每次都要初始化，会损失前几代中的知识
- In the asynchronous PBT, only one ready individual is compared with a randomly selected individual from the remaining population in each generation, and then the worse individual copies the parameters and hyperparameters of the better individual and adds noise to its hyperparameters.
  ls-type:: annotation
  hl-page:: 7
  hl-color:: yellow
  id:: 64282b2a-c265-4fa6-8c9e-f0e53152c51e
	- 异步PBT算法的迭代步骤，拉马克进化算法
- Moreover, [58] has proposed a collection of benchmarks derived from hyperparameter optimization to verify the performance of quality diversity methods.
  ls-type:: annotation
  hl-page:: 8
  hl-color:: yellow
  id:: 64282d29-6f48-4e6a-8e8a-4d9d554ae3e1
	-