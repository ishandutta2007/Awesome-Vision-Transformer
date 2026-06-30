# Autonomous Vehicle Spatio-Temporal BEV Perception Stacks

Autonomous Vehicle Spatio-Temporal BEV Perception Stacks aggregate inputs from multiple multi-camera video streams into a unified 3D Bird's-Eye-View (BEV) map. The BEVFormer architecture uses grid-shaped BEV queries to perform spatial cross-attention across cameras and temporal self-attention across history frames. This provides stable object tracking, velocity estimation, and robust self-driving navigation maps.

## Architectural Diagram

```mermaid
graph TD
    A[Multi-Camera 2D Streams] --> B[Spatio-Temporal Transformer]
    B --> C[Spatial Cross-Attention]
    B --> D[Temporal Self-Attention]
    C & D --> E[Unified 3D Bird's-Eye-View Grid Map]
```

---
[← Back to README](../README.md)
