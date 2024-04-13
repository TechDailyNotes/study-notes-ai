# Positional Encoding

## Some Ideas

1. Even time-steps in the [0, 1] range
   1. Problems
      1. Time-step deltas have different meanings across different sentences, especially when the sentences have different lengths.
2. Linear numeric value encoding
   1. Problems
      1. Uncertain length of the sequence
      2. Sentence length might be too long so that the numeric value is too large to be handled by the model.
      3. Poor generalization: the model may not be able to generalize to sequences of unseen lengths.

## Extra Requirements

1. Uniqueness
   1. Positional encodings for different time-steps should be unique.
2. Consistency
   1. Distances between different time-steps should be consistent across different sentences.
3. Generalization
   1. The model should be able to generalize to sequences of unseen lengths.

## Reference Ideas

1. Binary representation of decimal numbers

## Sinusoidal Positional Encoding

\(
\overrightarrow{p_t}^{(i)} = f(t)^{(i)} := \begin{cases}
\sin(\omega_k \cdot t), & \text{if } i = 2k \\
\cos(\omega_k \cdot t), & \text{if } i = 2k+1
\end{cases} \quad \text{where } \omega_k = \frac{1}{10000^{2k/d}}
\)
