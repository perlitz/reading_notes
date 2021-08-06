# NLG Tasks

##  Question answering

The problem of QA is usually splitter in to 2 parts:

1. Find documents that (might) contain an answer, this is usually handled by traditional information retrieval/web search
2. Finding an answer in a paragraph or a document (reading comprehension)

### Reading comprehension by QA

Buegas 2013 defined machine comprehension using a question answering framework. They collected the MCTest that contained kids stories, questions and answers.

In the 2015 with the production of large datasets which permits supervised rural systems to be built, namely:

1. Hermann et al. (NIPS 2015) CNN/DM dataset
2. Rajpurkar et al.(EMNLP 2016) SQuAD
3. MS MARCO, TriviaQA, RACE, NewsQA, NarrativeQA...

The most widely used dataset is **SQuAD**

####  SQuAD

**S**tanford **Qu**estion **A**nswering **D**ataset (SQuAD) is a reading comprehension dataset, consisting of questions posed by crowdworkers on a set of Wikipedia articles, where the answer to every question is a segment of text, or *span*, from the corresponding reading passage, or the question might be unanswerable.

- **SQuAD V1.1,** the previous version of the SQuAD dataset, contains 100,000+ question-answer pairs on 500+ articles.
- **SQuAD V2.0** combines the 100,000 questions in SQuAD1.1 with over 50,000 unanswerable questions written adversarially by crowdworkers to look similar to answerable ones. To do well on SQuAD2.0, systems must not only answer questions when possible, but also determine when no answer is supported by the paragraph and abstain from answering.

Some limitations of SQuAD are that:

1. There are only span based answers (no yes/no, counting, implicit why)
2. Questions were constructed looking at passages, this means  that no genuine information needed, it more similar to resolved references.

#### The Stanford Attentive Reader (DrQA)

1. Look up a word embedding for each word in the Q, feed the Q in to a Bi-LSTM, concat the output to one 2d vector. 
2. Look up a word embedding for each word in the passage feed it in to a Bi-LSTM.
3. Find the answer in the passage by using bilinear attention (with a learned $W$ weight matrix). There are two types of $W$ matrices, one for the start and one for the end word. 

####  BiDAF - main innovation: Attention Flow layer

Main Idea: attention should flow both ways - from the context to the question and from the question to the context. They created a similarity score between every word in the Q and in the passage. These similarity scores were used to create an attention weighted Q and Passage. Both attention weighted and original LSTM outputs are fed to another 2 BiLSTM layers that produces the start and end words.

#### FusionNet - a different type of attention

Saved computation by varying a bilinear form of attention to a different product of two lower rank matrices with two RELUs.

## Text style transfer

A List of papers can be found [here](https://github.com/fuzhenxin/Style-Transfer-in-Text)

### [Deep Learning for Text Style Transfer: A Survey (Jin 2020)](https://arxiv.org/pdf/2011.00416.pdf)

Text style transfer (TST) is an important task in natural language generation (NLG), which **aims to control certain attributes in the generated text, such as politeness, emotion, humor, and many others.** 

In this paper, we present a systematic survey of the research on neural text style transfer, spanning over 100 representative articles since the first neural text style transfer work in 2017. We discuss the task formulation, existing datasets and subtasks, evaluation, as well as the rich methodologies in the presence of parallel and non-parallel data. We also provide discussions on a variety of important topics regarding the future development of TST.1

### [A Probabilistic Formulation of Unsupervised Text Style Transfer (Junxian 2020)](https://arxiv.org/abs/2002.03912)

We present a **deep generative model for unsupervised text style transfer that unifies previously proposed non-generative techniques**. 

Our probabilistic approach models non-parallel data from two domains as a partially observed parallel corpus. By hypothesizing a parallel latent sequence that generates each observed sequence, our model learns to transform sequences from one domain to another in a **completely unsupervised fashion**. In contrast with traditional generative sequence models (e.g. the HMM), our model makes few assumptions about the data it generates: it uses a recurrent language model as a prior and an encoder-decoder as a transduction distribution. 

While computation of marginal data likelihood is intractable in this model class, we show that amortized variational inference admits a practical surrogate. Further, by drawing connections between our variational objective and other recent unsupervised style transfer and machine translation techniques, we show how our probabilistic view can unify some known non-generative objectives such as backtranslation and adversarial loss. 

Finally, we demonstrate the effectiveness of our method on a wide range of unsupervised style transfer tasks, including **sentiment transfer, formality transfer, word decipherment, author imitation, and related language translation**. Across all style transfer tasks, our approach yields substantial gains over state-of-the-art non-generative baselines, including the state-of-the-art unsupervised machine translation techniques that our approach generalizes. Further, we conduct experiments on a standard unsupervised machine translation task and find that our unified approach matches the current state-of-the-art.



















