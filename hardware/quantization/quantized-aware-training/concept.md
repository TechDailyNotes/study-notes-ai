# QAT (Quantized Aware Training)

## Fake Quantization

1. Purpose: Simulate the effects of quantization during training without actually reducing the precision of the computation.

## Features

1. Insertion of fake quantization nodes: Fake quantization nodes are inserted in the model to simulate the rounding and clipping effects of quantization of weights and activations.
2. Forward Pass Simulation: Weights and activations are quantized and de-quantized to simulate the effects of quantization during the forward pass without actually reducing the precision of the underlying computation.
3. Back-propagation Adjustment: During the back-propagation, gradients are computed considering the quantization effects.
4. No Actual Quantization: During the fake quantization, the underlying storage data and the precision of computation remain unchanged.

## Straight Through Estimator (STE)

1. Applications: Applied in non-differentiable functions to approximate the gradient.
2. Outputs: Always set the gradient to 1.
