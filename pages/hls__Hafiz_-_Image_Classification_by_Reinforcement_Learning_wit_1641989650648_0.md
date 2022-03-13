-
- In  computer  vision,  good  initial  work [7,14,15,11,9,5,12,16-20]has  been  undertaken.
  ls-type:: annotation
  hl-page:: 1
  id:: 61dec80f-2692-42c0-9488-a014db9e949b
  collapsed:: true
	- 14中，自适应的选择每张图片的分辨率，小物体为主则为高分辨率；大物体为主则选择小分辨率，降低计算成本。
	- 20中，基于连续奖励的解析梯度计算的策略搜索的q学习目标检测。
	- 23中，提出Q学习深度信念网络，使用深度自动编码器来提取特征作为智能体当前状态
	- 26中，这个我熟悉一些，使用强化学习来缩放和平移、细化目标检测框。
- Maximum  Power  Point  Tracking  (MPPT) 
  ls-type:: annotation
  hl-page:: 1
  id:: 61decaab-ad87-48a5-8303-31d00237f0cd
	- 本文工作的启发，最大功率点跟踪
- The technique involves using feature maps obtained from a  pre-trained  CNN  like  ResNet50 [30],  InceptionV3 [31], or  AlexNet [32].  Next,  reinforcement  learning  is  used  for optimal action proposal generation (rotation by a specific angle or translation) on the image. After application of the final  action  to  the  original  test  image,  and  obtaining  feature  map  from  the  CNN [33-36,30,31,37],  classification  is done using a second classifying structure, like a Support Vector Machine (SVM) [38-40]or a Neural Network (NN) which has been trained on the CNN feature maps of training images.
  ls-type:: annotation
  hl-page:: 1
  id:: 61decacd-34c9-4302-a2e7-b81769adefd3
	- 这个就很有意思了，本文的工作简述流程，由获得的特征图，强化学习生成最优动作决策（平移和旋转固定角度），将动作加到图片上之后再提取特征图，最后使用SVM等进行分类。
	- 这里就生成了两个问题
	  1. 为什么选择这两个动作，这明显是数据增强范围内的工作
	  2. 奖励是怎么设定的，是分类结果的好坏还是其他的
	-
- the Q-table has two rows and two/three columns
  ls-type:: annotation
  hl-page:: 2
  id:: 61ded2e5-ae91-40a7-b6e3-eb4231e325d8
	- 指的是两个状态以及两/三个行为
	- 两/三个行为前面已经提到了，是固定角度旋转以及平移，那么状态是指什么。
	- 前面以为是特征图，现在看来应该不是。
- [:span]
  ls-type:: annotation
  hl-page:: 2
  id:: 61deda34-1049-401f-a27b-2d1d76abd5f1
  hl-type:: area
  hl-stamp:: 1641994803400
	- 奖励函数的设计 [[61decacd-34c9-4302-a2e7-b81769adefd3]] ，回答奖励函数的设计
	- 这里其实通篇没有提及两个状态是什么，应该是原始的特征图以及添加了动作之后的特征图
	- 其他的更新方式和Q学习相同