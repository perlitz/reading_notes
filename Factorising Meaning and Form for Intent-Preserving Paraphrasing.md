# [Seperator: Factorising Meaning and Form for Intent-Preserving Paraphrasing](https://www.aclanthology.org/2021.acl-long.112) [code](https://github.com/tomhosking/separator)

Separating encoding spaces to generate paraphrases.

A current trend is using some kind of bottleneck like back-translation or VAEs, this however does not constrain the expressiveness of the paraphrase.

Another trend is of syntactic control, in which an input is given along with the sentence with, for example a required syntactic tree. 

The training goes as two sentences are inputted to two separate encoders, these encodinges are then inputted to a decoder that is to create a sentence with a similar meaning as the top and a structure of the bottom.

![image-20210802172203818](Factorising Meaning and Form for Intent-Preserving Paraphrasing.assets/image-20210802172203818-7914126-7914127.png)

The meaning encoding is represented in a continuous space while the structure of the other sentence is encoded in a discreet form (with QVAEs)

The matching examples are chosen in the following process:

![image-20210802172435007](Factorising Meaning and Form for Intent-Preserving Paraphrasing.assets/image-20210802172435007-7914276.png)

As test time, there is no exemplar sentence, so the semantic and syntactic encoding of the original sentence will be used to predict a syntactic encoding.

![image-20210802175237976](Factorising Meaning and Form for Intent-Preserving Paraphrasing.assets/image-20210802175237976-7915960-7915962.png)