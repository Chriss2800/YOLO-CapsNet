# YOLO-CapsNet

## Enhancing Lung Nodule Detection with a YOLO-CapsNet Hybrid Model

This repository was developed as part of a master's thesis exploring the combination of YOLO (You Only Look Once) and Capsule Networks (CapsNet) to enhance lung nodule detection. It includes scripts for dataset preprocessing, model training, and testing, along with comparative evaluations against other approaches.

---

## Repository Structure

### 1. **Dataset Preprocessing**
Scripts for manual preprocessing of datasets:
- **`LIDC_Dataset.ipynb`** – Preprocessing for LIDC dataset.
- **`PET_Dataset.ipynb`** – Preprocessing for PET dataset.

### 2. **CapsNet Training**
Scripts for training the Capsule Network:
- **`Callbacks.py`** – Implements early stopping.
- **`caps_utils.py`** – Utility functions for CapsNet training.

#### **Full Image CapsNet**
- **`caps_normal_model.py`** – Model definition.
- **`caps_normal_train.ipynb`** – Training script.
- **Results:** Stored in `CAPS_CROPPED/weights/caps_normal.pt`

#### **Cropped Image CapsNet**
- **`caps_cropped_model.py`** – Model definition.
- **`caps_cropped_train.ipynb`** – Training script.
- **Results:** Stored in `CAPS_CROPPED/weights/caps_crop_new.pt`

### 3. **YOLO Training**
Scripts for training the YOLO model:
- **`YOLO1_dataset.yaml`** – Dataset configuration.
- **`yolo11m.pt`** – Pre-trained YOLO model weights.
- **`YOLO1_model.ipynb`** – Training script.
- **Results:** Stored in `YOLO1/1/weights/best.pt`

### 4. **Testing & Comparisons**
Evaluation and comparison of different approaches:

#### **1. Cropped Image CapsNet vs. Full Image CapsNet**
- **`test_caps_cropped.ipynb`** – Evaluation of cropped image CapsNet.
- **`test_caps_normal.ipynb`** – Evaluation of full image CapsNet.

#### **2. YOLOv11 + Cropped Image CapsNet vs. Cropped Image CapsNet vs. YOLOv11**
- **`test_caps_cropped.ipynb`** – Evaluation of cropped image CapsNet.
- **`test_complete.ipynb`** – Combined evaluation.

#### **3. YOLOv11 + Cropped Image CapsNet + YOLOv11 vs. YOLOv11**
- **`test_complete.ipynb`** – Final evaluation.

