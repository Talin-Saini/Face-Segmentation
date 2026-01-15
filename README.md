# Face Segmentation on Easy Portrait Dataset using U-Net and DeepLabV3

This repository contains Jupyter Notebook implementations for **face segmentation** on the **Easy Portrait dataset** using **U-Net** and **DeepLabV3**.  
The project uses **Run-Length Encoding (RLE)** for mask representation and decoding during training and evaluation.

---

## Overview

Face segmentation is a pixel-wise classification task where each pixel is labeled as **face** or **background**.  
This project compares a classical encoder–decoder segmentation network (**U-Net**) with a modern semantic segmentation model (**DeepLabV3**) for accurate face region segmentation in portrait images.

Ground truth masks are provided in **RLE format** and are decoded on-the-fly inside the notebooks to generate binary segmentation masks.

---

## Dataset

- **Dataset:** Easy Portrait Dataset  
- **Task:** Binary face segmentation  
- **Annotation Format:** Run-Length Encoding (RLE)

> ⚠️ The dataset is **not included** in this repository.  
> Please download it separately and update the dataset paths inside the notebooks.

---

## Notebooks

| Notebook | Description |
|--------|-------------|
| `unet_face_segmentation.ipynb` | Face segmentation using U-Net with RLE-decoded masks |
| `deeplabv3_face_segmentation.ipynb` | Face segmentation using DeepLabV3 with RLE-decoded masks |

Each notebook includes:
- RLE mask decoding
- Data preprocessing
- Model architecture definition
- Training and validation
- Evaluation and qualitative visualization

---

## Models

### U-Net
- Encoder–decoder architecture with skip connections
- Trained from scratch
- Strong performance on fine-grained boundaries

### DeepLabV3
- Atrous convolution-based semantic segmentation
- ASPP module for multi-scale context aggregation
- Superior global context understanding

---

## Mask Encoding (RLE)

Segmentation masks are stored using **Run-Length Encoding (RLE)** and decoded into binary masks before being used for training and evaluation.

Using RLE:
- Reduces annotation storage size
- Is standard in many segmentation datasets and challenges
- Enables efficient mask handling

---

## Evaluation Metric

- **RLE Score** (higher is better)

---

## Results

| Model     | RLE Score |
|-----------|-----------|
| U-Net     | **0.9371** |
| DeepLabV3 | **0.9875** |

DeepLabV3 significantly outperforms U-Net, demonstrating the advantage of atrous convolution and multi-scale context aggregation for face segmentation on portrait images.

---


jupyter notebook
