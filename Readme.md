

# Glaucoma Detection using Deep Learning

This project presents a deep learning–based approach for automated detection of **Glaucoma** from retinal fundus images. The model uses transfer learning with **EfficientNet-B0** to classify images as **glaucoma** or **normal**.

The system achieves **98% accuracy** and **0.999 ROC-AUC**, demonstrating strong performance for automated screening and early glaucoma detection.

---

# Project Overview

Glaucoma is one of the leading causes of irreversible blindness worldwide. Early diagnosis is critical for preventing vision loss. This project applies **deep learning and computer vision techniques** to automatically analyze retinal fundus images and assist in glaucoma screening.

The model is trained using transfer learning and evaluated using standard machine learning metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* ROC Curve
* ROC-AUC Score

---

# Model Architecture

The system uses **transfer learning** with EfficientNet-B0:

* Pretrained on ImageNet
* Final classifier modified for **binary classification**
* Sigmoid activation for probability output

**Loss Function**

* Binary Cross Entropy with Logits

**Optimizer**

* Adam optimizer

---

# Dataset Structure

The dataset follows the standard folder structure used by PyTorch:

```
dataset/
│
├── train/
│   ├── glaucoma/
│   └── normal/
│
├── val/
│   ├── glaucoma/
│   └── normal/
│
└── test/
    ├── glaucoma/
    └── normal/
```

Each folder contains retinal fundus images belonging to the respective class.

---

# Data Preprocessing

Images are preprocessed using the following steps:

* Resize to **224 × 224**
* Random horizontal flip
* Random rotation
* Image normalization (ImageNet statistics)

These transformations help improve model generalization.

---

# Training Details

| Parameter     | Value             |
| ------------- | ----------------- |
| Model         | EfficientNet-B0   |
| Epochs        | 10                |
| Batch Size    | 32                |
| Optimizer     | Adam              |
| Learning Rate | 0.0001            |
| Loss Function | BCEWithLogitsLoss |

---

# Evaluation Metrics

The model performance is evaluated using:

* **Classification Report**
* **Confusion Matrix**
* **ROC Curve**
* **ROC-AUC Score**
* **Training Loss Curve**
* **Training Accuracy Curve**

Example results:

| Metric    | Score |
| --------- | ----- |
| Accuracy  | 0.98  |
| ROC-AUC   | 0.999 |
| Precision | ~0.98 |
| Recall    | ~0.97 |

---

# Visualizations

The project generates the following plots:

* Training Loss Curve
* Training Accuracy Curve
* Confusion Matrix
* ROC Curve

These help analyze model performance and classification behavior.

---




# Technologies Used

* Python
* PyTorch
* Torchvision
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

---

# Future Improvements

* Multi-class glaucoma severity classification
* Integration with clinical decision support systems
* Larger ophthalmology datasets
* Explainable AI (Grad-CAM visualization)

---

# License

This project is intended for **research and educational purposes**.

---
