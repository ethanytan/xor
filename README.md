# Generalisation in Bitwise XOR

I trained a 1-layer MLP to predict the bitwise XOR of two numbers. Using weight decay, the model consistently learns to generalise to the whole dataset using a fraction of the data as training. When the fraction of data is chosen at a suitable level, this generalisation occurs long after the model achieves perfect accuracy on the training data. Moreover, the algorithm it learns is consistently the same, and I was able to reverse engineer it by observing the model weights.

The algorithm involves the use of the Hadamard transform, and by changing to the associated basis, it is possible to measure quantitatively how much any given model has learned real patterns, and how much it has memorised. Models without weight decay obtain increasingly large test loss as training occurs, but interestingly, these models partially learn real patterns quickly before freezing up and settling into a half-memorised, half-generalised state.

I've uploaded a LaTeX write-up of my findings, as well as the python notebook where I conducted my research.
