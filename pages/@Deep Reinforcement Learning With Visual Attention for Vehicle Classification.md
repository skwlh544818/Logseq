tags:: [[分类]], [[已阅读]], [[强化学习]], [[重要]]
date:: 12/2017
issn:: "2379-8920, 2379-8939"
issue:: 4
extra:: 🏷️ 阅读中
doi:: 10.1109/tcds.2016.2614675
title:: @Deep Reinforcement Learning With Visual Attention for Vehicle Classification
pages:: 356-367
volume:: 9
item-type:: [[journalArticle]]
access-date:: 2021-12-05T02:48:44Z
call-number:: 3.379
rights:: ⭐⭐⭐⭐
original-title:: Deep Reinforcement Learning With Visual Attention for Vehicle Classification
language:: en
url:: http://ieeexplore.ieee.org/document/7580631/
publication-title:: IEEE Transactions on Cognitive and Developmental Systems
journal-abbreviation:: IEEE Trans. Cogn. Dev. Syst.
authors:: [[Dongbin Zhao]], [[Yaran Chen]], [[Le Lv]]
library-catalog:: 3
links:: [Local library](zotero://select/library/items/BHQT8T4W), [Web library](https://www.zotero.org/users/8746250/items/BHQT8T4W)

- [[Abstract]]
	- Automatic vehicle classiﬁcation is crucial to intelligent transportation system, especially for vehicle-tracking by police. Due to the complex lighting and image capture conditions, image-based vehicle classiﬁcation in real-world environments is still a challenging task and the performance is far from being satisfactory. However, owing to the mechanism of visual attention, the human vision system shows remarkable capability compared with the computer vision system, especially in distinguishing nuances processing. Inspired by this mechanism, we propose a convolutional neural network (CNN) model of visual attention for image classiﬁcation. A visual attention-based image processing module is used to highlight one part of an image and weaken the others, generating a focused image. Then the focused image is input into the CNN to be classiﬁed. According to the classiﬁcation probability distribution, we compute the information entropy to guide a reinforcement learning agent to achieve a better policy for image classiﬁcation to select the key parts of an image. Systematic experiments on a surveillance-nature dataset which contains images captured by surveillance cameras in the front view, demonstrate that the proposed model is more competitive than the large-scale CNN in vehicle classiﬁcation tasks.
	  id:: 6253c356-34bc-4e87-b634-b6cbba812ee1
- [[Attachments]]
	- [Zhao 等。 - 2017 - Deep Reinforcement Learning With Visual Attention .pdf](zotero://select/library/items/I3INKMG3) {{zotero-imported-file I3INKMG3, "Zhao 等。 - 2017 - Deep Reinforcement Learning With Visual Attention .pdf"}}
- #强化学习 #分类
- 本文主要是通过使用视觉注意机制来处理图片，然后利用CNN来进行分类，将得到的每个类别的概率计算信息熵来指导强化学习智能体来选择关注焦点，来进一步使用注意力机制来处理图片。
  id:: 6253c37a-e688-4bbe-8082-a99408dfa77e
	- 视觉注意机制：主要是仿人体视觉的方式，只关注图片物体的重点，而将不是重点的物体来模糊化
	- CNN：本文中的主干网络大概是使用的VGG网络
	- 信息熵：根据CNN得到的类别概率分布计算得到的，可以作为分类准确的置信度，信息熵越小，分类置信度越高；也可以作为给予强化学习的奖励标准。
	- 强化学习：用来选择图片上的重点区域，然后将重点区域与前几步的重点区域叠加后输入进视觉注意机制来模糊化。
- 视觉注意机制：$$X_f=f_d(X,\Phi)=\Phi \odot X$$,$$\phi_{ij}=sigmoid(d)=\frac{1}{1+exp(\alpha(d+\beta))}$$
	- 其中d是像素与焦点中心的距离，$$\alpha,\beta$$是超参数
- 信息熵：$$H(P)=E[-log(p_c)]=-\sum_{c=1}^Cp_clog(p_c)$$，然后进行归一化的操作$$H'(P)=\frac{H(P)}{log(C)}$$,
	- $p_c$是每个类别的概率
- 强化学习三元组：
	- 状态：经过视觉注意模块处理的图片
	- 行为：将注意焦点移动的方向和步数，一共是16个动作
	- 奖励：$$r_t = \begin{cases}0,& y=y^* \& H'(X_{mf})>H'(X_{mf}^{*})\\1,& y=y^* \& H'(X_{mf})\leq H'(X_{mf}^{*})\\ -1 & y!=y^*\end{cases}$$
- 这个文章的一个最大的启发就是提供了信息熵这个概念给我，我可以利用这个概念在现在的强化学习的分类实验上作为置信度。这个视觉注意力机制的处理，也很有意思，但是现在来看没有其他很大的利用场景。或许可以将这个机制利用在处理遮挡分类上
	- LATER 寻找一些遮挡的数据集，来看看其他处理方法。然后看一下这个方法