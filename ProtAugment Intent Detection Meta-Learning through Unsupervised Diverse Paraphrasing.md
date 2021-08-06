# [ProtAugment: Intent Detection Meta-Learning through Unsupervised Diverse Paraphrasing](https://aclanthology.org/2021.acl-long.191.pdf)

Recent research considers few-shot intent detection as a meta-learning problem: the model is learning to learn from a consecutive set of small tasks named episodes. 

In this work, we propose PROTAUGMENT, a meta-learning algorithm for short texts classification applied to the intent detection task. PROTAUGMENT is a novel extension of Prototypical Networks (Snell et al., 2017) that limits over-fitting on the bias introduced by the few-shots classification objective at each episode. It relies on diverse paraphrasing: a conditional language model is first fine-tuned for paraphrasing, and diversity is later introduced at the decoding stage at each meta-learning episode. The diverse paraphrasing is unsupervised as it is applied to unlabelled data and then fueled to the Prototypical Network training objective as a consistency loss. PROTAUGMENT is the stateof-the-art method for intent detection metalearning, at no extra labeling efforts and without the need to fine-tune a conditional language model on a given application domain.



