# [Mention Flags (MF): Constraining Transformer-based Text Generators (Wang 21)](https://aclanthology.org/2021.acl-long.9.pdf)

Generally, decoding algorithms for text generation can be made to produce certain parts of the input in the output via:

1. Copy mechanisms, that can be trained to copy parts of the inputs but cannot guarantee constraint satisfaction.
2. Constraint decoding algorithms that are computationally expensive and can lower generated text quality.

The paper proposes to add mention flags which inputs to the generator, wether the input words had been produced yet:

![image-20210802110303789](Mention Flags (MF) Constraining Transformer-based Text Generators (Wang 21).assets/image-20210802110303789.png)

Each input $x_i$ Gets an additional mention flag corresponding to the following:

![image-20210802104733892](Mention Flags (MF) Constraining Transformer-based Text Generators (Wang 21).assets/image-20210802104733892-7890455.png)

In the above example, circles correspond to a MF of 1 (no circle is 0), when the circle is orange, it is two.

We not that Varied types of mention flags can be given to fit the task.

In training, all mention flags has to be set to complete before an <EOS> token can be outputted. 

![image-20210802105549735](Mention Flags (MF) Constraining Transformer-based Text Generators (Wang 21).assets/image-20210802105549735-7890951.png)

The MF are inputted to the in parallel to the masked self-attention and transformer encoder input.

Results seem very impressive as this method improves upon the baselines in both precision and quality.