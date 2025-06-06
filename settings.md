# ⚙️ Typhoon V1 (SDXL) – Recommended Settings

This isn’t your average SDXL model—it’s temperamental, stylish, and expects you to treat it right. Follow these settings for best results:

---

## 🧩 Base Generation

- **Resolution**:  
  - 1024x1024 (default, safe)  
  - 896x1152 or 832x1216 (recommended for portraits)  
  - 1152x896 or 1216x832 (recommended for landscapes)  
  - Avoid going ultrawide or ultra-tall—artifacts love to party there.

- **CFG Scale**:  
  - **3.5 to 5.5** is the sweet zone  
  - 4.0 is a safe default  
  - Higher values (6+) tend to overbake and hallucinate nonsense

- **Sampler**:  
  - **DPM++ 2M Karras** (gold standard)  
  - DPM++ SDE Karras is also solid  
  - Avoid DDIM—Typhoon eats it for breakfast and spits out blobs

- **Steps**:  
  - 25–35 steps recommended  
  - Can go lower if speed matters, but you’ll lose that juicy detail

---

## 🔨 Refiner? No Thanks

Typhoon V1 does **not** require the SDXL refiner. In fact, it clashes with it.  
Stick with the base model from start to finish.

---

## 📸 Hires Fix & Upscaling

- **Enable**: Only if you must go beyond 1024px in either dimension  
- **Denoising strength**: 0.4–0.6  
- **Upscale method**: Latent (or ESRGAN if you're wild)  
- **CFG (2nd pass)**: Match the first, or bump slightly for detail  
- Bonus tip: 1.5x upscale is usually enough; 2x gets heavy fast

---

## 🎨 VAE

- **Don't use one**  
  SDXL has internal VAE support—don’t mess with it unless you *really* know what you’re doing.

---

## ⚠️ Known Quirks

- **Prompt Overload**: Too many tags? Model might ignore half of them. Keep prompts lean and specific.  
- **Avoid Merging**: Typhoon SDXL is not merge-safe. Not with anything. Not even itself.  
- **Third-party sites**: Expect unpredictable results. This model was trained for local generation workflows.

---

Use it with care, keep your prompts tight, and Typhoon will return the favor with slick, stylish generations. Abuse it, and it’ll remind you who’s in charge.
