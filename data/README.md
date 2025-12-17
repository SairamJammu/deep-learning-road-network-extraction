## Dataset Information

This project uses the **Massachusetts Roads Dataset** sourced from Kaggle
for supervised road network extraction from aerial imagery.

### Dataset Source
- Kaggle: Massachusetts Roads Dataset  
- Author: balraj98  
- Link: https://www.kaggle.com/datasets/balraj98/massachusetts-roads-dataset

### Dataset Description
- High-resolution aerial images of Massachusetts
- Corresponding binary road segmentation masks
- Task: Pixel-wise road extraction (semantic segmentation)

### Download Method
The dataset was downloaded programmatically using the Kaggle API:

```bash
kaggle datasets download -d balraj98/massachusetts-roads-dataset
