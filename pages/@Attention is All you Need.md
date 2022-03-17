tags:: [[/unread]], [[⛔ No DOI found]], [[已阅读]], [[重要]], [[transformer]] 
date:: 2017
publisher:: "Curran Associates, Inc."
proceedings-title:: Advances in Neural Information Processing Systems
title:: @Attention is All you Need
volume:: 30
item-type:: [[conferencePaper]]
access-date:: 2022-03-14T07:10:56Z
rights:: ⭐⭐⭐⭐⭐
original-title:: Attention is All you Need
url:: https://proceedings.neurips.cc/paper/2017/hash/3f5ee243547dee91fbd053c1c4a845aa-Abstract.html
authors:: [[Ashish Vaswani]], [[Noam Shazeer]], [[Niki Parmar]], [[Jakob Uszkoreit]], [[Llion Jones]], [[Aidan N Gomez]], [[Łukasz Kaiser]], [[Illia Polosukhin]]
library-catalog:: Neural Information Processing Systems
links:: [Local library](zotero://select/library/items/GCHSHNNB), [Web library](https://www.zotero.org/users/8746250/items/GCHSHNNB)

- [[Attachments]]
	- [Vaswani et al_2017_Attention is All you Need.pdf](https://proceedings.neurips.cc/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf) {{zotero-imported-file KUU52WAB, "Vaswani et al_2017_Attention is All you Need.pdf"}}
- 这篇文章提出了一种处理语言翻译的新框架--Transformer，其没有使用RNN等网络，而是使用了多头自注意力机制的方法。相比与RNN等方法，Transformer提高了网络并行性以及减少了所需操作数，进而提高了运行速度。
- DONE  RNN等网络除了并行等问题以外，是什么促使作者选择了Transformer架构
  :LOGBOOK:
  CLOCK: [2022-03-14 Mon 22:08:27]--[2022-03-14 Mon 22:08:27] =>  00:00:00
  CLOCK: [2022-03-14 Mon 22:08:28]--[2022-03-14 Mon 22:08:28] =>  00:00:00
  CLOCK: [2022-03-14 Mon 22:08:29]--[2022-03-14 Mon 22:08:30] =>  00:00:01
  :END:
	- 好像就是因为顺序的句子结构无法并行，以及自注意力机制的广发使用，才促使了transformer的产生
	-
- Transformer中使用了layer norm，不是batch norm/
	- DONE layer norm和batch norm的区别 [[Mar 15th, 2022]]
	  :LOGBOOK:
	  CLOCK: [2022-03-14 Mon 22:18:52]--[2022-03-14 Mon 22:18:53] =>  00:00:01
	  :END:
		- batch norm对一个batch-size样本内的每个特征做归一化，layer norm 对每条样本的所有特征做归一化，两者都是在深度学习中让当前层的参数稳定下来，避免梯度消失或者梯度爆炸，方便后面的继续学习。
		- 如果特征依赖不同样本的统计参数，那Batch Norm更有效， 因为它不考虑不同特征之间的大小关系，但是保留不同样本间的大小关系。
		- NLP领域适合用LayerNorm， CV适合BatchNorm
		- batch norm训练阶段需要保存每个batch的均值和方差，以求出整体均值和方差在infrence阶段使用
	- DONE 这里为什么要用layer norm [[Mar 15th, 2022]]
		- 由于各个样本的特征长度长短不一，如果对没个batch做norm的话，会导致在特征缺少的特征处，求得的batch norm浮动比较大，layer norm相对稳定
		- NLP任务不考虑不同样本间的大小关系，无需保留样本内不同特征之间的大小关系
-
-