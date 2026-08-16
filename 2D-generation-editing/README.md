# 2D Generation with Editing

> **Using this repo? Go straight to [papers.md](papers.md)** — that's the paper list.

Papers whose core contribution is *editing* an existing or generated image — not synthesizing a fresh image from scratch. Tracked in a single table: [papers.md](papers.md).

## Categorization criterion

Categorized by **what technically drives the edit**: does it need training data of edit pairs, a mask, GAN latent space vs. diffusion feature space, per-subject fine-tuning, or is it a unified any-to-any foundation model? This is the axis that actually separates how these papers work, more than surface features like "what task" they perform.

- Inversion + attention/latent manipulation — training-free diffusion editing
- Instruction-following — trained end-to-end on instruction↔image pairs
- Mask/region-based inpainting
- GAN-based latent-space editing
- Subject-driven / personalization-based editing
- Unified / any-to-any multimodal foundation-model editing

Sort or filter [papers.md](papers.md) by the **Category** column to get each view.
