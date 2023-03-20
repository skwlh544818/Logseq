tags:: [[/reading]], [[待读]], [[重要]]
date:: 2022
archive-location:: 5 📊
extra:: "Publisher: ACM New York, NY"
doi:: 10.1145/3569096
title:: @Combining Evolution and Deep Reinforcement Learning for Policy Search: a Survey
item-type:: [[journalArticle]]
original-title:: Combining Evolution and Deep Reinforcement Learning for Policy Search: a Survey
short-title:: Combining Evolution and Deep Reinforcement Learning for Policy Search
publication-title:: ACM Transactions on Evolutionary Learning
authors:: [[Olivier Sigaud]]
library-catalog:: Google Scholar
links:: [Local library](zotero://select/library/items/K85IPVTQ), [Web library](https://www.zotero.org/users/8746250/items/K85IPVTQ)

- [[Attachments]]
	- [Full Text](https://dl.acm.org/doi/pdf/10.1145/3569096) {{zotero-imported-file X5VJGPV6, "Sigaud - 2022 - Combining Evolution and Deep Reinforcement Learnin.pdf"}}
- [[Notes]]
	- # 注释 
	   (2023/3/18 下午4:05:36)
	  
	  “A broader perspective and survey on all the evolutionary and rl combinations anterior to the advent of the so called ždeep learning" methods using large neural networks can be found in [19].” (Sigaud, 2022, p. 1) 之前的强化学习与进化算法的结合方法的综述，需要考量一下。
	  
	  “even emerging libraries dedicated to their implementation” (Sigaud, 2022, p. 1) 进化算法和强化学习结合的库
	  
	  三篇比较进化算法和强化学习的综述
	  
	  “Deep Reinforcement Learning Versus Evolution Strategies: A Comparative Survey.” (Sigaud, 2022, p. 18)
	  
	  “Derivative-free reinforcement learning: A review.” (Sigaud, 2022, p. 19)
	  
	  “Policy Search in Continuous Action Domains: an Overview” (Sigaud, 2022, p. 20)
	  
	  “the neural network architecture as a simple vector of parameters. This approach is known to require tedious hyperparameter tuning and generally perform worse than evolution strategies which are also mathematically more founded [9, 79]. In particular, the genetic operators used in erl and cerl based on a direct encoding have been shown to induce a risk of catastrophic forgetting of the behavior of eicient individuals.” (Sigaud, 2022, p. 4) ERL和CERL的缺点，基于进化算法，参数硬编码，需要超参数巨大，并且表现比进化策略差，存在遗忘优秀个体的风险
	  
	  “the genetic operators of erl are replaced by operators using local replay bufers” (Sigaud, 2022, p. 4)
	  
	  “Note that if an rl actor is injected in an evolutionary population and if evolution uses a direct encoding, the rl actor and evolution individuals need to share a common structure. Removing this constraint might be useful, as evolutionary methods are often applied to smaller policies than rl methods. For doing so, one might call upon any policy distillation mechanism that strives to obtain from a large policy a smaller policy with similar capabilities.” (Sigaud, 2022, p. 5) 查找相关的论文，学习策略提炼机制，将强化学习机制转化成类似能力的小的策略
	  
	  “A weakness of all the methods combining evolution and rl that we have listed so far is that they require evaluating the agents to perform the evolutionary selection step, which may impair sample eiciency” (Sigaud, 2022, p. 6) 结合进化算法和强化学习的一个问题是，评估智能体来执行选择步骤，可能损害样本效率
	  
	  这个综述不是一个好的综述，仅仅是将各个算法进行了一个分类，并没有认真介绍每个算法的内容。
	  
	  Referred in [注释 (2022/10/11 下午6:20:07)](zotero://note/u/JPH6GU2C/?ignore=1)
- 综述将进化强化学习分为了几个不同的内容主题：
	- 1. 为了提高性能使用进化策略，这一部分是最主要的内容，比如ERL、PDERL等内容