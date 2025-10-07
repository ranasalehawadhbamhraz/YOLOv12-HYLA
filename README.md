# Yemeni-Coffee-Beans-Detection
YOLOv12-HYLA: YOLOv12-based model for detecting Yemeni coffee beans maturity levels.

This repository contains the code and model configuration used in the paper:
**"YOLOv12-HYLA: A Hybrid Learnable Attention Architecture Leveraging Fixed-Learnable Weights for Enhanced Coffee Bean Detection"**

## Overview
e propose YOLOv12-HYLA, a hybrid learnable object detection framework tailored for real-time coffee bean maturity assessment. YOLOv12-HYLA integrates ACmix Fixed-weight modules for stable multi-scale feature fusion and SECBAM Learnable-weight module for adaptive channel–spatial attention refinement.

## Dataset
The dataset is publicly available on Kaggle:
👉 [Yemeni Coffee Beans Dataset](www.kaggle.com/datasets/ranasalehbamhraz2/yemeni-coffee-beans-dataset)

## Model Training
Training was performed with:
- Image size: 1280
- Epochs: 200
- Data Split: (70, 20, 10)
- Split: 1540 train / 443 val / 207 test   
- Epochs: 200                 
- Batch Size: 4 
- Image Size: (1280, 1280)
- cosine learning rate scheduler: Enabled
- Optimizer: AdamW
- Warmup epochs: 3
- Warmup epoch: 0.2

## Detection Results

| Metric | YOLOv8s | YOLOv9s | YOLOv10s | YOLOv11s | YOLOv12s | YOLOv12-HYLA |
|--------|---------|---------|----------|----------|----------|---------------|
| Precision (%) | 85.3 | 88.6 | 86.3 | 89.7 | 89.7 | **91.6** |
| Recall (%) | 88.0 | 87.8 | 86.1 | 87.7 | 88.9 | **89.6** |
| F1-score | 0.8663 | 0.8820 | 0.8619 | 0.8869 | 0.8926 | **0.9058** |
| mAP@0.5 (%) | 91.6 | 92.3 | 91.8 | 92.1 | 93.1 | **94.8** |
| mAP@0.5:0.95 (%) | 71.4 | 72.8 | 69.3 | 73.2 | 72.6 | **74.1** |
| Preprocess Time (ms) | 0.8 | 1.8 | 1.5 | 2.8 | 1.3 | 1.7 |
| Inference Time (ms) | 9.2 | 16.6 | 15.4 | 14.0 | 17.0 | 15.3 |
| Postprocess Time (ms) | 1.5 | 1.2 | 0.4 | 1.5 | 1.6 | 1.1 |
| Total Time (ms) | 11.5 | 19.6 | 17.3 | 18.3 | 19.9 | 18.1 |
| FPS | 108.70 | 60.24 | 64.94 | 71.43 | 58.82 | 65.36 |
| FLOPs (G) | 28.4 | 26.7 | 21.4 | 21.3 | 21.2 | 22.4 |

## Countin Error Metrics Results

| Model | RMSE | MAE |
|-------|------|-----|
| YOLOv8s | 2.4635 | 1.5686 |
| YOLOv9s | 2.2174 | 1.3382 |
| YOLOv10s | 2.4872 | 1.5588 |
| YOLOv11s | 2.2980 | 1.3793 |
| YOLOv12s | 2.5173 | 1.4000 |
| YOLOv12-HYLA | **2.0111** | **1.2956** |


## Citation
If you use this code or dataset, please cite:
> R. S. Bamhraz (2025). YOLOv12-HYLA: A Hybrid Learnable Attention Architecture Leveraging Fixed-Learnable Weights for Enhanced Coffee Bean Detection . GitHub. https://github.com/ranabamhraz/Yemeni-Coffee-Beans-Detection

## License
Code released under the [MIT License](LICENSE).
Dataset licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

