## Dataset Information

This project uses the **Massachusetts Roads Dataset** from Kaggle for supervised road network extraction from aerial imagery.

### Dataset Source

- Kaggle: Massachusetts Roads Dataset
- Author: balraj98
- Link: https://www.kaggle.com/datasets/balraj98/massachusetts-roads-dataset

### Dataset Description

- High-resolution aerial images of Massachusetts
- Corresponding binary road segmentation masks
- Task: pixel-wise road extraction using semantic segmentation
- Approximate project split: train, validation, and test image-mask folders
- Road pixels represent roughly 4.89% of total pixels, so the dataset is strongly imbalanced

### Download Method

The dataset was downloaded programmatically using the Kaggle API:

```bash
kaggle datasets download -d balraj98/massachusetts-roads-dataset --unzip
```

The full dataset and model checkpoints are not committed to this repository because the source imagery is several GB and should be downloaded directly from Kaggle when reproducing the project.
