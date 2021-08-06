# [Keep the Primary, Rewrite the Secondary: A Two-Stage Approach for Paraphrase Generation (Su 21)](https://aclanthology.org/2021.findings-acl.50.pdf)

Propose a new Identification-thenAggregation (IA) framework to tackle this paraphrase generation. In the identification step, the input tokens are sorted into two groups by a novel Primary/Secondary Identification (PSI) algorithm, in train time the split is done via $PSI(\bold{X},\bold{Y})$​, however, in test time there is no access to $\bold{Y}$​ so the split is either done with  $PSI(\bold{X},\bold{X})$ Or using an LSTM that trained to imitate the $PSI$ Function on the train set​. 

In the aggregation step, these groups are separately encoded, before being aggregated by a custom designed decoder, which autoregressively generates the paraphrased sentence. 

In extensive experiments on two benchmark datasets, we demonstrate that our model outperforms previous studies by a notable margin. We also show that the proposed approach can generate paraphrases in an interpretable and controllable way.

