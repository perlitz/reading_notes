# [On Training Instance Selection for Few-Shot Neural Text Generation](https://aclanthology.org/2021.acl-short.2.pdf)

How to select the samples for few-shot learning.

First the authors use K-MEANS (in some embedding space) to cluster the samples, they then train the same model on different selection strategies from the clusters. They show that choosing the samples that are closest to the cluster centers is superior to randomly sampling and to sampling from the farther points or all from single cluster.

