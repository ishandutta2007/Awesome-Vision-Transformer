# Multi-Head Latent Attention (MLA)

Multi-Head Latent Attention (MLA), popularized by DeepSeek, addresses the memory bottlenecks of the Key-Value (KV) cache in transformer models. Instead of caching high-dimensional key and value vectors for every head, MLA down-projects keys and values into a shared low-rank latent vector before attention calculation. The latent space is up-projected on-the-fly during decoding, significantly reducing the VRAM footprint of long context sequences in multi-modal vision tasks.

## Architectural Diagram

```mermaid
graph TD
    A[Key-Value Sequence] --> B[Low-Rank Down-Projection]
    B --> C[Compressed Latent Vector]
    C --> D[Up-Projection to Multi-Head Keys/Values]
    D --> E[Attention Computation with Queries]
```

---
[← Back to README](../README.md)
