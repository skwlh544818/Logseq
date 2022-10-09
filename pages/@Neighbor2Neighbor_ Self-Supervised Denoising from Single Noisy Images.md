links:: [Local library](zotero://select/library/items/2Q6L32CN), [Web library](https://www.zotero.org/users/8746250/items/2Q6L32CN)
library-catalog:: DOI.org (Crossref)
authors:: Tao Huang, Songjiang Li, Xu Jia, Huchuan Lu, Jianzhuang Liu
short-title:: Neighbor2Neighbor
url:: https://ieeexplore.ieee.org/document/9577596/
language:: en
original-title:: Neighbor2Neighbor: Self-Supervised Denoising from Single Noisy Images
access-date:: 2022-04-18T13:48:37Z
item-type:: [[conferencePaper]]
pages:: 14776-14785
title:: @Neighbor2Neighbor: Self-Supervised Denoising from Single Noisy Images
doi:: 10.1109/CVPR46437.2021.01454
isbn:: 978-1-66544-509-2
proceedings-title:: 2021 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)
conference-name:: 2021 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)
place:: "Nashville, TN, USA"
publisher:: IEEE
archive-location:: 18 citation(s)
date:: 6/2021
tags:: /unread

- [[Abstract]]
	- In the last few years, image denoising has beneﬁted a lot from the fast development of neural networks. However, the requirement of large amounts of noisy-clean image pairs for supervision limits the wide use of these models. Although there have been a few attempts in training an image denoising model with only single noisy images, existing self-supervised denoising approaches suffer from inefﬁcient network training, loss of useful information, or dependence on noise modeling. In this paper, we present a very simple yet effective method named Neighbor2Neighbor to train an effective image denoising model with only noisy images. Firstly, a random neighbor sub-sampler is proposed for the generation of training image pairs. In detail, input and target used to train a network are images sub-sampled from the same noisy image, satisfying the requirement that paired pixels of paired images are neighbors and have very similar appearance with each other. Secondly, a denoising network is trained on sub-sampled training pairs generated in the ﬁrst stage, with a proposed regularizer as additional loss for better performance. The proposed Neighbor2Neighbor framework is able to enjoy the progress of state-of-the-art supervised denoising networks in network architecture design. Moreover, it avoids heavy dependence on the assumption of the noise distribution. We explain our approach from a theoretical perspective and further validate it through extensive experiments, including synthetic experiments with different noise distributions in sRGB space and real-world experiments on a denoising benchmark dataset in raw-RGB space.
- [[Attachments]]
	- [Huang 等。 - 2021 - Neighbor2Neighbor Self-Supervised Denoising from .pdf](zotero://select/library/items/HUAKZ5J6) {{zotero-imported-file HUAKZ5J6, "Huang 等。 - 2021 - Neighbor2Neighbor Self-Supervised Denoising from .pdf"}}
- #图像去噪
- 本文是在noise2noise的基础上进行改进的，一共改进了两点，一个是noise2noise是使用两张噪声图片进行的训练。本文使用采样的方法将单张图片转换成了两张图片，然后输入进noise2noise网络架构。这是单张图片的自监督方式。第二点就是由于是采样得来的两张图片，所以并不完全符合noise2noise的理论，作者在损失函数上加上了约束项。
- 采样方式：
	- 作者采用了随机采样的方式，首先将图片的分割成$\frac{H}{2}\times\frac{W}{2}$个小块，每个小块内有四个像素，从四个像素中选择相邻的两个像素块来分别当作采样图片的一个像素。
- 约束项：
	- 根据理想状态下最优的去噪函数应该存在的特征，来约束所设计的损失函数，这样可以使得所设计的网络会朝着理想最优的状况优化。最后作者使用拉格朗日乘子法将约束转变成了正则化项。
- 这个论文是对noise2noise的改进，在这个论文上进一步改进其实是没有什么好想法的，不过这个设计理念则是有一些用处，比如将这个采样的方式用在其他需要两张图片的架构中完成其他任务。现在能想到的一个方式就是双目深度估计。