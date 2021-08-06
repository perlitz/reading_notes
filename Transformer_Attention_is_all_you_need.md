# [Transformer: Attention is all you need](https://arxiv.org/abs/1706.0376) [note]()

## Intro

A paper describing a new way to do sequence to sequence modeling where instead of using an LSTM+attention mechanism to get the context, only attention is used.

They propose a new simple network architecture, the Transformer, based solely on attention mechanisms, dispensing with recurrence and convolutions entirely. 

Other than just getting better results, another benefit of the Transformer is the ability to parallelize computation greatly.

Transformer is the first transduction model relying entirely on self-attention to compute representations of its input and output without using sequence aligned RNNs or convolution.  

## Methods

## Encoder 

The encoder is composed of a stack of N = 6 identical layers. Each layer has two sub-layers. 

- The first is a multi-head self-attention mechanism
- The second is a simple, positionwise fully connected feed-forward network.

The two layers employ residual connections and layer normalization which normalizes the activation across the features. This is different from BN which normalizes across the batch. "In layer normalization, the statistics are computed across each feature and are independent of other examples."

### Decoder 

The decoder is also composed of a stack of N = 6 identical layers, In addition to the two sub-layers in each encoder layer, the decoder inserts a third sub-layer, which performs multi-head attention over the output of the encoder stack.

The self-attention sub-layer in the decoder stack is modified to prevent positions from attending to subsequent positions.

This masking, combined with fact that the output embeddings are offset by one position, ensures that the **predictions for position i can depend only on the known outputs at positions less than i** (causality).

### Attention

Attention used here is called Scaled Dot-Product Attention, as the name implies, it weights each value with the exponent of the dot product of the corresponding key and value, in case the key and value are the same, the values similarity to the quary is weighting it as intuitive in attention, the metric in which they are close is set by the function Q, V and  K which produces the quary key and value for the real values.

### Multi-head attention

Instead of performing a single attention function with model-dimensional keys, values and queries, we found it beneficial to linearly project the queries, keys and values h times with different, learned linear projections to dk, dk and dv dimensions, respectively. After the multiple attention operations, the results are concatenated.

The multi-head attention is used in three parts:

- encoder-decoder attention, allows every position in the decoder to attend over all positions in the input sequence. This is similar to the common attention introduced by bengio.
- Self attention in the encoder.
- (Causal) Self attention on the decoder

#### Embeddings

Use learned embeddings to convert the input tokens and output tokens to vectors of dimension d_model.

### Positional Encoding

Since the model contains no recurrence and no convolution, in order for the model to make use of the order of the sequence, one must inject some information about the relative or absolute position of the tokens in the sequence.

- To achieve this positional embedding is added to the input.

Self attention is shown to be beneficial from the stand points of complexity, number of sequential operations. it is also said to be more interpretable.

## Results

A new state-of-the-art BLEU score of 28.4 (Training took 3.5 days on 8 P100 GPUs) on the WMT 2014 English-to-German translation test.