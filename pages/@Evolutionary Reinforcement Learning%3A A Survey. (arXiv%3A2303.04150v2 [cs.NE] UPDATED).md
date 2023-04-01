links:: [Local library](zotero://select/library/items/MA4RHDQD), [Web library](https://www.zotero.org/users/8746250/items/MA4RHDQD)
publication-title:: arXiv Computer Science
url:: https://arxiv.org/abs/2303.04150?utm_source=researcher_app&utm_medium=referral&utm_campaign=RESR_MRKT_Researcher_inbound
original-title:: Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)
item-type:: [[journalArticle]]
doi:: arXiv:2303.04150v2
tags:: /reading, Researcher App, ⚠️ Invalid DOI, 待读, 重要
title:: @Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)

- [[Abstract]]
	- Reinforcement learning (RL) is a machine learning approach that trains agents
	  to maximize cumulative rewards through interactions with environments. The
	  integration of RL with deep learning has recently resulted in impressive
	  achievements in a wide range of challenging tasks, including board games,
	  arcade games, and robot control. Despite these successes, there remain several
	  crucial challenges, including brittle convergence properties caused by
	  sensitive hyperparameters, difficulties in temporal credit assignment with long
	  time horizons and sparse rewards, a lack of diverse exploration, especially in
	  continuous search space scenarios, difficulties in credit assignment in
	  multi-agent reinforcement learning, and conflicting objectives for rewards.
	  Evolutionary computation (EC), which maintains a population of learning agents,
	  has demonstrated promising performance in addressing these limitations. This
	  article presents a comprehensive survey of state-of-the-art methods for
	  integrating EC into RL, referred to as evolutionary reinforcement learning
	  (EvoRL). We categorize EvoRL methods according to key research fields in RL,
	  including hyperparameter optimization, policy search, exploration, reward
	  shaping, meta-RL, and multi-objective RL. We then discuss future research
	  directions in terms of efficient methods, benchmarks, and scalable platforms.
	  This survey serves as a resource for researchers and practitioners interested
	  in the field of EvoRL, highlighting the important challenges and opportunities
	  for future research. With the help of this survey, researchers and
	  practitioners can develop more efficient methods and tailored benchmarks for
	  EvoRL, further advancing this promising cross-disciplinary research field.
- [[Attachments]]
	- [Evolutionary Reinforcement Learning.pdf](https://arxiv.org/pdf/2303.04150.pdf) {{zotero-imported-file D9RNX9BS, "Evolutionary Reinforcement Learning.pdf"}}
- [[Notes]]
	- # 注释 
	   (2023/3/20 下午9:20:40)
	  
	  “Despite these successes, there remain several crucial challenges, including brittle convergence properties caused by sensitive hyperparameters, difficulties in temporal credit assignment with long time horizons and sparse rewards, a lack of diverse exploration, especially in continuous search space scenarios, difficulties in credit assignment in multi-agent reinforcement learning, and conflicting objectives for rewards.” (“Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)”, p. 1) 强化学习存在的一些问题，比如超参数比较敏感，奖励比较稀疏，缺乏多样性探索问题
	  
	  “We then discuss future research directions in terms of efficient methods, benchmarks, and scalable platforms.” (“Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)”, p. 1) 在高效方法、基准以及可扩展平台上的未来方向
	  
	  “EvoRL involves maintaining a population of agents, which offers several benefits, such as provision of redundant information for improved robustness [9], enabling diverse exploration [10], ability to evaluate agents using an episodic fitness metric [9], and the ease of generating trade-off solutions through multi-objective EC algorithms [11].” (“Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)”, p. 2) EvoRL的好处，可以提供冗余信息以提高鲁棒性，多样性探索
	  
	  “Finally, the article discusses potential improvement approaches for future research, including efficient methods in terms of EvoRL processes, tailored benchmarks, and scalable platforms.” (“Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)”, p. 2) 可能改进的方法
	  
	  “Policy search seeks to identify a policy that maximizes the cumulative reward for a given task.” (“Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)”, p. 3) 这句话比较对，也是因为这个原因才使用进化算法来进行策略搜索的
	  
	  “F is the Fisher information matrix (FIM) of the parametric family of the search distribution,” (“Evolutionary Reinforcement Learning: A Survey. (arXiv:2303.04150v2 [cs.NE] UPDATED)”, p. 5) Fisher信息矩阵是用于评估参数估计的精度和可靠性的一种数学工具。它通常用于最大似然估计中，以评估参数的方差和协方差。以下是计算Fisher信息矩阵的一般步骤：
	  
	  1. 确定模型的参数向量θ。
	  2. 构建似然函数L(θ|x)，其中θ是模型的参数向量，x是观测到的数据。
	  3. 计算对数似然函数l(θ) = log L(θ|x)。
	  4. 计算对数似然函数的二阶导数，即Hessian矩阵：
	     H(θ) = ∂²l(θ)/∂θ²
	  5. 取负数并取期望值，得到Fisher信息矩阵I(θ)：
	     I(θ) = -E[H(θ)]
	  
	  在实际操作中，可以使用数值方法来近似计算Hessian矩阵和Fisher信息矩阵。
- GP的计算：
	- 搜索空间由一组程序组成，这些程序用各种编码方式表示，**如抽象语法树、可执行图（如笛卡尔GP和纠结程序图）、有限状态机和上下文自由语法等等[28]。**