# Memory Model

## Concept

Memory model is known as the Neural Turing Machine, which enables the neural networks to read from/write to the Memory Bank.

## Read/Write

1. Read: 基于 $t$ 时刻的权重向量 $\textbf{w}_t$, 对 Memory Bank 各行数据 $\textbf{M}_t^{(i)}$ 进行加权求和, 得到读取的数据.
2. Write: 基于 $t$ 时刻的权重向量 $\textbf{w}_t$, 删去向量 $\textbf{e}_t$ 和 增加向量 $\textbf{a}_t$, 对 Memory Bank 进行写入操作.

## Weight Vector

1. Content-based Addressing: 基于当前输入 $\textbf{k}_t$, Memory Bank $\textbf{M}_t$ 和 key strength $\beta_t$, 通过计算相似度得到权重向量 $\textbf{w}_t^c$.
2. Gated Interpolation: 基于当前输入 $\textbf{w}_t^c$, 上一时刻权重向量 $\textbf{w}_{t-1}$ 和 interpolation gate $g_t$, 通过插值得到权重向量 $\textbf{w}_t^g$.
3. Location-based Addressing: 基于当前输入 $\textbf{w}_t^g$, Memory Bank $\textbf{M}_t$ 和 shift weight $\textbf{s}_t$, 通过卷积操作得到权重向量 $\textbf{w}_t^l$.
4. Sharpening: 基于当前输入 $\textbf{w}_t^l$, Memory Bank $\textbf{M}_t$ 和 sharpening factor $\gamma_t$, 通过归一化得到最终的权重向量 $\textbf{w}_t$.
