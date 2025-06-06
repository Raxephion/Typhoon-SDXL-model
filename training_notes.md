# Typhoon V1 – Training Notes

This document outlines the development process, training challenges, and methods used to bring Typhoon V1 to life.

---

## ⚙️ Model Development

Typhoon was trained in phases — both as a checkpoint and with supporting LoRAs, which were carefully merged into the final model.

- **Phase 1: Base Checkpoint Training**  
  Initial training began from a stable SDXL base model. This was selected for being minimally altered — free of unnecessary "refiner dependencies", NSFW filters, or baked-in aesthetic biases. The goal was to create a clean artistic foundation that could scale.

- **Phase 2: LoRA Training & Merging**  
  Custom LoRAs were trained on **1024×1024** images, targeting specific traits like lighting, composition, facial expression clarity, and texture stylization.

  These LoRAs were then:
  - Evaluated using strength/impact tests
  - Merged into the base SDXL checkpoint one at a time
  - Tuned with weight offsets to maintain stylistic integrity

  This manual merging process was tedious but essential — automated pipelines consistently produced inferior results or broke the consistency of the visual language.

  About **75% of all training runs failed** due to instability, bad weights, or aesthetic degradation.

---

## 🧪 LoRA Analyzer Tooling

The challenges above prompted the creation of two custom diagnostic tools:

- [**LoRA Strength Analyzer**](https://github.com/Raxephion/loRA-Strength-Analyser)  
  This tool compares outputs at multiple LoRA strength values using SSIM/BRISQUE metrics to detect degradation or collapse.

- [**LoRA Epoch Analyzer**](https://github.com/Raxephion/loRA-Epoch-Analyser)  
  Evaluates aesthetic and structural quality across training epochs to identify optimal snapshot points.

These tools are **open-source** and currently in **alpha**.

---

## 💸 GPU Rental & Costs

No local GPUs were harmed in the making of this model — because I didn’t have any. Instead:

- All training was performed via rented A100 and 3090 instances
- Compute time was spent across multiple providers (RunPod, Vast.ai, Lambda)
- The failure rate was expensive (three dead checkpoints, endless reruns)

In total, this wasn’t a budget operation. Call it a hobby. A very expensive hobby.

---

*Enjoy the storm.*
