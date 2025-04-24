# aurora-wonder-demo

*A GPU‑powered fractal tunnel that morphs between golden‑ratio geometries, complete with optional 528 Hz harmony.*

![Aurora Wonder screenshot](docs/screenshot.webp)

## ✨ Features

| Control | What it does |
|---------|--------------|
| **Constant** selector | Instantly shifts the scaling constant used in the fractal between<br>• φ ≈ 1.618 (Golden Ratio)<br>• φ² ≈ 2.618<br>• **Aurora** ≈ 2.914 (from the Aurora Equation)<br>• **Aurora⁻¹** ≈ 0.077 |
| **Depth** slider | Sets the maximum iteration count (20 → 120) |
| **Tunnel** slider | Warps the flat fractal into a 3‑D‑look spiral tunnel |
| **Sound** toggle | One‑click 528 Hz major chord (C‑E‑G) for resonance |

All visuals are rendered in a single WebGL fragment shader at full speed on desktop and mobile.

## 🔧 Quick Start

```bash
# clone & open
$ git clone https://github.com/your‑user/aurora‑wonder-demo.git
$ cd aurora‑wonder-demo
# just open aurora-wonder.html in any browser
```

No build step, no dependencies—pure HTML + GLSL + vanilla JS.

## 🏃‍♂️ Controls

* **Mouse / Touch** — Drag to pan, wheel/pinch to zoom (mobile‑friendly).
* **UI sliders** — Depth, tunnel strength, constant swap.
* **`🔇 Sound`** — Starts/stops the 528 Hz chord (audio begins only after a user click to satisfy browser autoplay rules).

## 🚀 How It Works

* **Fragment shader** computes an iterative complex‑plane function using the selected constant.  By warping UV‑coords `(r,θ)` with `r → r^(1−tunnel)` and `θ += time`, we get a continuous fly‑through illusion.
* **Golden‑angle hue cycling** (`+137.5°` per frame) ensures endlessly varied aurora colors.
* **Adaptive fade** on radius prevents screen‑center blow‑out.
* **CPU side** only updates four uniforms each frame—everything else is on the GPU.

## 📦 Offline‑Ready

All assets are inline.  Drop the folder on an air‑gapped machine and it runs.

## 📝 License

MIT—do anything you like, but a link back would be cosmic. 🌌

---

> *Awaken the Core. Illuminate the Quiet.* 🐉✨

