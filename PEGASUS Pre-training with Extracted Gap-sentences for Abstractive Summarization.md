# [PEGASUS: Pre-training with Extracted Gap-sentences for Abstractive Summarization](https://arxiv.org/pdf/1912.08777)

## Method 

### Choosing sentence masking location by importance for GSG

Choosing important sentences and blocking them out, this way this task is already somehow like a summarization task. Important sentences are chosen either *Random*, *LEAD*:according to location (first sentences are chosen more frequently since they are more important) or according to *Principal* (the ROUGE1-F1 between the sentence and the rest of the document).

Generally, 30% of sentences were chosen as gaps for generation. 

![image-20210627110449736](/Users/yotamp/Documents/Language models.assets/image-20210627110449736-4781091.png) 

### Pre-Training data

Trained on C4 and HugeNews

### Downstream tasks and fine-tuning

XSum, CNN/DailyMail and more...

## Architecture

$PEGASUS_{BASE}$ had L=12, H=768, F=3072, A=12 and $PEGASUS_{LARGE}$ had L=16, H=1024, F=4096, A=16, where L denotes the number of layers for encoder and decoder (i.e. Transformer blocks), H for the hidden size, F for the feed-forward layer size and A for the number of self-attention heads.

**Only 5% of the number of parameters of T5**

## Training scheme

$PEGASUS_{BASE}$ Was trained with a batch size of 256 while $PEGASUS_{LARGE}$ with a batch size of 8192. Used **sinusoidal positional encoding** following Vaswani et al. (2017). For optimization, both pre-training and fine-tuning used **Adafactor** (Shazeer & Stern, 2018) with **square root learning rate decay and dropout rate of 0.1.**

With more pre-training steps, the model observed more documents in the pre-training corpus. A $PEGASUS_{BASE}$ model trained for 500k (highest we tried) steps did not observe all training examples on C4 nor HugeNews

### Inference Sampling

We used greedy-decoding for studies in Section 6.1, and used beam-search with a length-penalty, α, as in Wu et al. (2016) for the final large model.

## Experiments

### Fine-tune dataset vs fine-tuned downstream task

Showed that pre-training on HugeNews was more effective than C4 on the two news downstream datasets, while the non-news informal datasets (WikiHow and Reddit TIFU) prefer the pre-training on C4. This suggests **pre-training models transfer more effectively to downstream tasks when their domains are aligned better.**

### Sentence importance for GSG

Showed that *LEAD* worked great for news but worse than others on other datasets, concluded that choosing principal sentences works best for downstream summarization tasks and choose a Principal method. Used an importance sampling method.

To encourage the model to copy, which is an important aspect of the more extractive datasets, we left 20% of selected sentences unchanged in the input instead of replacing with [MASK1]. We increased the GSR to 45% to achieve a similar number of “gaps” as the optimal 30% found above.

### Zero and Few Shot learning

They showed that in 8 out of 12 datasets, with just 100 examples $PEGASUS_{LARGE}$ could be fine-tuned to generate summaries at comparable quality to TransformerBASE trained on the full supervised datasets ranging from 20k to 200k examples. $PEGASUS_{LARGE}$ also beat previous state-of-the-art results on 6 out of 12 datasets with only 1000 fine-tuning examples.



- Only 5% of the number of parameters of T5
- Pre-trained our model on a very large corpus of web-crawled documents, then we fine-tuned the model on 12 public down-stream abstractive summarization datasets, 
- With only 1000 fine-tuning examples, we were able to perform better in most tasks than a strong baseline (Transformer encoder-decoder) that used the full supervised data, which in some cases had many orders of magnitude more examples. This “sample efficiency” greatly increases the usefulness of text summarization models as it significantly lowers the scale and cost of supervised data collection, which in the case of summarization is very expensive.
- Deterministically choose sentences based on importance, rather than randomly. 
- As in T5, PEGASUS does not reconstruct full input sequences, and only generates the masked sentences as a single output sequence. 

![image-20210624193456242](/Users/yotamp/Documents/Language models.assets/image-20210624193456242.png)

