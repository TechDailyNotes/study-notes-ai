# Quantization

## Basic Concepts

1. Terms Scale: The ratio of the floating point range to the quantized range.
2. Zero-Point Mean: The representation of the floating point 0.0 in the quantized range.

## Types of Quantization

### Symmetry

1. Symmetric Quantization: The zero-point mean is 0.0 in the quantized range.
2. Asymmetric/Affine Quantization: The zero-point mean is not 0.0 in the quantized range.

### DQ vs QAT vs PTQ

1. DQ (Dynamic Quantization)
   1. Quantize model weights after training.
   2. Quantize model activations during inference.
2. QAT (Quantization Aware Training)
   1. Quantize model weights and activations during training.
   2. Minimize accuracy loss.
3. PTQ (Post Training Quantization)
   1. Quantize model weights and activations after training.
   2. Don't require retraining.

## Related Other Concepts

1. Clamp function: A function that restricts the input value to a specific bound.
2. EMA (Exponential Moving Average): A method to smooth out data over time.
