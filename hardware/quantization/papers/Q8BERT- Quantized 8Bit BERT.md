# Paper

## Overview

Explores the implementation of quantization-aware training during the fine-tuning phase of BERT to significantly reduce the model size and computational requirements while retaining high accuracy. This approach compresses BERT by 4x, making it more feasible for deployment in environments with limited resources such as mobile devices or embedded systems.

## Structure

1. Method
   1. Integration of quantization directly into the training process, which helps to minimize accuracy loss.
   2. Apply symmetric linear quantization to both the weights and activations of the BERT model during fine-tuning.
2. Result
   1. Test the quantized BERT model on the GLUE benchmark and the SQuAD dataset.
   2. Maintain 99% of the model's original accuracy across multiple NLP tasks.
3. Implementation
   1. Quantize all the Embedding and FC layers to Int8.
   2. Keep Softmax layers, Layer Normalization layers, and GELU layers in FP32.
4. Evaluation
   1. Dataset
      1. GLUE benchmark (General Language Understanding Evaluation) - for the development of general and robust natural language understanding systems.
      2. SQuAD dataset (Stanford Question Answering Dataset) - a reading comprehension dataset.
5. Limitation
