# The Low-Level Feature Blur Hazard

The low-level feature blur hazard occurs because standard ViTs partition images into rigid $16\times16$ patches at the very beginning of the network. This rough segmentation can discard microscopic features, such as fine text characters or delicate textures. Prepending a convolutional stem (a stack of shallow, small-kernel, strided convolutions) captures low-level spatial gradients and edge details, improving optimization stability and overall accuracy.

## Architectural Diagram

```mermaid
graph LR
    A[Input Image] --> B[Convolutional Stem Layer]
    B --> C[Shallow CNN Gradients]
    C --> D[Patch Projection]
    D --> E[Transformer Encoder]
```

---
[← Back to README](../README.md)
