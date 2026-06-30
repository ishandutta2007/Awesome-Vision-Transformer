# Hierarchical Window Transformers

Hierarchical Window Transformers constrain self-attention within localized pixel boundaries (or windows). Layers alternate between standard window-based multi-head self-attention (W-MSA) and shifted window-based multi-head self-attention (SW-MSA). This design drastically reduces the visual token matching search space while maintaining efficient information exchange across window boundaries, making it ideal for downstream tasks like object detection and semantic segmentation.

## Architectural Diagram

```mermaid
graph TD
    A[Input Feature Map] --> B[Subdivide into Local Windows]
    B --> C[Compute Local Window Self-Attention]
    C --> D[Shift Window Borders Diagonally]
    D --> E[Compute Shifted Local Self-Attention]
    E --> F[Feature Map Assembly]
```

---
[← Back to README](../README.md)
