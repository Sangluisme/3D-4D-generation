# 2D Generation with Editing — Paper Database

Single source of truth: one row per paper. Sort/filter by **Category** to reproduce the by-method view.

| Title | Category | Year | Venue | arXiv | Summary |
|---|---|---|---|---|---|
| SDEdit | Inversion + attention/latent manipulation | 2022 | ICLR 2022 | [2108.01073](https://arxiv.org/abs/2108.01073) | Adds noise to an input image then runs the reverse SDE/denoising process partway, trading edit strength against fidelity. |
| Prompt-to-Prompt | Inversion + attention/latent manipulation | 2022 | — | [2208.01626](https://arxiv.org/abs/2208.01626) | Injects and reweights cross-attention maps between source/target prompts during denoising so shared structure stays fixed. |
| Null-text Inversion | Inversion + attention/latent manipulation | 2023 | CVPR 2023 | — | Optimizes only the unconditional (null) embedding per image so DDIM inversion reconstructs a real photo exactly. |
| Plug-and-Play | Inversion + attention/latent manipulation | 2023 | CVPR 2023 | [2211.12572](https://arxiv.org/abs/2211.12572) | Injects the source image's DDIM-inverted self-attention and spatial features into generation under a new prompt. |
| pix2pix-zero | Inversion + attention/latent manipulation | 2023 | SIGGRAPH 2023 | [2302.03027](https://arxiv.org/abs/2302.03027) | Computes a CLIP text-embedding editing direction and applies it via cross-attention guidance, no prompt tuning needed. |
| MasaCtrl | Inversion + attention/latent manipulation | — | — | — | Replaces self-attention with mutual self-attention between a reconstruction branch and a generation branch, tuning-free. |
| Direct Inversion / PnP-Inversion | Inversion + attention/latent manipulation | — | — | [2310.01506](https://arxiv.org/abs/2310.01506) | Analyzes and corrects accumulated DDIM inversion error with a lightweight fix, boosting fidelity for PnP-style editors. |
| Imagic | Inversion + attention/latent manipulation | — | — | [2210.09276](https://arxiv.org/abs/2210.09276) | Interpolates between an optimized source-matching embedding and the target embedding, then briefly fine-tunes at that point. |
| InstructPix2Pix | Instruction-following | 2022 | — | — | Trains a conditional diffusion model on synthetic (image, instruction, edited-image) triples for one-pass instruction editing. |
| MagicBrush | Instruction-following | 2023 | NeurIPS 2023 (Datasets) | [2306.10012](https://arxiv.org/abs/2306.10012) | A large manually-annotated instruction-editing dataset used to fine-tune InstructPix2Pix, fixing low-fidelity synthetic edits. |
| HIVE | Instruction-following | 2024 | CVPR 2024 | [2303.09618](https://arxiv.org/abs/2303.09618) | Collects human preference rankings over instructional edits and fine-tunes the editor with a reward-weighted objective. |
| InstructDiffusion | Instruction-following | 2024 | CVPR 2024 | — | Casts many vision tasks (segmentation, keypoint detection, editing) as a unified "instruction → pixel edit" problem. |
| Emu Edit | Instruction-following | 2024 | CVPR 2024 | [2311.10089](https://arxiv.org/abs/2311.10089) | Multi-tasks a single diffusion model across many formally-specified editing/vision tasks via learned task embeddings. |
| SmartEdit | Instruction-following | 2024 | CVPR 2024 | — | Uses a VLM (LLaVA) to comprehend complex instructions and fuses that reasoning with diffusion image features. |
| SeedEdit 3.0 | Instruction-following | — | — | [2506.05083](https://arxiv.org/abs/2506.05083) | A fast, high-quality generative instruction editor trained end-to-end on large-scale instruction-edit data. |
| Step1X-Edit | Instruction-following | — | — | [2504.17761](https://arxiv.org/abs/2504.17761) | A multimodal LLM jointly encodes reference image + instruction into a latent conditioning a diffusion decoder. |
| Blended Diffusion | Mask/region-based inpainting | — | — | [2111.14818](https://arxiv.org/abs/2111.14818) | Blends noised original-image regions outside a mask with the sampling trajectory inside it, guided by CLIP, at every step. |
| Paint by Example | Mask/region-based inpainting | 2023 | CVPR 2023 | [2211.13227](https://arxiv.org/abs/2211.13227) | Conditions inpainting on an exemplar reference image via a bottlenecked CLIP embedding, preventing copy-pasting. |
| SmartBrush | Mask/region-based inpainting | — | — | — | Conditions inpainting on both text and an adjustable-precision mask (tight instance mask to coarse bounding box). |
| Imagen Editor | Mask/region-based inpainting | — | — | — | Fine-tunes a cascaded Imagen diffusion model for text-guided inpainting, feeding image+mask context into every stage. |
| GANSpace | GAN-based latent-space editing | 2020 | NeurIPS 2020 | [2004.02546](https://arxiv.org/abs/2004.02546) | Applies PCA to sampled GAN latent activations (W space) to discover unsupervised, interpretable edit directions. |
| InterFaceGAN | GAN-based latent-space editing | — | — | [2005.09635](https://arxiv.org/abs/2005.09635) | Trains a linear SVM on attribute-labeled latent codes to find linear edit directions for semantic attributes. |
| StyleGAN-NADA | GAN-based latent-space editing | — | — | [2108.00946](https://arxiv.org/abs/2108.00946) | Fine-tunes the StyleGAN generator with a CLIP-based directional loss for zero-shot text-driven domain adaptation. |
| StyleCLIP | GAN-based latent-space editing | — | — | — | Uses CLIP's joint embedding to optimize a latent code, train a mapper, or find a global StyleGAN direction matching text. |
| DreamBooth | Subject-driven / personalization | — | — | [2208.12242](https://arxiv.org/abs/2208.12242) | Fine-tunes a full diffusion model on a few images of a subject bound to a rare-token identifier, plus a class-preservation loss. |
| Custom Diffusion | Subject-driven / personalization | 2023 | CVPR 2023 | [2212.04488](https://arxiv.org/abs/2212.04488) | Fine-tunes only cross-attention key/value projections for a new concept, with closed-form multi-concept merging. |
| SEED-X | Unified / any-to-any foundation model | — | — | [2404.14396](https://arxiv.org/abs/2404.14396) | A unified multimodal LLM interleaving understanding/generation tokens for both instructional generation and pixel-precise editing. |
| OmniGen | Unified / any-to-any foundation model | — | — | [2409.11340](https://arxiv.org/abs/2409.11340) | Jointly models arbitrary interleaved text-and-image inputs in one unified transformer/diffusion architecture, no per-condition encoders. |
| FLUX.1 Kontext | Unified / any-to-any foundation model | — | — | [2506.15742](https://arxiv.org/abs/2506.15742) | A flow-matching rectified-flow transformer treats a reference image as in-context tokens for iterative, identity-consistent editing. |
| Qwen-Image-Edit | Unified / any-to-any foundation model | — | — | — | Builds on Qwen-Image + Qwen2.5-VL, treating reference-image tokens the same as generated tokens (mutual attention). |

**Note**: Step1X-Edit spans two categories (Instruction-following and Unified foundation-model) — an MLLM-conditioned unified editor that's also trained on instruction-edit data; listed once under Instruction-following, cross-reference from Unified.
