# 🌿 Crop Disease Detection in Uganda  
**Deep Learning Project | WorldQuant University**

## 📌 Overview

This project focuses on identifying **crop diseases from leaf images** using **deep learning** techniques. Developed in collaboration with **WorldQuant University**, the goal was to build an efficient multi-class image classification system that detects and classifies various plant diseases.

We used **transfer learning** with the **ResNet50** model and implemented a series of **model training callbacks** for efficient and optimized performance.

---

## 🧠 Key Concepts Covered

- **Transfer Learning** (with ResNet50)
- **Computer Vision** (using PyTorch & TorchVision)
- **Data Preprocessing & Augmentation**
- **Multi-class Classification**
- **Callbacks**: Early Stopping, Learning Rate Scheduler, Model Checkpointing
- **Probability Predictions using Softmax**

---

## 🧰 Libraries Used

```python
import matplotlib
import matplotlib.pyplot as plt
import numpy as np
import PIL
import torch
import torchvision
from torch.utils.data import DataLoader, random_split
from torchvision import datasets, transforms
from tqdm.notebook import tqdm
import sklearn.model_selection
import torch.nn as nn
import torch.optim as optim
from sklearn.metrics import ConfusionMatrixDisplay, confusion_matrix
from torchinfo import summary
```

---

## 📊 Dataset Preparation

### Steps:

1. **Dataset Exploration**: Understanding class distributions and folder structure.
2. **Image Transformation**:
   - Convert to **RGB**
   - Resize to **224x224**
   - **Normalize** using ImageNet means and std
3. **Split** into training and validation datasets.
4. **Batching** using PyTorch’s `DataLoader`.

---

## 🏗️ Model Architecture

- Built a **Convolutional Neural Network (CNN)** for multi-class classification.
- Used **Transfer Learning** with **ResNet50** pre-trained on ImageNet.
- Replaced the final classification layer to match the number of crop disease classes.

---

## ⚙️ Callbacks Used During Training

We used the following **callbacks** to optimize training:

1. **Early Stopping**  
   Stops training if validation loss doesn't improve for 5 consecutive epochs (to prevent overfitting).

2. **Learning Rate Scheduling**  
   Reduces learning rate as training progresses to refine the model.

3. **Model Checkpointing**  
   Saves the model every time the validation loss improves, ensuring we retain the best model.

---

##  Predicting Image Probabilities

We created a function `file_to_confidence()` to predict the **class probabilities** for a given image:

### final Steps:

1. **Open the image**.
2. Apply the **same transformation pipeline** used during training.
3. **Unsqueeze** image tensor to make it 4D: `1 x 3 x 224 x 224` as the model expects batches.
4. Move image to the appropriate **device (CPU/GPU)**.
5. **Predict** and pass output through **Softmax** to convert raw logits to **probabilities**.
6. Convert results to a **DataFrame** for readability.

---







Feel free to ⭐️ the repo or reach out for collaboration! 🌱

