# Attention Model

## Attention Types

1. General Attention
   1. Equation: $\text{score}(\textbf{s}_t, \textbf{h}_i) = \textbf{s}_t^\top \textbf{W}_a \textbf{h}_i$
2. Dot Product Attention
   1. Equation: $\text{score}(\textbf{s}_t, \textbf{h}_i) = \textbf{s}_t^\top \textbf{h}_i$
3. Scaled Dot Product Attention
   1. Equation: $\text{score}(\textbf{s}_t, \textbf{h}_i) = \frac{\textbf{s}_t^\top \textbf{h}_i}{\sqrt{n}}$
4. Content-based Attention
   1. Equation: $\text{score}(\textbf{s}_t, \textbf{h}_i) = \text{cosine\_similarity}(\textbf{s}_t, \textbf{h}_i)$
5. Location-based Attention
   1. Equation: $\alpha_{t, i} = \text{softmax}(\textbf{W}_a \textbf{s}_t)$
6. Additive Attention
   1. Equation: $\text{score}(\textbf{s}_t, \textbf{h}_i) = \textbf{v}_a^\top \text{tanh}(\textbf{W}_a \left[\textbf{s}_t; \textbf{h}_i\right])$

## Attention Classifications

1. Self-Attention vs. Cross-Attention
2. Global/Soft Attention vs. Local/Hard Attention
