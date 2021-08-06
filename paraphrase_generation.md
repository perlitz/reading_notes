# Paraphrase Generation

## Datasets

> A list of datasets is in https://github.com/wasiahmad/paraphrase_identification/tree/master/dataset



[ParaBank: Monolingual Bitext Generation and Sentential Paraphrasing via Lexically-constrained Neural Machine Translation](https://arxiv.org/abs/1901.03644) [data](https://nlp.jhu.edu/parabank/)

> 

##### [ParaBank2: Large-scale, Diverse, Paraphrastic Bitexts via Sampling and Clustering (Hu 19)](Large-scale, Diverse, Paraphrastic Bitexts via Sampling and Clustering (Hu 19)) [data](https://nlp.jhu.edu/parabank/)

> Summarize

##### [TwitterPPDB: A Continuously Growing Dataset of Sentential Paraphrases (Lan 17)](https://www.aclweb.org/anthology/D17-1126.pdf) [data](https://languagenet.github.io/)

> A collection of sentence level paraphrases from Twitter by linking tweets through shared URLs. This corpus is the largest up to date with 51,524 human annotated sentence pairs: 42200 for training and 9324 for testing. 

##### [ParaSCI](https://wanxiaojun.github.io/EACL2021Camera.pdf) [data](https://github.com/dqxiu/ParaSCI)

> large-scale paraphrase dataset in the scientific field, including 33,981 paraphrase pairs from ACL (ParaSCI-ACL) and 316,063 pairs from arXiv (ParaSCI-arXiv).

##### [WikiMatrix: Mining 135M Parallel Sentences in 1620 Language Pairs from Wikipedia](https://arxiv.org/pdf/1907.05791.pdf)

> A dataset including different language Bitext extracted from wikipedia with a semantic score above some threshold.

##### [PAWS: Paraphrase Adversaries from Word Scrambling](PAWS Paraphrase Adversaries from Word Scrambling)

> A dataset offering better data for paraphrase **classifications**, their innovation is in hard pairs, ones with large BOW overlap but different meanings.

##### [MRPC: Automatically Constructing a Corpus of Sentential Paraphrases](https://aclanthology.org/I05-5002.pdf) [data](https://deepai.org/dataset/mrpc)

> Contains 5,801 pairs of sentences with 4,076 for training and the remaining 1,725 for testing. 

##### [MSCOCO paraphrase](http://images.cocodataset.org/annotations/annotations_trainval2014.zip) :

> 328,000 images with 5 different sentences describing the corresponding image.

##### [QQP: Quora Question Paris](https://quoradata.quora.com/First-Quora-Dataset-Release-Question-Pairs)

> A large dataset (~400K) extracted from Quora questions that were classified as duplicates, offers more diverse paraphrases than other datasets, however, all sentences are in the form of questions. 

##### [ParaNMT-50M: Pushing the Limits of Paraphrastic Sentence Embeddings with Millions of Machine Translations](PARANMT-50M)

>  A dataset created automatically by back-translation Czech side of a Czech-English corpus, creating a Bitext that represents paraphrases. 

##### [PPDB 2.0: Better paraphrase ranking, fine-grained entailment relations, word embeddings, and style classification (Pavlick 15)](https://aclanthology.org/P15-2070.pdf) [data](http://paraphrase.org/#/download)

> 100m+ paraphrases, and 26k manually rated phrase pairs.

##### [Paralex: Paraphrase-Driven Learning for Open Question Answering (Fader 13)](http://knowitall.cs.washington.edu/paralex/acl2013-paralex.pdf) [data](http://knowitall.cs.washington.edu/paralex/)

> Paralex learns from a collection of 18 million question-paraphrase pairs scraped from WikiAnswers.

## Methods

##### [Paraphrasing with Large Language Models (Witteveen 19)](Paraphrasing with Large Language Models (Witteveen 19).md)

> #print

##### [Neural-Driven Search-Based Paraphrase Generation (Fabre 21)](Neural-Driven Search-Based Paraphrase Generation (Fabre 21).md)

> Introduce a search based paraphrasing generation in which the search is guided by a combination of Semantic score (BERT), Fluency (GPT2) and Diversity (Char-Level)

##### [LBoW: Paraphrase Generation with Latent Bag of Words (Fu 20)](Paraphrase Generation with Latent Bag of Words.md)

> Some kind of SOTA… #print

##### [Transformer and seq2seq model for Paraphrase Generation (Egonmwan 19)](Transformer and seq2seq model for Paraphrase Generation (Egonmwan 19).md)

> Proposes an architecture for paraphrasing using a RNN-GRU encoder-decoder with an additional Transformer encoder before.

##### [Exploring Diverse Expressions for Paraphrase Generation (Qian 19)](Exploring Diverse Expressions for Paraphrase Generation (Qian 19).md)

> #print

##### [An End-to-End Generative Architecture for Paraphrase Generation (Yang 19)](An End-to-End Generative Architecture for Paraphrase Generation (Yang 19).md)

> TODO

##### [Automatic Machine Translation Evaluation in Many Languages via Zero-Shot Paraphrasing ( Thompson 2020)](Automatic Machine Translation Evaluation in Many Languages via Zero-Shot Paraphrasing ( Thompson 2020).md)

> TODO

##### [Paraphrase Generation as Zero-Shot Multilingual Translation: Disentangling Semantic Similarity from Lexical and Syntactic Diversity (Thompson 2020)](Paraphrase Generation as Zero-Shot Multilingual Translation Disentangling Semantic Similarity from Lexical and Syntacti.md)

>TODO

##### [SOW+REAP: Neural Syntactic Preordering for Controlled Paraphrase Generation (Goyal 2020)](SOW+REAP Neural Syntactic Preordering for Controlled Paraphrase Generation (Goyal 2020).md)

> Increase the diversity of paraphrasing by introducing an additional module that selects possible reordering and passes the different options to the paraphraser as positional encodings.

##### [SCPN: Adversarial Example Generation with Syntactically Controlled Paraphrase Networks (Iyyer 2018)](Adversarial Example Generation with Syntactically Controlled Paraphrase Networks (Iyyer 2018).md)

> Syntactically controlled paraphrase generation. Using a parser, label the syntactic variation in large back-translated data, which provides training data for SCPN. The model favors syntactical variations to lexical ones, generates adversarial examples that fool pre-trained NLP models and can improve robustness upon training.

##### [An End-to-End Generative Architecture for Paraphrase Generation (Yang 2019)](https://aclanthology.org/D19-1309.pdf)

> Using a VAE… TODO

##### [A Deep Generative Framework for Paraphrase Generation (Gupta 2017)](https://arxiv.org/pdf/1709.05074.pdf)

> Using a VAE LSTM… TODO

##### [Unsupervised Paraphrase Generation via Dynamic Blocking (Niu 2020)](Unsupervised Paraphrase Generation via Dynamic Blocking (Niu 2020).md)

> Proposes a generation trick (forbid chains of input tokens in the outputs) that improves the diversity of PG in an unsupervised manner

##### [SGCP: Syntax-Guided Controlled Generation of Paraphrases (Kumar 2020)](SGCP Syntax-Guided Controlled Generation of Paraphrases (Kumar 2020).md)

>  TODO

##### [Controllable Paraphrase Generation with a Syntactic Exemplar (Chen 2019)](Controllable Paraphrase Generation with a Syntactic Exemplar (Chen 2019).md)

> TODO

##### [Paraphrase Generation with Deep Reinforcement Learning (Li 2018)](Paraphrase Generation with Deep Reinforcement Learning (Li 2018).md)

> TODO

##### [Unsupervised Paraphrase Generation using Pre-trained Language Models (Hegde 2020)](https://arxiv.org/pdf/2006.05477.pdf)

In this paper we **leverage this generation capability of GPT-2 to generate paraphrases without any supervision from labelled data.** 

We examine how the results compare with other supervised and unsupervised approaches and the effect of using paraphrases for data augmentation on downstream tasks such as classification. 

Our experiments show that paraphrases generated with our model are of good quality, are diverse and improves the downstream task performance when used for data augmentation.

##### [Style-transfer and Paraphrase: Looking for a Sensible Semantic Similarity Metric (Yamshchikov 2020)](https://arxiv.org/pdf/2004.05001.pdf)

The rapid development of such natural language processing tasks as style transfer, paraphrase, and machine translation often **calls for the use of semantic similarity metrics**. In recent years a lot of methods to measure the semantic s

imilarity of two short texts were developed. This paper provides a comprehensive analysis for more than a dozen of such methods. 

Using a **new dataset of fourteen thousand sentence pairs human-labeled according to their semantic similarity**, we demonstrate that **none of the metrics widely used in the literature is close enough to human judgment in these tasks.** A number of recently proposed metrics provide comparable results, yet Word Mover Distance is shown to be the most reasonable solution to measure semantic similarity in reformulated texts at the moment

##### [An Empirical Comparison on Imitation Learning and Reinforcement Learning for Paraphrase Generation (Du 2019)](https://arxiv.org/pdf/1908.10835.pdf)

Generating paraphrases from given sentences involves decoding words step by step from a large vocabulary. To learn a decoder, supervised learning which maximizes the likelihood of tokens always suffers from the exposure bias. Although both reinforcement learning (RL) and imitation learning (IL) have been widely used to alleviate the bias, the lack of direct comparison leads to only a partial image on their benefits. In this work, we present an empirical study on how RL and IL can help boost the performance of generating paraphrases, with the pointer-generator as a base model 1 . Experiments on the benchmark datasets show that (1) imitation learning is constantly better than reinforcement learning; and (2) the pointer-generator models with imitation learning outperform the state-of-theart methods with a large margin.