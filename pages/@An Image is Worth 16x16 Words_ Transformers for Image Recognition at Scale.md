links:: [Local library](zotero://select/library/items/AG9KSSA5), [Web library](https://www.zotero.org/users/8746250/items/AG9KSSA5)
authors:: Alexey Dosovitskiy, Lucas Beyer, Alexander Kolesnikov, Dirk Weissenborn, Xiaohua Zhai, Thomas Unterthiner, Mostafa Dehghani, Matthias Minderer, Georg Heigold, Sylvain Gelly, Jakob Uszkoreit, Neil Houlsby
short-title:: An Image is Worth 16x16 Words
url:: https://openreview.net/forum?id=YicbFdNTTy
language:: en
original-title:: An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale
rights:: ⭐⭐⭐⭐
access-date:: 2022-03-18T09:11:47Z
item-type:: [[conferencePaper]]
title:: @An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale
conference-name:: International Conference on Learning Representations
date:: [[Sep 28th, 2020]]
tags:: /unread, 已阅读

- [[Abstract]]
	- While the Transformer architecture has become the de-facto standard for natural language processing tasks, its applications to computer vision remain limited. In vision, attention is either applied...
- [[Attachments]]
	- [Dosovitskiy et al_2020_An Image is Worth 16x16 Words.pdf](https://openreview.net/pdf?id=YicbFdNTTy) {{zotero-imported-file UFFFIJ2G, "Dosovitskiy et al_2020_An Image is Worth 16x16 Words.pdf"}}
	- [Snapshot](https://openreview.net/forum?id=YicbFdNTTy) {{zotero-imported-file NMTWXWB3, "forum.html"}}
	- {{https://b23.tv/BV15P4y137jb}}
-
- 什么是归纳偏置
	- 归纳偏置也就是说是先验知识，在使用卷积神经网络时，我们引入了两个归纳偏置，一个是locality，也就是说在图片上相邻的区域有相同的特征，这个在生活中比较认同。
	- 第二个是平移等变性，transform equivalence，从公式上说就是$$f(g(x))=g(f(x))$$
	- ViT中使用了很少的归纳偏置
- 什么是few-shot accuracy
	- 这个概念是说，我们得到一个预训练模型后，不进行微调操作，直接在数据集每个类别中选取少量的数据来进行测试精度。这样可以很快的评估一个模型，节省算力等操作。
-
- 这篇文章主要讲了将图片切成每个patch作为transformer的输入