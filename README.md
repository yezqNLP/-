# 达观杯信息抽取比赛代码记录

简单记录一下第一次比赛代码。

一开始采用了BiLSTM+CRF的模型，使用pytorch实现，即pytorch文件夹，但F1徘徊在0.8左右；故采用TensorFlow实现了BiLSTM+CRF模型，即tf文件夹，模型最好效果F1达到了0.88左右，继续调参没有效果；故采用了BERT预训练加fine-tune的模型，即BERT-pretrain和BERT-NER文件夹，效果最好达到了0.926（A 榜）。不同模型的的数据读取和评测代码略微有所改动，以BERT的为准。

> 比赛经验总结

模型的融合非常重要，没有采用模型融合导致最后结果调不上去。看了前10名的获奖ppt，发现普遍采用了多个模型的融合。

> 比赛结果（B榜）:

Rank：52/1261(4.1%); F1: 0.935（第1名0.949）


