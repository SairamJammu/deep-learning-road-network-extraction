# deep-learning-road-network-extraction
Deep learning–based road network extraction from high-resolution aerial imagery using U-Net, DeepLabV3+, PSPNet, and FPN.

This project presents a comparative evaluation of deep learning–based semantic segmentation models
for automated road network extraction from high-resolution aerial imagery.

## Problem Context (GIS + Computer Vision)
Accurate road network extraction is critical for:
- GIS mapping and cartography
- Urban planning and smart cities
- Autonomous navigation
- Emergency response and disaster management

Manual digitization and rule-based methods do not scale. This project evaluates deep learning
architectures for pixel-level road segmentation under extreme class imbalance.

## Models Evaluated
- U-Net
- DeepLabV3+
- PSPNet
- Feature Pyramid Network (FPN)

## Dataset
- Massachusetts Roads Dataset (HDR aerial imagery)
- ~1,171 image–mask pairs
- Severe class imbalance (~5% road pixels)
- Original resolution: 1500×1500 TIFF images

## Methodology
- Image tiling and resizing to 256×256
- Data augmentation (rotation, flips, brightness, noise)
- Weighted BCE + Dice Loss
- Identical training pipeline for all models

## Key Results
- **U-Net achieved best performance**
  - IoU: 0.2954
  - F1-score: 0.4556
  - Inference speed: ~1549 FPS
- Skip connections preserved thin road topology better than deeper architectures

## Tools & Technologies
- Python, PyTorch
- Semantic segmentation
- GIS & remote sensing concepts
- High-resolution aerial imagery
- Model evaluation (IoU, F1, Precision, Recall)

## Deliverables
- 📄 Full technical report (PDF)
- 📊 Final presentation
- 📓 Training notebook
- 🖼️ Qualitative prediction visualizations

## Author
Sairam Jammu  
Kent State University – MS Business Analytics
