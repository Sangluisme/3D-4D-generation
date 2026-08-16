# 4D Generation Methods

> **Using this repo? Go straight to [papers.md](papers.md)** — that's the paper list.

Recent 4D (dynamic 3D) generation papers, tracked in a single table: [papers.md](papers.md).

Each row has one paper with **Target** (object-level vs. scene-level) and **Method** columns, using the same taxonomy as [3D generation](../3D-generation/papers.md) rather than a representation-based category like "Gaussian" — nearly every 4D paper outputs dynamic Gaussians regardless of mechanism, which made representation a poor primary axis:

- Diffusion — direct sampling of the video/multi-view/4D signal
- Auto-regression — sequential frame/token/state prediction
- Flow-matching — currently an empty category for full 4D asset generation (see the gap note in the table)
- Score-distillation optimization — iterative SDS-style optimization against a frozen 2D/video diffusion prior; the single largest category in 4D generation today
- Feed-forward reconstruction — single-pass regression or direct (non-SDS) fitting to an already-generated video
- Other — physics-guided, training-free, compositional/multi-agent, editing, GAN (essentially absent in 4D)

Sort or filter the table by either column to reproduce the two categorized views. Some papers straddle categories (e.g. video-diffusion output reconstructed into Gaussians via fitting vs. via a live SDS gradient loop); each is placed by its core technical contribution, with a note in the Method cell where the boundary is genuinely blurry (e.g. EPONA is tagged "Diffusion + Auto-regression (hybrid)").
