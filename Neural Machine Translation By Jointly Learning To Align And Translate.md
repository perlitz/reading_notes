# [Neural Machine Translation By Jointly Learning To Align And Translate](https://arxiv.org/pdf/1409.0473.pdf)

## Intro

This paper was the first to introduce attention as an NLP method for translation.

It expands upon the Encoder-Decoder structure of MNT but surpasses the problem of the fixed length hidden state vector by incorporating the representations of different parts of the sequence via attention

They achieve a translation performance comparable to the existing state-of-the-art phrase-based system.

It seem like this alignment mechanism qualitatively works.

## Methods

The paper describes the encoder-decoder architecture for NMT using RNNs. They add the use of bidictional  connections in the RNN to allow context to flow in both directions.

The align mechanism works as follows: each time the proposed model generates a word in a translation, it (soft-)searches for a set of positions in a source sentence where the most relevant information is concentrated. The model then predicts a target word based on the context vectors associated with these source positions and all the previous generated target words.

The model contains an extra an extra NN with the goal of generating the attention weights using some energy calculation and a softmax over it, how much should other words representations be considered in the current word representation. 

Unlike in traditional machine translation the alignment is not considered to be a latent variable. Instead, the alignment model directly computes a soft alignment, which allows the gradient of the cost function to be back-propagated through. This gradient can be used to train the alignment model as well as the whole translation model jointly.

Once a model is trained, we use a beam search to find a translation that approximately maximizes the conditional probability

## Results

Authors show that their model deals with longer sequences much better.

In a qualitative view, the attention weights are presented showing that the network indeed learned to align correctly.