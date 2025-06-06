# 🌀 Usage Guide for Typhoon V1 (SDXL)

Typhoon V1 is a visually expressive, artistically biased SDXL model trained for high-quality, creative generations. This guide explains how to get the best results out of it — whether you’re using `.safetensors` or the `diffusers` version.

---

## 🧠 General Prompting Advice

Typhoon SDXL works best with **tag-style prompts**. It’s not allergic to natural language, but structured tags are much more reliable due to the way it was trained.

**Example:**

`masterpiece, best quality, dramatic lighting, solo, medium shot, ultra-detailed, looking at viewer`

> No trigger words are needed. You can still use artist tags, composition terms, or style descriptors if you want to direct the output more precisely.

---

## 🛠 Recommended Generation Settings

- **Resolution**: `1024x1024` (native)
  - You can safely go to `1152x896` or `960x1280` for variation.
  - Avoid ultrawide — it’s still an SDXL model, not a landscape painter.
- **CFG Scale**: `3 – 7`  
  - Lower values (~3–4) give more naturalistic outputs  
  - Higher values (~6–7) increase detail but might hallucinate
- **Sampler**:  
  - `DPM++ 2M Karras` (recommended)  
  - `DPM++ SDE Karras` also works well  
- **Steps**: 25–35  
- **Refiner**: Not required or recommended — Typhoon is tuned for full strength outputs without it.

---

## 🔨 Hires Fix (Optional)

Not strictly necessary for SDXL, but if you want ultra-detailed upscales:

- **Deno**
