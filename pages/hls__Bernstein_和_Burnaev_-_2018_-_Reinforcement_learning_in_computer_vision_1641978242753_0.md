-
- Reinforcement Learning in Computer Vision
  hl-page:: 1
  ls-type:: annotation
  id:: 61de9c89-a801-4df7-9919-17837f857124
	- 这是一篇综述，主要介绍了强化学习技术及在计算机视觉上的应用。
-
-
- hus, various solutions of this CV task should be estimated on basis of results of performed actions (further navigationand path planning).
  ls-type:: annotation
  hl-page:: 1
  id:: 61de9f0d-f188-47e2-9dca-92d3439d721b
	- 将实际的CV任务与强化学习挂钩，用强化学习的决策结果对CV任务进行评估
-
- filtering, extracting image features, localizing objects 
  ls-type:: annotation
  hl-page:: 1
  id:: 61deb247-92da-4490-bbe8-5950f1281af7
	- 定位任务的综述已经看过了，但是提取图像特征和过滤的还没有见过。
	-
- [:span]
  ls-type:: annotation
  hl-page:: 2
  id:: 61deb44f-3c47-439f-b8bd-aaedc46aabea
  hl-type:: area
  hl-stamp:: 1641985101474
	- 马尔可夫决策过程的的组成
	  + 行为
	  + 状态
	  + 奖励
	  + 转移函数
	-
-
- Parameter Selection in Edge Detection Algorithm
  ls-type:: annotation
  hl-page:: 3
  id:: 61debd8a-ecff-4852-96fa-b5ec0ffc3c80
	- 本节是使用强化学习来进行边缘提取算法的参数选择，也就是阈值
	- 该阈值是指边缘提取算法中两个相邻像素之间的强度变化必须多大才能表示这些像素之间存在边缘。
	- 奖励值的确定很有意思，评估Pratt品质因数模块的评估值可以作为奖励。
	- 那么其实强化学习的应用场景很适合那些有确定的评估算法的学科上。
- Image Classification using Visual Features
  ls-type:: annotation
  hl-page:: 4
  id:: 61dec148-be9a-4055-a734-f1b01f47c6c6
	- 这个任务没有很明确的表示，强化学习所做的工作是什么，以及解决的是分类问题还是什么问题。这个需要看以下他的引文，33，36，40
	- 根据一些恒准标准来确定分类的不准确性，来基于奖励指导智能体何时细化分类
- maps  raw  captured  images  directly  to  robot’s  actuating  mechanism
  ls-type:: annotation
  hl-page:: 4
  id:: 61dec2d0-be0e-41f3-adad-780467d25c55
	- 直接使用原始图像作为输入，来控制机器人的行为
- onstructing a fast classifier that predicts salient objects givenlarge-scale visual features 
  ls-type:: annotation
  hl-page:: 4
  id:: 61dec34e-b710-47d8-b362-5239ff090f11
	- 这个很有意思，注意引文的内容，学习一下其构建的思路，引文56
	-
- 这个综述很糟糕