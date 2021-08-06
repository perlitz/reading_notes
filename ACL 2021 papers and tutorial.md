# ACL 2021 papers and tutorial

## Papers

### Not in ACL

[Plug and Play Language Models: A Simple Approach to Controlled Text Generation (Dathathri 19)](https://arxiv.org/pdf/1912.02164) [blog](https://eng.uber.com/pplm/)

> Performing conditional text generation using an unconditional LM (like GPT2) and an attribute model. Sampling entails a forward and backward pass in which gradients from the attribute model push the LM's hidden activations and thus guide the generation. #LM

[Measuring the Intrinsic Dimension of Objective Landscapes (Li 18)](https://arxiv.org/pdf/1804.08838) 

> Investigate the Intrinsic Dimension (ID) by training networks with increasing number of their parameters unfrozen. The number of parameters in which the network seems to solve the problem is the ID of the objective landscape.

[iBLEU: Joint Learning of a Dual SMT System for Paraphrase Generation (Sun 12)](https://aclanthology.org/P12-2008.pdf)

> A metric combining diversity and correctness: $iBLEU(s, r_s, c) = αBLEU(c, r_s) − (1 − α)BLEU(c, s)$​​​) with $s, r_s$ and $c$ are the source, other reference paraphrases and paraphrase respectively.    

[SARI: Optimizing Statistical Machine Translation for Text Simplification (Xu 16)](https://watermark.silverchair.com/tacl_a_00107.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAAs0wggLJBgkqhkiG9w0BBwagggK6MIICtgIBADCCAq8GCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQMvYHnDIYsaw7ZVJ74AgEQgIICgJXJ4m441bVmKSro2qzOVtnpP-wAoWVCg-6qH9jzB94uvzOsYRCxXv_GxokbfikFvDQIMUnhrdcmYnpFVjlg4Rh3fXlTzq-zIEqnR1WOqxuq9OUm2X4TS7PCCaAGL0NZu2ZfFJrivVnTZW0sjkjKOoFhtAOXdyJi7Ash4HDoIfCT_3EttfJXgxvHKcMlG5CLqRfqgy7BmJklLRp_1zv0PV67q4SpKh1jwb8MQgjJCIOAtKMYKlpBPc3X2j8diMFsPL1mmpWCch9kiXseOqYcFU1BKoITG5U1jW_Dd_pqoqoa_7wBMqSzCSwkM_7x7gfDdpvjauPGuLdq1GklQGXq9JLaUEQUVNovdbXfUufFGOP0sokS6DwJO8Aa-tppLSMcD73mK_f6h6i-6AuC-HByxU3xeuR7p0JY2i1Zmexgw3wAePjRPRV3W5pI1kjJ8I0uxPy-IW778r3k8XfmTuGaFO74mqH_EQz5sMPDw3RvW4derIax8Xvqp9W-k7YBqXnb6QRi8rGhfUl6Qf93msTRJiFfQ_o0tuMy7t4HOEY1TPn5cnDq91plFf_z4GDd9OwPs2JxKHt7JaRe61_-EI7feqnWOJNrvMP84pYix_43XRFA_M0wPWONRFjohraVCwjK_ei9l6gqY-GbOicTmSnSWgmXqZjqFM0AEUMFdzzTJwedZv30NaUuICI_Sjra3N_qqnAZbQhy6Yggwu9wjeQkwc78VT04mCRUJEku5RUYBl2Zl0fjlW8co1iB8xVmHnQnzlIlh3CbZkM_rkOFLo4fw4iOo5IHNDPOfvfNjXvyo6ODRrJoi_QIROMkR5ZpzfdXOoMTJwM-cd9gtBjtLGnUGc8)

> 

[Diverse Beam Search: Decoding Diverse Solutions from Neural Sequence Models (Vijayakumar 16)](https://arxiv.org/pdf/1610.02424)

> Not yet

[Dataset Cartography: Mapping and Diagnosing Datasets with Training Dynamics](https://arxiv.org/pdf/2009.10795.pdf)

> Not yet

### To watch

[Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning (Aghajanyan 21)](Intrinsic Dimensionality Explains the Effectiveness of Language Model Fine-Tuning (Aghajanyan 21).md)

> Not yet




[Vocabulary Learning via Optimal Transport for Neural Machine Translation](Vocabulary Learning via Optimal Transport for Neural Machine Translation.md)

> Not yet

### Watched

[Pushing Paraphrase Away from Original Sentence: A Multi-Round Paraphrase Generation Approach (Lin 21)](Pushing_Paraphrase_Away_from_Original_Sentence_A_Multi-Round Paraphrase_Generation_Approach.md)

> Propose to sequentially paraphrase sentences in order to increase diversity while keeping semantics using back-translation.

[Reflective Decoding: Beyond Unidirectional Generation with Off-the-Shelf Language Models (West 21)](Reflective Decoding Beyond Unidirectional Generation with Off-the-Shelf Language Models.md)

> Propose to perform #PG using an LTR #LM to generate context from the source sentence and then an RTL language model to get a paraphrase from the context (the same for the different direction), nice results.


[Better than Average: Paired Evaluation of NLP systems (Peyrarad 21)](https://aclanthology.org/2021.acl-long.179.pdf)

> Argue that the mean and median should not qualify as a quantity with which model comparison is compared, suggest to use the Bradley–Terry (BT) model  instead that also takes the correlations between compared models into account by using pair-wise comparisons. #metrics #evaluation

[Implicit Representations of Meaning in Neural Language Models (Li 21)](https://aclanthology.org/2021.acl-long.143.pdf)

> Show contextual word representations in #LM that function as *models of entities and situations* as they evolve throughout a discourse, these representations have functional similarities to linguistic models: they support a linear readout of each entity’s current properties and relations, and can be manipulated with predictable effects on language generation. 

[Scientific Credibility of Machine Translation Research: A Meta-Evaluation of 769 Papers (Marie 21)](https://aclanthology.org/2021.acl-long.566.pdf)

> #MT evaluations are flawed, this paper presents a set of guidelines to improve them.

[UnNatural Language Inference (Sinha 21)](UnNatural Language Inference (Sinha 21).md)

> SOTA LM are less insensitive to grammar and word order than expected as they are able to perform NLI task as good accuracy even beyond sentence permutation (==Not sure I agree with this paper, need to go over it with someone else==)

[Keep the Primary, Rewrite the Secondary: A Two-Stage Approach for Paraphrase Generation (Su 21)](Keep the Primary, Rewrite the Secondary A Two-Stage Approach for Paraphrase Generation (Su 21).md)

> Utilize a splitting mechanism ($PSI$​) to split the source in to primary and secondary words according to their importance. Using the split, two sentences are formed each with the primary/secondary [masked]. These two sentences are fed in to a different encoder, then aggregated and decoded. #PG

[Seperator: Factorising Meaning and Form for Intent-Preserving Paraphrasing](Factorising Meaning and Form for Intent-Preserving Paraphrasing)

> Proposes a #PG mechanism in which the encoding of an original sentence is separated in to *semantic* and *syntactic* encodings. This is done by training with two input sentences, one that conveys the meaning of the target and one that conveys the surface form (structure). Each sentence is inputted to a different encoder that learns to embed different dimensions from the input.

[ProtAugment: Intent Detection Meta-Learning through Unsupervised Diverse Paraphrasing (Dotierre 21)](ProtAugment Intent Detection Meta-Learning through Unsupervised Diverse Paraphrasing)

> Propose ProtAugment, a meta-learning algorithm for short texts classification (the intent detection task). This an extension of Prototypical Networks, that limits overfitting on the bias introduced by the few-shots classification objective at each episode. **Relies on diverse paraphrasing: a conditional language model is first fine-tuned for paraphrasing, and diversity is later introduced at the decoding stage at each meta-learning episode.**  #PG

[On Training Instance Selection for Few-Shot Neural Text Generation (Chang 21)](On Training Instance Selection for Few-Shot Neural Text Generation.md)

> Investigating Training Instance Selection for Few-Shot Neural Text Generation, show that sampling at random is suboptimal and can be improved upon with simple clustering over some embedding space.

[Mention Flags (MF): Constraining Transformer-based Text Generators (Wang 21)](Mention Flags (MF) Constraining Transformer-based Text Generators (Wang 21).md)

> Proposes the use of MF, for **trainable constrained generation**, the input tokens to the decoder has a flag concatenated to them that marks whether they are constrained and of so if they already appeared. Nice results. #PG

[Mind Your Outliers! Investigating the Negative Impact of Outliers on Active Learning for Visual Question Answering](Mind Your Outliers! Investigating the Negative Impact of Outliers on Active Learning for Visual Question Answering.md) 

> Using a dataset map that collectively decides which are the hardest samples, then removing these samples from the dataset, and by which fixes an inherent problem with AL which chooses these (very hard) samples substantially more. #VQA #AL

[Including Signed Languages in Natural Language Processing](https://www.aclanthology.org/2021.acl-long.570) [video](https://underline.io/events/167/sessions/6092/lecture/25681-including-signed-languages-in-natural-language-processing)

> A summary of the state of research of sign-language

