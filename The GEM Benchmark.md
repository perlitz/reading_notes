# [The GEM Benchmark (Gehrmann 21)](https://arxiv.org/pdf/2102.01672.pdf)

## Diversity

As argued by [Hashimoto et al. (2019)](https://aclanthology.org/N19-1169.pdf) among many others, **NLG models intrinsically trade off diversity and quality**. A model can produce more diverse outputs through sampling but at the cost of output quality. 

To account for this aspect, GEM computes multiple diversity metrics, starting with those proposed for the analysis of the results of the E2E NLG challenge (Dusek et al., 2020) and by van Miltenburg et al. (2018). Including: 

1. Shannon Entropy (Shannon and Weaver, 1963) over unigrams and bigrams (H1, H2)
2. Mean segmented type token ratio over segment lengths of 100 (MSTTR, Johnson, 1944)
3. Ratio of distinct n-grams over the total number of n-grams (Distinct1,2)
4. Count of n-grams that only appear once across the entire test output (Unique1,2 from [A Diversity-Promoting Objective Function for Neural Conversation Models (Li et al., 2016)](https://aclanthology.org/N16-1014.pdf)).