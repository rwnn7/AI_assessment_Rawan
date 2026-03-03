# Robust Road Object Detection under Adverse Conditions

## Overview

This project implements a YOLOv8-based object detector for four road-relevant classes:

- Person  
- Car  
- Truck  
- Traffic Light  

The objective is to evaluate and improve model robustness under adverse visual conditions such as low illumination, noise, and motion blur.

---

## Methodology

1. **Baseline Model**
   - YOLOv8n (pretrained)
   - 640×640 input size
   - 50 epochs
   - Default training configuration

2. **Synthetic Adverse Test Set**
   A degraded version of the clean test set was generated using:
   - Brightness/contrast shifts  
   - Gamma correction  
   - Random shadows  
   - Gaussian noise  
   - Motion blur  

3. **Robust Model (robust_v2)**
   Trained with stronger augmentations:
   - HSV color shifts  
   - Translation & scaling  
   - Mosaic & Mixup  
   - Horizontal flipping  

---

## Results

| Model     | mAP50 (Clean) | mAP50 (Adverse) |
|------------|---------------|-----------------|
| Baseline   | 0.4159        | 0.3023          |
| Robust_v2  | 0.4078        | 0.2655          |

Both models show performance degradation under adverse conditions.  
The robustness-enhanced model maintains comparable clean performance while slightly improving localization quality (mAP50-95).

Full analysis is available in the report.

---

## How to Run

Install dependencies:
pip install -r requirements.txt
Then open and run:
notebook.ipynb

The notebook includes:
- Training (baseline & robust)
- Adverse test generation
- Evaluation
- Visualization

---

## Environment

- Python 3.9  
- PyTorch 2.6  
- Ultralytics YOLOv8  
- Trained on Apple M2 CPU  

---

## Report

See:  
`Road_Object_Detection_Robustness_Report.docx`

For detailed methodology, evaluation analysis, and future work.
