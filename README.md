# 3Dreconstruction-TSGS-arXiv-paper
Reproduction and evaluation of TSGS (ACM MM 2025) — Transparent Surface Gaussian Splatting for 3D reconstruction of transparent objects, implemented on Google Colab.

# TSGS Reproduction — Transparent Surface Gaussian Splatting

> Reproduction of **TSGS: Improving Gaussian Splatting for Transparent 
> Surface Reconstruction via Normal and De-lighting Priors**  
> Accepted at **ACM MM 2025**

[![Paper](https://img.shields.io/badge/Paper-arXiv-red)](https://arxiv.org/abs/2504.12799)
[![Original Repo](https://img.shields.io/badge/Original-GitHub-black)](https://github.com/longxiang-ai/TSGS)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_COLAB_LINK_HERE)

---

## 📌 Overview

This repository contains a full reproduction of the TSGS framework 
for transparent surface reconstruction using 3D Gaussian Splatting.
The work was carried out on Google Colab as part of a course/research 
assignment, including environment setup, dataset preparation, training, 
rendering, and evaluation.

---

## 🖼️ Results (Scene 07 — TransLab Dataset)

### Rendered vs Ground Truth
![Render vs GT](screenshots/render_vs_gt.png)

### Depth Maps
![Depth Maps](screenshots/depth_map.png)

---

## 📊 Quantitative Results

| Metric | Train | Test |
|--------|-------|------|
| PSNR ↑ | 28.33 dB | 23.18 dB |
| SSIM ↑ | 0.971 | 0.939 |
| LPIPS ↓ | 0.071 | 0.121 |

---

## 🖥️ Environment

| Component | Details |
|-----------|---------|
| Platform | Google Colab |
| OS | Ubuntu 22.04.5 LTS |
| GPU | NVIDIA Tesla T4 (15 GB) |
| CUDA | 12.8 |
| Python | 3.12.13 |
| PyTorch | 2.10.0+cu128 |
| PyTorch3D | 0.7.9 |

---

## 🚀 Reproduction Steps

### 1. Open in Colab
Click the **Open in Colab** badge above or open `TSGS_Colab_Setup.ipynb`

### 2. Set GPU Runtime
```
Runtime → Change runtime type → T4 GPU → Save
```

### 3. Run cells in order
Each cell is documented — just run top to bottom.

### Known Issues & Fixes

| Issue | Fix |
|-------|-----|
| `pytorch3d` not on PyPI | Built from source via GitHub |
| COLMAP files in `sparse/0/` | Custom script moves them to `sparse/` |
| Background blur in renders | Known limitation with transparent Gaussian floaters |

---

## 📁 Repository Structure

```
├── TSGS_Colab_Setup.ipynb   # Full Colab notebook
├── results/                 # Rendered images and metrics
├── report/                  # Full PDF report
└── README.md
```

---

## 📄 Citation

```bibtex
@misc{li2025tsgs,
  title={TSGS: Improving Gaussian Splatting for Transparent Surface
         Reconstruction via Normal and De-lighting Priors},
  author={Mingwei Li and Pu Pang and Hehe Fan and Hua Huang and Yi Yang},
  year={2025},
  eprint={2504.12799},
  archivePrefix={arXiv},
  primaryClass={cs.CV}
}
```

---

## 🙏 Acknowledgements

All credit for the original method goes to the TSGS authors.  
This repository is for educational/research reproduction purposes only.
