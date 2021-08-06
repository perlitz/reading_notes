# [Paraphrase Generation with Deep Reinforcement Learning (Li 2018)](https://www.aclweb.org/anthology/D18-1421.pdf)

In this paper, we present a **deep reinforcement learning approach to paraphrase generation.** 

Specifically, we propose a new framework for the task, which consists of a generator and an evaluator, both of which are learned from data. The generator, built as a sequence-to-sequence learning model, can produce paraphrases given a sentence. The evaluator, constructed as a deep matching model, can judge whether two sentences are paraphrases of each other. The generator is first trained by deep learning and then further fine-tuned by reinforcement learning in which the reward is given by the evaluator. 

For the learning of the evaluator, we propose two methods based on supervised learning and inverse reinforcement learning respectively, depending on the type of available training data. Experimental results on two datasets demonstrate the proposed models (the generators) can produce more accurate paraphrases and outperform the state-of-the-art methods in paraphrase generation in both automatic evaluation and human evaluation.