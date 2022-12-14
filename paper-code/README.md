Paper-Recurrence | Still work
========================

由于考虑到部分模型及思路想法的复现代码量比较大，集中放在一个仓库中不合适，所以这里将一些代码量较大的项目分离到单独的仓库中，并通过引用指向。

# Notice | 特别说明
**特别说明**：此处模型代码为纯模型结构的代码，且都经过本人训练、测试、评价使用无误的代码，在代码关键处我添加了必要的注释，可以放心使用。

目前我的想法是直接复现论文时，只上传模型结构的代码，这样有利于缩小项目体积（后续逐步构建完善）。当然，如果有对部分复现代码感兴趣的伙伴，想要提出交流或者想要我实现完整过程等，欢迎提Issue。

# Data | 数据
1. [smudict](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/data/cmudict-0.7b)
2. [thchs30](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/data/lexicon.txt)
3. [ubuntu corpus](http://dataset.cs.mcgill.ca/ubuntu-corpus-1.0/)
4. TrecQA：TrecQA是QA最广泛评估和长期作为标准的数据集之一，用于回答基于事实的问题的任务
5. QatarLiving：答案通常是主观的而不是事实的，在这个数据集中，每个问题有十个答案，标记为“正向”和“负向”
6. Tweet Reply Prediction：数据集中包含对知名品牌的Tweet-Response对

7. [ETT(变电站温度数据)](https://github.com/zhouhaoyi/ETDataset)
8. [ECL(耗电量数据)](https://archive.ics.uci.edu/ml/datasets/ElectricityLoadDiagrams20112014)
9. [天气数据](https://www.ncdc.noaa.gov/orders/qclcd/)
10. [DailyDialog++](https://github.com/iitmnlp/Dialogue-Evaluation-with-BERT)：DailyDialog数据集的升级版，11K的多轮对话上下文，每个上下文包括五个标准的参考回复、五个不相关的回复、五个随机挑选的回复
11. [DailyDialog: A Manually Labelled Multi-turn Dialogue Dataset](https://drive.google.com/file/d/1sj3Z_GZfYzrhmleWazA-QawhUEhlNmJd/view?usp=sharing)：包含对话意图和情感信息的多轮对话数据集

# Code | 模型代码

1. [Byte Pair Encoding（BPE）](https://github.com/DengBoCong/paper/blob/master/paper-code/bpe.py)：论文代码
2. [Batch Normalization](https://github.com/DengBoCong/paper/blob/master/paper-code/batch_normalization.py)
3. [Cosine Normalization](https://github.com/DengBoCong/paper/blob/master/paper-code/conv2d_cosnorm.py)
4. [Group Normalization](https://github.com/DengBoCong/paper/blob/master/paper-code/group_normalization.py)：论文代码
5. [data_enhancement](https://github.com/DengBoCong/paper/blob/master/paper-code/data_enhancement.py)：文本匹配中句子对数据增强

6. [SIF和USIF](https://github.com/DengBoCong/sentence2vec/blob/main/sentence2vec/transform.py)：SIF和uSIF的Sentence Embedding实现

## Tensorflow2.3
### Tools
1. [en_text_to_phoneme](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/tools/en_text_to_phoneme.py)：文本转音素的切分方式
2. [preprocess_tfrecord](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/tools/preprocess_tfrecord.py)：TFRecord格式保存以及Dataset加载
3. [attention](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/tools/attention.py)：加法、点乘、自注意力等各类Attention实现
4. [logME](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/tools/logME.py)：预训练模型评估方法


### Models
1. [Transformer](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/transformer.py)
2. [Scheduled Sampling for Transformer](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/transformer.py)
3. [GPT2](https://github.com/DengBoCong/paper/blob/master/paper-code/tensorflow_src/models/gpt2.py)
4. [GPT2-TF2.3完整仓库](https://github.com/DengBoCong/GPT2-TF2.3)：使用GPT2以及TensorFlow2.3实现闲聊，后续更新PyTorch。
5. [Sequential Matching Network](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/smn.py)
6. [Seq-to-Seq base](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/seq2seq.py)
7. [Neural Belief Tracker](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/nbt.py)
8. [An End-to-End Trainable Neural Network Model with Belief Tracking for Task-Oriented Dialog](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/task)
9. [SMN](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/smn.py)
10. [DAM](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/DAM.py)
11. [Informer](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/informer.py)
12. [InferSent](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/tensorflow_src/models/InferSent.py)：七种方式中，选用BiLSTM+Max Pooling+BERT Base融合

## Pytorch1.7.0
[Seq-to-Seq base](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/pytorch_src/seq2seq)：包含完整数据处理、训练、对话、模型保存恢复等代码

### Tools
[logME](https://github.com/DengBoCong/nlp-paper/blob/master/paper-code/pytorch_src/logME.py)：预训练模型评估方法