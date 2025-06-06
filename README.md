# 🌩️ Typhoon (SDXL)

> **📢 Welcome to Typhoon SDXL — a stylized, cinematic model built for clarity, precision, and the occasional artful overkill.**  
> This is *not* a raw realism model. It’s got opinions. Strong ones.

---

[![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)](https://www.python.org/)
[![GitHub Repo](https://img.shields.io/badge/GitHub-Raxephion/Typhoon--SDXL--model-181717?logo=github)](https://github.com/Raxephion/Typhoon-SDXL-model)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-Raxephion/Typhoon--SDXL--V1-orange?logo=huggingface)](https://huggingface.co/Raxephion)
![HF Downloads](https://img.shields.io/badge/Downloads-Fresh%20Out%20The%20Lab-orange?logo=huggingface)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

---

## 🧠 About

Typhoon SDXL began as a planned sequel to Tornado — but things escalated. What started as *Tornado v3* took on its own identity, eventually diverging into a standalone model with a distinct, stylized realism that balances cinematic lighting, visual depth, and highly clean detail.

This model was built from the ground up using:
- ✅ Full SDXL 1.0 training (not a merge)
- ✅ Clean, curated datasets with subject + lighting emphasis
- ✅ A suite of custom-trained LoRAs selectively merged back in
- ✅ Manual tuning using merge weighting, style balancing, and… trial-by-GPU-failure

> Fun fact: 1 out of every 4 training runs failed. So yes, your prompts aren’t the only thing that gets unstable.

---

## 🌪️ What Makes Typhoon SDXL Different?

- **Stylized Precision:** Default outputs are vivid, high-detail, and slightly polished — favoring “clean realism” over documentary grit.
- **Portrait-Grade Quality:** Close-ups are sharp, defined, and don’t need Adetailer.
- **Cinematic Depth & Lighting:** Reworked light behavior gives more drama per pixel.
- **Prompt Simplicity:** No trigger words. Just describe what you want. Seriously.

Expect strong highlights, bold lighting, high-contrast renders, and an aesthetic that sits halfway between real-world and a concept art board.

> ⚠️ It *can* do raw realism — but it won’t default there. You’ll have to nudge it.

---

## 📦 Model Characteristics

| Feature               | Notes                                                                 |
|-----------------------|-----------------------------------------------------------------------|
| Base Model            | SDXL 1.0                                                              |
| Resolution            | Native 1024x1024                                                      |
| Default Aesthetic     | “Rendered real” – clean, vivid, cinematic realism                     |
| Close-up Performance  | Excellent – no Adetailer needed                                       |
| Lighting & Composition| Enhanced depth, strong shadows, balanced contrast                     |
| Prompting Style       | Natural language and/or tag-based — both work well                    |
| NSFW Output           | **Unstable** — neutered base, partial restoration, use with caution   |

---

## ⚙️ Recommended Settings

These were tested on Forge WebUI, but should translate well to most SDXL interfaces.

- **CFG Scale:** `0.3 – 0.8`  
  > Sweet spot seems to be `0.5 – 0.7` depending on lighting and scene complexity

- **Sampler:**  
  - `DPM++ 2M Karras` (🥇 recommended)  
  - `Euler`, `Euler A`  
  - `DPM++ SDE`  
  - Most usual suspects work fine

- **Steps:** `15+`  
  > More steps = more detail, but diminishing returns after 30-ish

- **Face Restoration:**  
  > ❌ Disable it. Especially for close-ups — it muddies the eyes.

- **Prompting:**  
  - Descriptive sentence-style prompts are highly effective  
  - Tag-style also works, especially for concept art or fantasy styles

---

## ✨ Style Fit

Typhoon SDXL works best for:
- Portraits and close-ups
- Cinematic compositions
- Soft realism and fantasy realism
- Stylized concept art and clean render-style scenes

You’ll get bold visuals with depth, rich lighting, and smooth but defined surface detail.

---

## 📷 Sample Output

All images generated **natively** using Typhoon SDXL without external LoRAs, inpainting, or fixers. What you see is pure model output.

<table> <tr> <td><img src="./images/typhoonxl_0001.png" width="160"/></td> <td><img src="./images/typhoonxl_0002.png" width="160"/></td> <td><img src="./images/typhoonxl_0003.png" width="160"/></td> <td><img src="./images/typhoonxl_0004.png" width="160"/></td> <td><img src="./images/typhoonxl_0005.png" width="160"/></td> </tr> </table>

---

## 🛠️ Behind The Storm

Building Typhoon SDXL was not a straight line. The process involved:

1. **Base Checkpoint Training** — Starting from clean SDXL 1.0
2. **Targeted LoRA Development** — Custom LoRAs were trained for lighting, facial detail, anatomy, and style
3. **Manual Merge Tuning** — Each LoRA was merged back via experimental merge weights + scaling
4. **Hand Calibration** — This wasn’t a ComfyUI pipeline — merge order and value tweaks were done manually.

Also developed during the process:

- [`LoRA Strength Analyzer`](https://github.com/Raxephion/loRA-Strength-Analyser) — Get math-backed advice on LoRA merge weights
- [`LoRA Epoch Analyzer`](https://github.com/Raxephion/loRA-Epoch-Analyser) — Find which epoch actually did the work

Both tools are in alpha and being wrapped into a Gradio UI soon™.

---

## ⚠️ Limitations

- NSFW output is **very inconsistent** — some recovery work has been done, but YMMV
- Default aesthetic leans “stylized-real” — gritty realism must be forced
- High-gloss lighting can over-emphasize skin or fabric unless balanced
- Like all SDXL models, heavy prompting can still cause drift if poorly structured

---

## 🚫 Usage Restrictions

This model is released under a modified CreativeML Open RAIL-M license:

- ✅ Personal, local use is encouraged.
- ❌ **Do not merge** with other models — Typhoon’s internal balance will break.
- ❌ **Do not upload** to public generation sites, bots, or APIs.

> Basically: use it, don’t abuse it. Keep the storm local.

---

## 📍 Attribution

- Base: Stable Diffusion XL 1.0 (`stabilityai/stable-diffusion-xl-base-1.0`)
- VAE: [stabilityai/sdxl-vae](https://huggingface.co/stabilityai/sdxl-vae)
- Custom Tools: [Raxephion/loRA-Strength-Analyser](https://github.com/Raxephion/loRA-Strength-Analyser), [Raxephion/loRA-Epoch-Analyser](https://github.com/Raxephion/loRA-Epoch-Analyser)
- Hugging Face Repo: [Raxephion/Typhoon-SDXL-V1](https://huggingface.co/Raxephion/Typhoon-SDXL-V1)

---

## ☕ Support the Storm

If you like what I’m building — Typhoon, Tornado, tools, and controlled chaos — and want to help keep the GPUs humming:

**💖 [https://ko-fi.com/raxephion](https://ko-fi.com/raxephion)**

It helps cover compute, coffee, and catastrophic merge experiments.

---

### 🌩️ Enjoy the storm!
