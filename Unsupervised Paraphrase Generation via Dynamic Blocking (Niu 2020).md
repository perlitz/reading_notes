# [Unsupervised Paraphrase Generation via Dynamic Blocking (Niu 2020)](https://arxiv.org/pdf/2010.12885.pdf)

We propose Dynamic Blocking, a **decoding algorithm** which enables large-scale pretrained autoregressive models (such as BART, T5, GPT-2 and XLNet) to **generate high-quality paraphrases in an unsupervised setting**. 

In order to obtain an alternative surface form, **whenever the language model emits a token that is present in the source sequence, we prevent the model from generating the subsequent source token for the next time step.** 

**We show that our approach achieves state-of-the-art results on benchmark datasets when compared to previous unsupervised approaches**, and is even comparable with strong supervised, indomain models. 

We also propose a new automatic metric based on **self-BLEU and BERTscore** which not only discourages the model from copying the input through, but also evaluates text similarity based on distributed representations, hence avoiding reliance on exact keyword matching. In addition, we demonstrate that our model generalizes across languages without any additional training.