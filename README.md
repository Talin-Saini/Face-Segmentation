# Face Segmentation on Easy Portrait Dataset using U-Net and DeepLabV3

This repository contains Jupyter Notebook implementations for **face segmentation** on the **Easy Portrait dataset** using **U-Net** and **DeepLabV3**.  
The project uses **Run-Length Encoding (RLE)** for mask representation and decoding during training and evaluation.

---

## Overview

Face segmentation is a pixel-wise classification task where each pixel is labeled as **face** or **background**.  
This project compares a classical encoder–decoder network (**U-Net**) with a modern semantic segmentation model (**DeepLabV3**) for accurate face region segmentation in portrait images.

Mask annotations provided in **RLE format** are decoded on-the-fly inside the notebooks to generate binary segmentation masks.

---

## Dataset

- **Dataset:** Easy Portrait Dataset  
- **Task:** Binary face segmentation  
- **Annotation Format:** Run-Length Encoding (RLE)

> ⚠️ The dataset is not included in this repository.  
> Please download it separately and update the dataset path inside the notebooks.

---

## Notebooks

| Notebook | Description |
|--------|-------------|
| `unet_face_segmentation.ipynb` | Face segmentation using U-Net with RLE-decoded masks |
| `deeplabv3_face_segmentation.ipynb` | Face segmentation using DeepLabV3 with RLE-decoded masks |

Each notebook includes:
- RLE mask decoding
- Data preprocessing and augmentation
- Model definition
- Training and validation
- Evaluation using standard segmentation metrics
- Visualization of predictions

---

## Models

### U-Net
- Encoder–decoder architecture with skip connections
- Trained from scratch
- Suitable for precise boundary segmentation

### DeepLabV3
- Atrous convolution-based segmentation
- ASPP module for multi-scale context
- Optional pretrained backbone

---

## Mask Encoding

Ground truth segmentation masks are stored using **Run-Length Encoding (RLE)**.  
RLE strings are decoded into binary masks before being fed into the segmentation models.

This approach:
- Reduces storage size
- Is commonly used in segmentation challenges and datasets
- Allows efficient mask reconstruction during training

---

## Evaluation Metrics

- Intersection over Union (IoU)
- Dice Coefficient
- Pixel Accuracy

---

## Results

| Model     | IoU  | Dice | Pixel Accuracy |
|-----------|------|------|----------------|
| U-Net     | XX.X | XX.X | XX.X           |
| DeepLabV3 | XX.X | XX.X | XX.X           |

Qualitative results and prediction visualizations are available within the notebooks.

---

## Requirements

Typical dependencies:
- Python 3.x
- PyTorch
- torchvision
- numpy
- matplotlib
- opencv-python
- tqdm

---

## Usage

Open and run the notebooks sequentially:
```bash
jupyter notebook
