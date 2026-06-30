# Contrastive Alignment (CLIP)

Contrastive Alignment, typified by OpenAI's CLIP (Contrastive Language-Image Pre-training), trains joint vision-language encoders. An image encoder (usually a ViT) and a text encoder (usually a Transformer) embed paired visual and textual descriptions into a shared latent space. The training objective maximizes the cosine similarity of matching pairs while minimizing it for mismatched pairs, yielding highly generalizable zero-shot classifiers.

## Architectural Diagram

```mermaid
graph TD
    A[Image] --> B[Image Encoder]
    C[Text Caption] --> D[Text Encoder]
    B --> E[Image Embedding]
    D --> F[Text Embedding]
    E & F --> G[Compute Similarity Matrix]
    G --> H[InfoNCE / Contrastive Loss]
```

---
[← Back to README](../README.md)
