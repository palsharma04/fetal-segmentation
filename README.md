# fetal-segmentation

# Project Summary

This repository showcases a complete deep learning pipeline for **multi-label segmentation** of fetal anatomical structures (fetus, placenta, umbilical cord, and amniotic fluid) in **bSSFP MRI scans**.  
The project is designed for research and educational use, aiming to support clinical translation of automated fetal MRI analysis through **open-source, benchmarked models**.

---

## Objective

This project implements and compares two deep learning pipelines for automated segmentation of fetal and uterine structures in volumetric MRI:

- **MONAI-based models** (2D and 3D U-Net)
- **nnU-Net-based models** (2D and 3D full-resolution)

The goal is to evaluate and compare the performance of these two popular medical imaging frameworks on multi-label segmentation tasks involving:
- Fetal body  
- Placenta  
- Umbilical cord  
- Amniotic fluid

Performance is evaluated using:
- **Dice score**
- **Volume overlap**
- **Precision & recall**
- **Qualitative visualization**

---

## Code Overview

| File | Description |
|------|-------------|
| `2d-preprocessing-training.py` | Trains and evaluates a **2D MONAI U-Net** using slice-wise fetal MRI data. Includes preprocessing, augmentation, training, and visualization. |
| `3d-preprocessing-training.py` | Trains and evaluates a **3D MONAI U-Net** on full volumetric MRI using sliding window inference and Dice + CE loss. |
| `2d-testing.py` | Inference and visualization script for the **2D MONAI model**. Overlays predicted segmentations on grayscale MRI slices. |
| `3d-testing.py` | Inference and visualization script for the **3D MONAI model**, showing segmentation overlays in 3D anatomical views. |
| `2d-3d-nnunet.py` | Configures and trains **2D and 3D nnU-Net** models using the framework’s auto-configuration and training pipeline. |

---

## Example Outputs

Below are examples of qualitative results from the trained models:

- Input MRI slice (grayscale)
- Ground truth segmentation overlaid in color
- Model prediction overlaid in color

![Axial Example](examples/axial_output.png)
![Coronal Example](examples/coronal_output.png)

---

## References

If you use this code in your research, please consider citing:



