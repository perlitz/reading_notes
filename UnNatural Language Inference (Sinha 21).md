# [UnNatural Language Inference (Sinha 21)](https://aclanthology.org/2021.acl-long.569.pdf)

  What do we mean when we say LM knows syntax? One test of syntax is the order of words, changing them can alter the meaning of the sentence. If models understand syntax, the model should notice word order has changed.

Observation: state-of-the-art Natural Language Inference (NLI) models assign the same labels to permuted examples as they do to the original, i.e. they are largely invariant to random word order permutations.

Natural Language Inference (NLI) typically consists of two sentences: a premise and a hypothesis. The objective is to predict whether the premise entails the hypothesis, contradicts it, or is neutral with respect to it.

The paper:

1. Proposes a suite of metrics (Permutation Acceptance) for measuring model insensitivity to word order (look at the blue/white in the figure…)

   - $Ω_{max}$​ gives the percentage of examples for which there is at least one permutation that the model assigns the gold label (one is enough to get the accuracy.
   - $Ω_{rand}$​, or where x = 1/m or chance probability (for balanced m-way classification, where m = 3 in NLI) so in the NLI case, at least a third of the permutations should be labeled correctly (better than random guess).
   - $Ω_{1.0}$ will mark the model as non 0 only in case all permutations are correct

   ![image-20210804120440487](UnNatural Language Inference (Sinha 21).assets/image-20210804120440487.png)

   Authors define $D_f$ to be the list of examples originally marked incorrect according to $\mathcal{A}$, but are now deemed correct according $Ω_{max}$. $D_c$ is the list of examples originally marked correct according to $\mathcal{A}$. Thus, we should expect $D_f$ < $D_c$ for models that have high accuracy ==I’m not sure I agree with that… I think it is clear if this is said with $Ω_{rand}$==.

2. Construct multiple permuted test datasets for measuring NLI model performance at a large scale: Train the model on the regular dataset train set and permute the test set in a random fashion leaving $(w-1)!$ options for each sentence as long as no word keeps its original location. In case $q$ (hparam) permuted are to be taken, a total of $\binom{(w−1)!}{q} $ possibilities exist

3. Show that NLI models focus on words more than word order, but can partially reconstruct syntactic information from words alone.

4. Show the problem persists on out-of domain data, 

5. Show that humans struggle with UnNatural Language Inference, underscoring the non-human likeness of SOTA models