# Deep Learning Road Network Extraction

Portfolio summary for a semantic segmentation project focused on extracting road networks from high-resolution aerial imagery. The project compares multiple deep learning architectures and frames the work through a GIS and remote-sensing lens.

## Portfolio Summary

Manual road digitization is slow and difficult to scale. This project evaluates whether deep learning segmentation models can identify road pixels from aerial imagery while handling thin road structures and severe class imbalance.

This repository currently preserves the project overview and dataset notes. Large training artifacts, source imagery, model checkpoints, and generated outputs are intentionally not stored in GitHub because of size and reproducibility constraints.

## Problem Context

Accurate road network extraction supports:

- GIS mapping and cartography
- Urban planning and smart-city analysis
- Autonomous navigation support datasets
- Emergency response and disaster management

## Data

- Massachusetts Roads Dataset
- Approximately 1,171 image-mask pairs
- Original image size: 1500 x 1500 TIFF imagery
- Road pixels represent a small share of each image, creating class imbalance

## Methods

Models evaluated:

- U-Net
- DeepLabV3+
- PSPNet
- Feature Pyramid Network (FPN)

Workflow:

- Tile and resize imagery to 256 x 256 patches
- Apply augmentation including rotations, flips, brightness changes, and noise
- Train with weighted BCE + Dice loss
- Compare models using IoU, F1-score, precision, recall, and inference speed

## Results

U-Net produced the strongest result in this experiment:

| Model | Best Reported Result |
| --- | --- |
| U-Net | IoU 0.2954, F1-score 0.4556, approximately 1549 FPS inference |

The result suggests that skip connections help preserve thin road topology better than deeper architectures in this project setup.

## Tools

Python, PyTorch, semantic segmentation, aerial imagery, GIS concepts, model evaluation.

## Repository Contents

| Path | Purpose |
|---|---|
| `README.md` | Project summary, methods, results, and portfolio framing |
| `data/README.md` | Dataset source, download method, and data-use notes |

## Recommended Next Repository Additions

To make the repository fully reproducible, the next version should add:

- A cleaned training notebook or script
- Environment setup instructions
- Metric tables for all evaluated architectures
- Qualitative prediction examples
- Links to the final report or presentation if the files are too large for GitHub

## Portfolio Value

This project demonstrates applied geospatial AI: turning imagery into structured infrastructure information, comparing model tradeoffs, and documenting results in a way that connects computer vision metrics to GIS use cases.

## Author

Sairam Jammu  
M.S. Business Analytics, Kent State University
