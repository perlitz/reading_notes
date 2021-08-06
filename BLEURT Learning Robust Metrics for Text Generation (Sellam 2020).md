# [BLEURT: Learning Robust Metrics for Text Generation (Sellam 2020)](https://arxiv.org/pdf/2004.04696.pdf)

BLEURT, a learned evaluation metric based on BERT that can model human judgments with a **few thousand possibly biased training examples.** 

A key aspect of our approach is a **novel pre-training scheme that uses millions of synthetic examples to help the model generalize.** 

BLEURT provides state-ofthe-art results on the last three years of the **WMT Metrics shared task** and the **WebNLG Competition dataset**. In contrast to a vanilla BERT-based approach, it yields superior results even when the **training data is scarce and out-of-distribution.**

Pre-train on synthetic data as a “warm up” or “priming” before the training data after the MLM pre-training. 

#### Creating the synthetic data

Take Wiki sentences $z$ and manipulate it to $\tilde{z}$. How are these manipulation done? Via 3 different ways:

1. Mask filling with BERT: drop out a few words and fill them with BERT.
2. Back-translation with a NMT: $z_{en}\rightarrow z_{fr}\rightarrow z_{en}$
3. Dropout words

#### Training a on the synthetic data

 Ask BERT to predict all the scores below. The loss would be a comparison between the score that BERT gave and a score given by some specialized model or metric. The entire game is to find the correct tasks that if BERT learns them it will learn something useful for the metric learning cause.

![image-20210630150116646](BLEURT Learning Robust Metrics for Text Generation (Sellam 2020).assets/image-20210630150116646.png)

#### Fine-tuning on the true supervised datasets

The last step is to train on the WMT dataset that was created by human annotators.

#### Results

BLEURT was shown to correlate very good with the human annotators but its true strength is in their generalization abilities which will allow them to train on different distributions of data and still be a reasonable metric. 