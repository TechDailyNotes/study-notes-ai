# Paper

## Overview

1. Apply a knowledge **distillation** method to transfer the knowledge from a large teacher model (BERT) to a small student model (TinyBERT).

## Structure

1. Method
2. Result
   1. TinyBERT can achieve over 96.8% of its teacher model's performance on GLUE benchmark tasks while being 7.5 times smaller and 9.4 times faster in inference.
3. Limitation
   1. Potential for performance degradation in extremely resource-constrained environments and scenarios requiring very high accuracy.
   2. Complexities involved in distilling models for specific tasks without losing general applicability might limit its use in certain applications.
