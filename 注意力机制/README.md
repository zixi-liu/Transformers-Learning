## Attention是一种加权平均
![image](https://github.com/user-attachments/assets/dca1f0f9-c1f3-44f3-a66f-93202a55f851)

Q表示query，表示的是K表示key，V表示value， dk是K的维度。

这个公式本质上就是表示按照关系矩阵进行加权平均。关系矩阵就是QK，而softmax就是把关系矩阵归一化到概率分布，然后按照这个概率分布对V进行重新采样，最终得到新的attention的结果。

![image](https://github.com/user-attachments/assets/e9063fc4-b49b-4a21-9a81-01e9be128d60)

[图解Transformer](https://github.com/datawhalechina/learn-nlp-with-transformers/blob/main/docs/%E7%AF%87%E7%AB%A02-Transformer%E7%9B%B8%E5%85%B3%E5%8E%9F%E7%90%86/2.2-%E5%9B%BE%E8%A7%A3transformer.md)
- Transformer模型对每个输入的词向量都加上了一个位置向量。这些向量有助于确定每个单词的位置特征，或者句子中不同单词之间的距离特征。词向量加上位置向量背后的直觉是：将这些表示位置的向量添加到词向量中，得到的新向量，可以为模型提供更多有意义的信息，比如词的位置，词之间的距离等。

- 计算Attention Score（注意力分数）。

## 多头注意力机制

## Bert系列大规模无监督学习

BERT创造性地提出在大规模数据集上无监督预训练加目标数据集微调（fine-tune）的方式，采用统一的模型解决大量的不同问题。
BERT的做法其实非常简单，本质就是大规模预训练。利用大规模数据学习得到其中的语义信息，再把这种语义信息运用到小规模数据集上。BERT的贡献主要是：1）提出了一种双向预训练的方式。（2）证明了可以用一种统一的模型来解决不同的任务，而不用为不同的任务设计不同的网络。（3）在11个自然语言处理任务上取得了提升。
BERT提出了几个简单的无监督的预训练方式。第一个是Mask LM，就是挡住一句话的一部分，去预测另外一部分。第二个是Next Sentence Prediction (NSP) ，就是预测下一句话是什么。这种简单的预训练使得BERT抓住了一些基本的语义信息和逻辑关系，帮助BERT在下流任务取得了非凡的成就。
