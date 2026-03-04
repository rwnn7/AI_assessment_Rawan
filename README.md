# Improving YOLOv8 Object Detection Robustness Under Adverse Visual Conditions

This project trains a baseline YOLOv8 object detection model and improves robustness under adverse visual conditions using synthetic data augmentation and fine-tuning.

The dataset is derived from a subset of COCO128 and includes four classes: person, car, truck, and traffic light. The objective is to compare model performance on clean images versus images affected by adverse visual conditions.

The repository contains three files: **AI_assessment_Rawan.ipynb**, which includes the full pipeline for dataset preparation, training, and evaluation; **requirements.txt**, which lists the required Python dependencies; and **README.md**, which provides project instructions.

To run the project, install the dependencies using `pip install -r requirements.txt`, then open **robust_yolov8_road4.ipynb** and run all cells.

The notebook automatically prepares the dataset, generates an adverse test set using image degradations (e.g., brightness/contrast changes, noise, blur, and compression), trains a baseline model, fine-tunes a robust model with augmented data, and evaluates both models on clean and adverse test sets using Precision, Recall, mAP50, and mAP50-95.

A fixed random seed and deterministic settings are used where possible to support reproducibility. The dataset and training outputs are generated automatically when the notebook is executed.

