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
	- 超参数优化也和质量多样性有关
- However, the current literature on HPO still faces several challenges, such as the lack of comprehensive performance metrics and the need for efficient convergence speed. Additionally, selecting hyperparameters from a large number of options is a combinatorial optimization problem that brings new challenges to EC methods.
  ls-type:: annotation
  hl-page:: 8
  hl-color:: yellow
  id:: 64282dc5-31de-4672-a912-433c0beed327
	- 超参数优化面临的问题，比如缺乏全面的性能指标以及高效的收敛速度，以及面临的时一个组合优化问题。
- focus on developing comprehensive evaluation metrics that consider both effectiveness and efficiency.
  hl-page:: 8
  ls-type:: annotation
  id:: 64282e1a-af68-4b5c-9a11-1c5238c6732f
  hl-color:: red
	- 可以研究的点：
	- 1. 开发综合考虑有效性和效率的评估指标；
	  2. 探索可以有效搜索高位和组合搜索空间的EC方法
	  3. 结合不同的HPO方法来提高优化过程的整体效率以及有效性
- sampling from diverse search directions and making full use of previous samples.
  ls-type:: annotation
  hl-page:: 9
  hl-color:: yellow
  id:: 6428343a-7c12-4366-81d8-1cf9bde7fae9
	- 对于ES算法应用到RL任务中，提高样本效率：
	- 1. 多样性搜索方向采样
	  2. 充分利用以前的样本
- such as the state-space crossover [122], the Q-filtered distillation crossover [123],
  ls-type:: annotation
  hl-page:: 14
  hl-color:: yellow
  id:: 6428e2ad-f42f-45be-86a5-305a3078a865
	- 这是对于神经网络进行交叉的两种方法比较常用的时Q过滤蒸馏交叉
-
- Empirical studies demonstrated that NS can bring unique advantages over fitness-based EC methods in overriding the deceptiveness of most fitness functions and making the evolutionary process more open-ended.
  ls-type:: annotation
  hl-page:: 18
  hl-color:: yellow
  id:: 64295a82-8d0c-4490-b708-560bfad077fe
	- NS在欺骗性奖励以及开放性搜索过程中具有优势。
- The first version, NS-ES, replaces the gradients of expected rewards with the gradients of expected novelty, and the other two versions, NSR-ES and NSRA-ES, trade off the gradients of expected rewards and novelty [6].
  hl-page:: 19
  ls-type:: annotation
  id:: 64295b8c-33fc-40bb-8743-0291b7b76eb9
  hl-color:: yellow
	- 想要改进的目的就是在这里，这里应该也可以将GAN网络的梯度与新颖性搜索的梯度一块进行衡量。
- Additionally, it may be beneficial to explore hybrid methods that combine EC and gradient-based methods to leverage the strengths of both methods.
  ls-type:: annotation
  hl-page:: 23
  hl-color:: yellow
  id:: 64297a89-7fd7-496f-a3c5-1ee838e5cb7d
	- 结合进化算法以及基于梯度的方法可以是有改进好处的
- Despite these indirect encodings, the development of efficient encoding schemes is still limited. 
  hl-page:: 32
  ls-type:: annotation
  id:: 642a629b-3aa9-4362-a008-aa97b94b6afb
  hl-color:: yellow
	- 改进效果一：可以考虑开发人类可以理解的编码和应用于ES的高效编码，可以从信息理论以及统计学习理论的见解中受益。
- Efficient sampling from the decision space is advantageous for ESs, but it has not been thoroughly investigated in GAs or GP based methods.
  hl-page:: 32
  ls-type:: annotation
  id:: 642a641c-b5e3-4c36-829d-aee9eac66d30
  hl-color:: red
	- 改进效果二：对于GA以及GP算法，可以改进一下在决策空间的采样方式。
- Hence, more efficient techniques need to be introduced into ESs. Furthermore, it remains to be investigated whether these techniques are feasible in GAs.
  hl-page:: 33
  ls-type:: annotation
  id:: 642a68f8-a314-4eb8-a1ad-9fe118f39480
  hl-color:: yellow
	- 改进效果三：需要在ES算法中开发与GA算法中的采样技巧。
- Besides topology distillation and gradient sensitive variation through imitation learning and distillation, more methods or techniques can be employed to improve the efficiency of variational operators, such as transfer learning and surrogate gradient methods.
  ls-type:: annotation
  hl-page:: 33
  hl-color:: red
  id:: 642a6ba2-ac4d-4fa0-8ab8-d9b1e31d4e96
	- 改进效果四：使用迁移学习以及代替梯度的方法进行变异。
- while discarding less promising ones. Finally, more search operators can be borrowed from EC (e.g., DE[237], PSO [238], and CSO [239]) to investigate their effectiveness for RL tasks.
  ls-type:: annotation
  hl-page:: 33
  hl-color:: red
  id:: 642a6ce1-036a-49f2-9cb3-1af7e0c104be
	- 改进效果五：使用EC算法中的搜索算子来验证对RL任务的有效性
- If the policy can be divided into components at a finer granularity, various functional modules can be automatically discovered using cooperative cooperation methods.
  hl-page:: 33
  ls-type:: annotation
  id:: 642a6d69-c96a-4886-9427-de1656a8d3cd
  hl-color:: red
	- 改进效果六：将策略网络划分成更细的部分，分而治之，实现不同组件的并行计算，确实一个比较好的内容，比如胶囊网络。