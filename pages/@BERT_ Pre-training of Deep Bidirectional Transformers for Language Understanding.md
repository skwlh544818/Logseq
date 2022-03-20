links:: [Local library](zotero://select/library/items/JAUW6HHX), [Web library](https://www.zotero.org/users/8746250/items/JAUW6HHX)
authors:: Jacob Devlin, Ming-Wei Chang, Kenton Lee, Kristina Toutanova
short-title:: BERT
url:: https://aclanthology.org/N19-1423
original-title:: BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
access-date:: 2022-03-13T15:35:07Z
item-type:: [[conferencePaper]]
pages:: 4171–4186
title:: @BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
doi:: 10.18653/v1/N19-1423
proceedings-title:: "Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers)"
conference-name:: NAACL-HLT 2019
place:: "Minneapolis, Minnesota"
publisher:: Association for Computational Linguistics
archive-location:: 9999 citation(s)
date:: 2019-06
tags:: /unread

- [[Abstract]]
	- We introduce a new language representation model called BERT, which stands for Bidirectional Encoder Representations from Transformers. Unlike recent language representation models (Peters et al., 2018a; Radford et al., 2018), BERT is designed to pre-train deep bidirectional representations from unlabeled text by jointly conditioning on both left and right context in all layers. As a result, the pre-trained BERT model can be fine-tuned with just one additional output layer to create state-of-the-art models for a wide range of tasks, such as question answering and language inference, without substantial task-specific architecture modifications. BERT is conceptually simple and empirically powerful. It obtains new state-of-the-art results on eleven natural language processing tasks, including pushing the GLUE score to 80.5 (7.7 point absolute improvement), MultiNLI accuracy to 86.7% (4.6% absolute improvement), SQuAD v1.1 question answering Test F1 to 93.2 (1.5 point absolute improvement) and SQuAD v2.0 Test F1 to 83.1 (5.1 point absolute improvement).
- [[Attachments]]
	- [Devlin et al_2019_BERT.pdf](https://aclanthology.org/N19-1423.pdf) {{zotero-imported-file AK6MUUBV, "Devlin et al_2019_BERT.pdf"}}
- #transformer #自监督
- BERT这篇的一个模型就是将ELMo中使用的双向信息，与GPT中使用的transformer模型相结合的产物。与ELMo相比，BERT使用了更为先进的transformer模型来替换双向RNN模型。与GPT相比，BERT使用了transformer中的编码器来结合双向信息，而GPT使用的是解码器模块来汇聚单向信息。
- BERT在预训练阶段训练了两个任务，一个是Masked LM，另一个是Next Sentence Prediction 任务。第一个任务让模型学会利用上下文信息，也就是双向信息。第二个任务让模型学会理解句子之间的依赖关系。这两个任务也就是启发了后面的图像领域的MAE模型。
	- 这个阶段也就是无监督模型，现在更常叫自监督模型，其实就是不使用标签，而是自己设计一种方法让模型来学习数据之间的关系。这个方法是可以自己设计的隐含标签，比如第一个任务中学习Mask的词元，第二个任务中的二分类问题。
- BERT的成功可能并不像作者所说的那样，完全是双向信息的功劳。BERT展示了transformer提取全局特征的能力要优于CNN的能力。从这个方面来说，transformer比CNN更适合用在无监督或者自监督领域，它适合从这些杂乱无章的数据中提取他们全局的关系，来训练模型。
- 其实从本质上来说，自监督的任务设计就是变相的特征工程，不再是我们从数据中提取关键的特征，而是让程序去学特征，但是机器怎么学，只有我们人设计任务来引导。BERT中的两个任务就是让模型在大量的无标签数据上寻找特征，去做特征工程。
- 无监督，或者是自监督能够很好的在数据上寻找任务所需要的特征，但是一个最主要的特点就是模型参数量很大，以及开销很大，其实这不利于整个行业的发展的，学术的发展和工业的发展已经有点相互脱离了。
	-