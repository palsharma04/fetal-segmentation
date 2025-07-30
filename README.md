# fetal-segmentation

Project Summary
This repository showcases a complete deep learning pipeline for multi-label segmentation of fetal anatomical structures (fetus, placenta, umbilical cord, and amniotic fluid) in bSSFP MRI scans. The project is designed for research and educational use, and aims to support clinical translation of automated fetal MRI analysis through open-source, benchmarked models.

This project implements and compares two deep learning pipelines for automated segmentation of fetal and uterine structures in volumetric MRI:

MONAI-based models (2D and 3D U-Net)

nnU-Net-based models (2D and 3D full-resolution)

The goal is to evaluate and compare the performance of these two popular medical imaging frameworks on multi-label segmentation tasks involving fetal body, placenta, umbilical cord, and amniotic fluid.

Code Functions:
2d-preprocessing-training.py: Trains and evaluates a 2D MONAI U-Net using slice-wise fetal MRI data. Includes preprocessing, augmentation, training loops, and visualization.

3d-preprocessing-training.py: Trains and evaluates a 3D MONAI U-Net on full volumetric MRI data using sliding window inference and Dice/CE loss.

2d-testing.py: Inference and visualization script for  2D MONAI model, used to overlay predicted segmentations on grayscale MRI for visual validation.

3d-testing.py: Inference and visualization script for 3D MONAI model, used to overlay predicted segmentations on grayscale MRI for visual validation.

2d-3d-nnunet.py: Configures and trains the nnU-Net (2D and 3D) for the same dataset using the framework’s auto-configuration and built-in training logic.
