# [SCPN: Adversarial Example Generation with Syntactically Controlled Paraphrase Networks (Iyyer 2018)](https://arxiv.org/pdf/1804.06059.pdf)

We propose **syntactically controlled paraphrase networks (SCPNs)** and use them to generate **adversarial examples.** 

**Given a sentence and a target syntactic form (e.g., a constituency parse), SCPNs are trained to produce a paraphrase of the sentence with the desired syntax.**

We show it is possible to create training data for this task by first doing backtranslation at a very large scale, and then using a parser to label the syntactic transformations that naturally occur during this process. Such data allows us to train a neural encoderdecoder model with extra inputs to specify the target syntax. 

A combination of automated and human evaluations show that SCPNs generate paraphrases that follow their target specifications without decreasing paraphrase quality when compared to baseline (uncontrolled) paraphrase systems. Furthermore, they are more capable of generating syntactically adversarial examples that both (1) “fool” pretrained models and (2) improve the robustness of these models to syntactic variation when used to augment their training data.