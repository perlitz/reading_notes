# Datasets

## Paraphrasing datasets

## Question answering

###  SQuAD

**S**tanford **Qu**estion **A**nswering **D**ataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or *span*, from the corresponding reading passage, or the question might be unanswerable.

- **SQuAD V1.1,** the previous version of the SQuAD dataset, contains 100,000+ question-answer pairs on 500+ articles.
- **SQuAD V2.0** combines the 100,000 questions in SQuAD1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering.

Some limitations of SQuAD are that:

1. There are only span based answers (no yes/no, counting, implicit why)
2. Questions were constructed looking at passages, this means  that no genuine information needed, it more similar to resolved references.

## Data-2-text datasets

### [The WebNLG Challenge: Generating Text from RDF Data](https://www.aclweb.org/anthology/W17-3518.pdf)

The WebNLG challenge consists in mapping sets of RDF triples to text. It provides a common benchmark on which to train, evaluate and compare “microplanners”, i.e. generation systems that verbalise a given content by making a range of complex interacting choices including referring expression generation, aggregation, lexicalisation, surface realisation and sentence segmentation. In this paper, we introduce the microplanning task, describe data preparation, introduce our evaluation methodology, analyse participant results and provide a brief description of the participating systems.

### [ToTTo: A Controlled Table-To-Text Generation Dataset](https://arxiv.org/pdf/2004.14373.pdf) ([code](https://github.com/google-research-datasets/totto))

An open-domain English table-to-text dataset with over 120,000 training examples that proposes a controlled generation task: given a Wikipedia table and a set of highlighted table cells, produce a one-sentence description.

## General dataset investigation 

### [Annotation Artifacts in Natural Language Inference Data (Gururagan 2018)](https://www.aclweb.org/anthology/N18-2017.pdf)

Large-scale datasets for natural language inference are created by presenting crowd workers with a sentence (premise), and asking them to generate three new sentences (hypotheses) that it entails, contradicts, or is logically neutral with respect to. **We show that, in a significant portion of such data, this protocol leaves clues that make it possible to identify the label by looking only at the hypothesis, without observing the premise.** Specifically, we show that a simple text categorization model can correctly classify the hypothesis alone in about 67% of SNLI (Bowman et al., 2015) and 53% of MultiNLI (Williams et al., 2018). Our analysis reveals that specific linguistic phenomena such as negation and vagueness are highly correlated with certain inference classes. **Our findings suggest that the success of natural language inference models to date has been overestimated, and that the task remains a hard open problem.**

Author trained a classifier on the second sentence in an NLI task (predict if the next sentence is an entailment, neutral or contradiction of the first sentence) and showed that it gets 66% accuracy where the expected performance should be 33%. When they took SOTA methods and evaluated on the hard set (the one that the above classifier could not predict), they got a huge drop in performance (88% -> 72%). This means that the methods used some annotation artifacts and did not really solve the task. 

### [Learning and Evaluating General Linguistic Intelligence (Yogatama 2019)](https://arxiv.org/pdf/1901.11373.pdf)

We define **general linguistic intelligence** as the ability to reuse previously acquired knowledge about a language’s lexicon, syntax, semantics, and pragmatic conventions to adapt to new tasks quickly. 

Using this definition, we analyze state-of-the-art natural language understanding models and conduct an extensive empirical investigation to evaluate them against these criteria through a series of experiments that assess the task-independence of the knowledge being acquired by the learning process. In addition to task performance, **we propose a new evaluation metric based on an online encoding of the test data that quantifies how quickly an existing agent (model) learns a new task.** 

Our results show that while the field has made impressive progress in terms of model architectures that generalize to many tasks, **these models still require a lot of in-domain training examples (e.g., for fine tuning, training task-specific modules), and are prone to catastrophic forgetting.** Moreover, we find that far from solving general tasks (e.g., document question answering), **our models are overfitting to the quirks of particular datasets** (e.g., SQuAD). We discuss missing components and conjecture on how to make progress toward general linguistic intelligence.

Showed that the transfer between different QA datasets is **Really** bad. 



















