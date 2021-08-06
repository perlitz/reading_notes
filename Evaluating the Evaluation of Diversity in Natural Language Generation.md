# [Evaluating the Evaluation of Diversity in Natural Language Generation](https://arxiv.org/pdf/2004.02990.pdf)

Propose a framework for evaluating diversity metrics. The framework measures the correlation between a proposed diversity metric and a diversity parameter, a single parameter that controls some aspect of diversity in generated text. 

The diversity parameter can be the generation temperature or might be a binary variable used to instruct crowdsourcing workers to generate text with either low or high content diversity. 

We demonstrate the utility of our framework by: 

1. establishing best practices for eliciting diversity judgments from humans, 
2. showing that humans substantially outperform automatic metrics in estimating content diversity, 
3. demonstrating that existing methods for controlling diversity by tuning a “decoding parameter” mostly affect form but not meaning. 

Found the n-gram based metrics to correlate best with the temperature and is even better than humans,  hinting that temperature mostly controls superficial changes to the generated text.

Showed that n-gram metrics does not separate semantic diversity (not surprising…)

Showed that top-p / top-k sweeps does not correlate as well with the n-gram metrics, meaning that they are not a good at creating diversity as the temperature (also clear why - since they cannot go, as temperature can, to above 1, which means that they cannot create more diversity than the baseline, only reduce it)