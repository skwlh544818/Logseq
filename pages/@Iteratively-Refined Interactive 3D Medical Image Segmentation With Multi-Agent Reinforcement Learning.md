tags:: [[/unread]]
date:: 6/2020
publisher:: IEEE
place:: "Seattle, WA, USA"
conference-name:: 2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)
proceedings-title:: 2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)
extra:: ZSCC: 0000019
isbn:: 978-1-72817-168-5
doi:: 10/ghbbzs
title:: @Iteratively-Refined Interactive 3D Medical Image Segmentation With Multi-Agent Reinforcement Learning
pages:: 9391-9399
item-type:: [[conferencePaper]]
access-date:: 2021-12-03T14:16:48Z
original-title:: Iteratively-Refined Interactive 3D Medical Image Segmentation With Multi-Agent Reinforcement Learning
language:: en
url:: https://ieeexplore.ieee.org/document/9157356/
authors:: [[Xuan Liao]], [[Wenhao Li]], [[Qisen Xu]], [[Xiangfeng Wang]], [[Bo Jin]], [[Xiaoyun Zhang]], [[Yanfeng Wang]], [[Ya Zhang]]
links:: [Local library](zotero://select/library/items/FY4GP6ZP), [Web library](https://www.zotero.org/users/8746250/items/FY4GP6ZP)

- [[Abstract]]
	- Existing automatic 3D image segmentation methods usually fail to meet the clinic use. Many studies have explored an interactive strategy to improve the image segmentation performance by iteratively incorporating user hints. However, the dynamic process for successive interactions is largely ignored. We here propose to model the dynamic process of iterative interactive image segmentation as a Markov decision process (MDP) and solve it with reinforcement learning (RL). Unfortunately, it is intractable to use single-agent RL for voxel-wise prediction due to the large exploration space. To reduce the exploration space to a tractable size, we treat each voxel as an agent with a shared voxel-level behavior strategy so that it can be solved with multi-agent reinforcement learning. An additional advantage of this multi-agent model is to capture the dependency among voxels for segmentation task. Meanwhile, to enrich the information of previous segmentations, we reserve the prediction uncertainty in the state space of MDP and derive an adjustment action space leading to a more precise and ﬁner segmentation. In addition, to improve the efﬁciency of exploration, we design a relative cross-entropy gain-based reward to update the policy in a constrained direction. Experimental results on various medical datasets have shown that our method signiﬁcantly outperforms existing state-ofthe-art methods, with the advantage of fewer interactions and a faster convergence.
- [[Attachments]]
	- [Liao 等。 - 2020 - Iteratively-Refined Interactive 3D Medical Image S.pdf](zotero://select/library/items/E9EPR263) {{zotero-imported-file E9EPR263, "Liao 等。 - 2020 - Iteratively-Refined Interactive 3D Medical Image S.pdf"}}