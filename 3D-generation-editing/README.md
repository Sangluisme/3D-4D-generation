# 3D Generation with Editing

> **Using this repo? Go straight to [papers.md](papers.md)** — that's the paper list.

Papers whose core contribution is *editing* an existing static 3D asset or scene (a NeRF, mesh, or 3D Gaussian Splatting scene) — not generating one from scratch, and not dynamic/4D scene editing (covered separately in [4D-generation/papers.md](../4D-generation/papers.md)). Tracked in a single table: [papers.md](papers.md).

## Categorization criterion

Categorized by the **technical editing mechanism** — the actual optimization/inference loop used to turn an edit instruction into a changed 3D asset. This cuts deeper than surface features like "NeRF vs. Gaussian" (most families now have instantiations in both) or "geometry vs. appearance" (most papers touch both).

- Iterative dataset-update — edit rendered training images with a 2D model, re-optimize, repeat
- Score-distillation optimization — SDS/DDS gradients from a 2D diffusion model update the 3D representation directly
- One-shot multi-view-consistent — enforce consistency across views during a single diffusion editing pass, then re-fit once
- Segmentation/grouping-based — localize the edit to a 3D region/instance via lifted 2D masks
- Mesh/texture repainting — text/image-to-UV-texture painting on an existing mesh
- Explicit geometric deformation — direct proxy-based (point/cage) deformation, no diffusion re-synthesis of appearance

Sort or filter [papers.md](papers.md) by the **Category** column to get each view.
