Robust Object Detection with YOLOv8 (ROAD4)

This project trains a baseline YOLOv8 object detection model and improves robustness under adverse visual conditions using synthetic data augmentation and fine-tuning.

The dataset is derived from a small subset of COCO128, keeping only four classes: person, car, truck, and traffic light. The goal is to evaluate model performance on clean images versus adverse conditions.

The repository contains three files. The notebook **robust_yolov8_road4.ipynb** includes the full pipeline for dataset preparation, training, evaluation, and robustness analysis. The file **requirements.txt** lists the Python dependencies needed to run the project. The **README.md** provides a brief project description and instructions.

To run the project, first install the dependencies using: `pip install -r requirements.txt`. Then open the notebook **robust_yolov8_road4.ipynb** and run all cells.

The notebook automatically loads COCO128, creates the ROAD4 clean dataset, generates an adverse test set using image degradations (brightness/contrast changes, gamma shifts, noise, motion blur, and JPEG compression), trains a baseline model, fine-tunes a robust model using augmented data, and evaluates both models on clean and adverse test sets using Precision, Recall, mAP50, and mAP50–95.

For reproducibility, a fixed random seed and deterministic settings are used where possible. The dataset and training outputs are not stored in the repository and are automatically generated when running the notebook.
