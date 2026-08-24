# Adaptive-Patch-Clustering-with-Suboptimal-Wiener-Filter-in-PCA-Domain
# Adaptive Patch Clustering with Suboptimal Wiener Filter in PCA Domain

An image denoising implementation combining adaptive patch clustering with a suboptimal Wiener filter applied in the Principal Component Analysis (PCA) domain, evaluated across multiple noise types.

## 🎯 Project Overview

Image degradation from noise introduced during acquisition is a long-standing problem in image processing. This project implements and validates a denoising pipeline where image patches are **adaptively clustered** and then denoised using a **suboptimal Wiener filter** operating in the **PCA-transformed domain** — exploiting the fact that principal components tend to capture scene structure, while trailing components mainly capture noise.

The approach is evaluated on grayscale images corrupted by four distinct noise types:
- **Gaussian noise**
- **Salt & pepper noise**
- **Speckle noise**
- **Poisson noise**

## 🧪 Methodology

1. **Noise corruption** — a clean grayscale image is corrupted using each of the four noise models in turn.
2. **Adaptive patch clustering** — overlapping image patches are grouped into clusters based on structural similarity, allowing patches with similar local content to be denoised together.
3. **PCA transform** — each cluster of patches is projected into its own PCA basis, concentrating signal energy into the leading components.
4. **Suboptimal Wiener filtering** — a Wiener filter is applied in the PCA domain to suppress noise-dominated coefficients while preserving signal-carrying components.
5. **Reconstruction** — denoised patches are transformed back and aggregated into the final restored image.

## 📊 Evaluation

Denoising performance is quantified using standard image quality metrics, typically including:
- **PSNR** (Peak Signal-to-Noise Ratio)
- **SSIM** (Structural Similarity Index)
- Additional perceptual/quality metrics as applicable

Each noise type is evaluated separately to give a comprehensive picture of how the method performs under different corruption conditions.

## 📁 Repository Structure

```
.
├── (denoising implementation notebook/script)
├── (sample/test images)
└── README.md
```

*(Update this section with your actual file names once finalized — see naming suggestions below.)*

## 🚀 Running the Project

```
pip install numpy scipy scikit-image matplotlib opencv-python
# then run the notebook or script, e.g.:
jupyter notebook <notebook_name>.ipynb
```

## 📈 Results

*(Add: PSNR/SSIM comparison table across the four noise types, plus before/after denoising image comparisons.)*

## 📚 Reference

This implementation is based on the methodology described in:

Rane, S., Ragha, L., Biradar, S., & Pandit, V. (2022). Image Denoising using Adaptive Patch Clustering with Suboptimal Wiener Filter in PCA Domain. *International Journal of Engineering Trends and Technology (IJETT)*, 70(11), 19–27.

## 🎓 Context

Developed as part of coursework/research within a Data Science MS program (IMSciences, Peshawar), focused on image processing and denoising techniques.

## 📄 License

Educational/academic use.
