# Perceiver

## Problems to Solve

1. Hard to Generalize: Domain-specific models are not generalizable because they make architectural assumptions about the data.
2. Quadratic Bottleneck: Transformer architecture is computationally expensive and not scalable to large datasets because the attention mechanism has a quadratic complexity.

## Challenges for Multi-Modal Data

1. Heterogeneous Data: Different data types (e.g., images, text, audio) require different models and modalities.
2. Time Complexity: Quadratic complexity of the attention mechanism in the Transformer architecture limits its scalability to large datasets.

## Key Ideas

1. Keep refining queries and representations for keys and values iteratively.
