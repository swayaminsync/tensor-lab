## Tips
- Avoid intemediate tensor materializations as much as possible
- Use the fused operations provided by torch

### softmax
- Softmax is shift invariant: $\text{softmax}(x) = \text{softmax}(x + c\mathbf{1})$ for any scalar constant $c$.
- We use $c$ as the max value of input to avoid the exponent exploding
