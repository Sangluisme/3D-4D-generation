# 3D Generation Methods

> **Using this repo? Go straight to [papers.md](papers.md)** — that's the paper list.

Recent 3D generation papers, tracked in a single table: [papers.md](papers.md).

Each row has one paper with **Target** (object-level vs. scene-level) and **Method** columns:

- Diffusion
- Auto-regression
- Flow-matching
- Score-distillation optimization — iterative SDS-style optimization against a frozen 2D diffusion prior
- Feed-forward regression — single deterministic forward pass, no sampling or per-asset optimization
- GAN

Sort or filter the table by either column to reproduce the two categorized views instruction.md originally asked for — there's a single source of truth per paper instead of duplicate entries across separate by-target/by-method files. This method taxonomy is shared with [4D generation](../4D-generation/papers.md) so the two domains are directly comparable.
