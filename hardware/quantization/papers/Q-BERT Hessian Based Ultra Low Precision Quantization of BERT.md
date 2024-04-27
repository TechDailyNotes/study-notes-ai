# Paper

## Target

Quantize the model to ultra-low bits

## Methods

1. Hessian-based mixed-precision method
   1. Challenge 1: Mix-precision quantization has a exponentially large search space
      1. Solution: Second-order sensitivity-based method
   2. Challenge 2: Embedding layers are more sensitive to quantization than encoder lagers, and different encoder layers have different sensitivities
      1. Solution
         1. Hessian-based mixed-precision quantization
            1. Compute the sensitivity of each layer to quantization using the Hessian matrix
            2. Assign more bits to more sensitive layers
2. Group-wise quantization scheme
   1. Challenge 1: Directly quantizing all the weights of the model leads to a large performance drop because the model has more than 2M params and more than 3072 neurons, and parameters in each layer has its own quantization range
      1. Solution: Group-wise quantization
      2. Specification
         1. Treat the individual matrix W with respect to each head in one dense matrix of MHSA as a group so there will be 12 groups
         2. Bucket sequential output neurons as sub-groups, e.g.,each 6 output neurons as one sub-group so there are 12 × 64 = 128 sub-groups

## Results

1. quantization to as low as 2 bits while limiting performance degradation to a maximum of 2.3%
2. Tested tasks: Sentiment Classification, Natural Language Inference, Named Entity Recognition, and Machine Reading Comprehension
3. Baseline: Direct quantization without mix-precision and group-wise quantization

## Limitations

1. a larger performance drop when quantizing models trained on SQuAD, suggesting that these models had not adequately converged
