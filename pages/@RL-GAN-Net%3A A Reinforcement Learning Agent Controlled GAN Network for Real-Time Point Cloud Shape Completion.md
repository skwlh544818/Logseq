links:: [Local library](zotero://select/library/items/LFANJN2P), [Web library](https://www.zotero.org/users/8746250/items/LFANJN2P)
library-catalog:: openaccess.thecvf.com
authors:: Muhammad Sarmad, Hyunjoo Jenny Lee, Young Min Kim
short-title:: RL-GAN-Net
url:: https://openaccess.thecvf.com/content_CVPR_2019/html/Sarmad_RL-GAN-Net_A_Reinforcement_Learning_Agent_Controlled_GAN_Network_for_Real-Time_CVPR_2019_paper.html
original-title:: RL-GAN-Net: A Reinforcement Learning Agent Controlled GAN Network for Real-Time Point Cloud Shape Completion
access-date:: 2022-03-24T13:38:38Z
item-type:: [[conferencePaper]]
pages:: 5898-5907
title:: @RL-GAN-Net: A Reinforcement Learning Agent Controlled GAN Network for Real-Time Point Cloud Shape Completion
conference-name:: Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition
date:: 2019
tags:: /unread, 待读

- [[Attachments]]
	- [Sarmad et al_2019_RL-GAN-Net.pdf](http://openaccess.thecvf.com/content_CVPR_2019/papers/Sarmad_RL-GAN-Net_A_Reinforcement_Learning_Agent_Controlled_GAN_Network_for_Real-Time_CVPR_2019_paper.pdf) {{zotero-imported-file NRBYPGCT, "Sarmad et al_2019_RL-GAN-Net.pdf"}}
- #GAN #强化学习 #点云恢复
- 这个文章使用强化学习、GAN以及AE相结合的方式来恢复点云形状，编码器将不完整的点云编码成潜在特征，该潜在特征会作为强化学习的状态产生出GAN所需要的噪声z，GAN根据噪声z会模拟出全局的潜在特征，解码器会根据全局的潜在特征产生出全局的点云，也就恢复成了原先的形状。
- GAN和AE均是在数据集上预训练过的模型
- 强化学习四要素：
	- 环境：整个实验模型框架
	- 状态：AE的编码器转换的不完整点云的潜在特征
	- 行为：GAN所需要的噪声z
	- 奖励：三个损失函数权重的加和
		- 1. Chamfer loss：$$L_{C H}=d_{C H}\left(P_{i n}, E^{-1}(G(z))\right)$$，$$ E^{-1}$$是解码器
		- $$d_{C H}\left(P_{1}, P_{2}\right)=\sum_{a \in P_{1}} \min _{b \in P_{2}}\|a-b\|_{2}^{2}+\sum_{b \in P_{2}} \min _{a \in P_{1}}\|a-b\|_{2}^{2}$$
		- 2. GFV loss：$$L_{G F V}=\left\|G(z)-E\left(P_{i n}\right)\right\|_{2}^{2}$$，产生器与编码器之间的损失
		- 3. Discriminator loss：$$L_{D}=-D(G(z))$$，GAN网络的损失
		- $$r=w_{C H} \cdot r_{C H}+w_{G F V} \cdot r_{G F V}+w_{D} \cdot r_{D}$$
- 这个文章比较重要的一个贡献就是使用强化学习控制GAN模型，为GAN模型提供一个合适的输入
- 实验结果部分也并没有与其他实验进行过多的对比，大部分都是自验证，并且没有一个合适的指标，只有一个大致相似性。不过也提供了一个比较好的实验行为，实验结果对比有一些问题的话是需要进行解释的，或者说是自己的猜想。
- 对于模型形成错误的形状的实验结果，为什么会出现这种情况，该如何改进
	- 对于RL-GAN模型出现与原形状不符的形状，我觉得是因为缺少局部特征造成的。整个实验只使用了全局的特征，并没有使用局部特征，会形成整体上相似，或者说类别相同，但是局部上不相同的状况。但是AE模型形成的形状虽然缺少了一些全局的细节，但是对于局部的特征却复现了出来。
	- TODO 模型的最后是在AE形成的模型与RL-GAN模型中二选一，是不是可以结合两者的模型形状，而不是二选一 #TODO
	- TODO 或者说可以提供给RL-GAN模型一些局部特征，比如在GFV loss那里 #TODO
- 文章中的指出强化学习用来提出边界框的位置，用来寻找分割的种子点
- 后续的进展则有，将类似的思想用在图像修复上，我也想着可以用在图像遮挡上处理。
-