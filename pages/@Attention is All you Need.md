tags:: [[/unread]], [[⛔ No DOI found]], [[已阅读]], [[重要]]
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
- Transformer中使用了layer norm，不是batch norm
	- TODO layer norm和batch norm的区别
	- TODO 这里为什么要用layer norm
-