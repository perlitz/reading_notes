# [SGCP: Syntax-Guided Controlled Generation of Paraphrases (Kumar 2020)](https://aclanthology.org/2020.tacl-1.22.pdf)

Given a sentence (e.g., ‘‘I like mangoes’’) and a constraint (e.g., sentiment flip), the goal of controlled text generation is to produce a sentence that adapts the input sentence to meet the requirements of the constraint (e.g., ‘‘I hate mangoes’’). 

Going beyond such simple constraints, recent work has started exploring the incorporation of complex syntactic guidance as constraints in the task of controlled paraphrase generation. In these methods, syntactic-guidance is sourced from a separate exemplar sentence. However, this prior work has only utilized limited syntactic information available in the parse tree of the exemplar sentence. We address this limitation in the paper and propose **Syntax Guided Controlled Paraphraser (SGCP), an end-to-end framework for syntactic paraphrase generation**. We find that SGCP can generate syntax-conforming sentences while not compromising on relevance. We perform extensive automated and human evaluations over multiple real-world English language datasets to demonstrate the efficacy of SGCP over state-of-the-art baselines. 

