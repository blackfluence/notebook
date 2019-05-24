## Sequence Tagging

### Bidirectional LSTM-CRF Models for Sequence Tagging

Code: https://pytorch.org/tutorials/beginner/nlp/advanced_tutorial.html#bi-lstm-conditional-random-field-discussion

Abstract: 第一个将LSTM-CRF用于做NLP任务的论文，分别采用了lstm和bi-lstm的output作为crf的**Features**。rnn层学习词的上下文信息，crf层学习句子级表示。

### Empower Sequence Labeling with Task-Aware Neural Language Model

Code: https://github.com/LiyuanLucasLiu/LM-LSTM-CRF

Abstract: 这篇论文使用的基于字的bi-lstm到基于词的bi-lstm，然后crf层学习特征输出Tag。

## Bert

https://github.com/huggingface/pytorch-pretrained-BERT
https://github.com/google-research/bert
BERT-Base, Chinese: Chinese Simplified and Traditional, 12-layer, 768-hidden, 12-heads, 110M parameters

https://syncedreview.com/2019/02/15/microsofts-new-mt-dnn-outperforms-google-bert/

### Multi-Task Deep Neural Networks for Natural Language Understanding

https://syncedreview.com/2019/02/15/microsofts-new-mt-dnn-outperforms-google-bert/
Code：https://github.com/namisan/mt-dnn

Abstract：

### BERT-BiLSMT-CRF-NER

Code：https://github.com/macanv/BERT-BiLSTM-CRF-NER
Tutorial：https://blog.csdn.net/macanv/article/details/85684284

**benchmark**

https://github.com/Embedding/Chinese-Word-Vectors
Toolkits: All word vectors are trained by [ngram2vec](https://github.com/zhezhaoa/ngram2vec/) toolkit. Ngram2vec toolkit is a superset of [word2vec](https://github.com/svn2github/word2vec) and [fasttext](https://github.com/facebookresearch/fastText) toolkit, where arbitrary context features and models are supported.

## Mutil-Task Learning





------

http://www.52nlp.cn/tag/google-bert
