# Colab Lab: ViT on CIFAR-10 (Q1) and Text-Driven Segmentation with SAM 2 (Q2)

Deadline: Saturday, 11:59 PM (local time).

This repository intentionally contains only three files, as required:
- q1.ipynb
- q2.ipynb
- README.md

Both notebooks are designed to run end-to-end on Google Colab with a GPU runtime.

Quick start (Colab)
- Open this repo on GitHub and open q1.ipynb (and later q2.ipynb) in Google Colab.
- In Colab: Runtime -> Change runtime type -> Hardware accelerator: GPU.
- Run all cells from top to bottom. Install cells are provided at the top of each notebook.

Q1 — Vision Transformer on CIFAR-10 (PyTorch)
- Implements: patchify, learnable positional embeddings, CLS token, Transformer encoder blocks (MHSA + MLP with residual + norm), classification from CLS token.
- Includes a config cell you can tweak (patch size, depth, width, heads, dropout, optimizer, schedule, etc.).
- Goal: maximize CIFAR-10 test accuracy.

Best model config (to fill in after you finish your runs)
- Patch size: <value>
- Depth: <value>
- Embed dim: <value>
- Heads: <value>
- MLP ratio: <value>
- Optimizer / LR schedule: <value>
- Augmentations: <value>

Results (test accuracy on CIFAR-10)
| Model | Patch | Depth | Heads | Aug | Optim/Sched | Test Acc (%) |
|-------|-------|-------|-------|-----|-------------|---------------|
| ViT (best) | <p> | <d> | <h> | <aug> | <opt/sched> | <acc%> |

Bonus (optional analysis; keep it concise)
- Brief notes on patch size choices, depth/width trade-offs, augmentation effects, optimizer/schedule variants, overlapping vs. non-overlapping patches, etc.

Q2 — Text-Driven Image Segmentation with SAM 2
Pipeline (as implemented in q2.ipynb)
- Load image (upload or URL) -> accept text prompt -> convert text to region seeds (e.g., via CLIPSeg) -> feed seeds to SAM 2 -> display final mask overlay.
- Notebook includes install cells and a simple, end-to-end runnable scaffold on Colab. If SAM 2 API or checkpoints change, instructions are included in the notebook to update the install/checkpoint cell accordingly.

Limitations & notes (Q2)
- Quality depends on the text-to-region seeds; ambiguous prompts can degrade results.
- You may need to tune thresholding or number of seed points.
- SAM 2 checkpoint and API can evolve; use the latest recommended weights from the official repo if needed.

Submission checklist
- Colab only: Both notebooks run top-to-bottom on GPU.
- GitHub repo contains only q1.ipynb, q2.ipynb, README.md.
- Submit your best CIFAR-10 test accuracy (%) and repo link via the provided Google Form.
