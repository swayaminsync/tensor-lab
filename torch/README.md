## Tips
- Avoid intemediate tensor materializations as much as possible
- Use the fused operations provided by torch

### softmax
- Softmax is shift invariant: $\text{softmax}(x) = \text{softmax}(x + c\mathbf{1})$ for any scalar constant $c$.
- We use $c$ as the max value of input to avoid the exponent exploding

### Dropout
- Samples from the bernoulli distribution i.e. $P(keep) = P(u < 1-p) = 1- p$ hence the probability passed here as $p$ will be the dropping probability
