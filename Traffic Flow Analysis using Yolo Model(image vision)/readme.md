
# 🚦 Traffic Analysis with YOLO & Real-Time Video Processing 

##  Project Overview
This project is focused on **Traffic Flow Analysis** in collaboration with **WQU**, leveraging the **YOLO (You Only Look Once)** model for real-time object detection in traffic surveillance videos.

The objective is to **analyze traffic patterns** and **optimize traffic flow** using **real-time video analytics**, by detecting objects like cars, buses, bikes, and pedestrians from every frame.

---

##  How YOLO Detects Objects

- **Grid-Based Detection**: YOLO divides an image into S×S grids (e.g., 4×4), each predicting bounding boxes and confidence scores.
- **Fast Inference**: YOLO uses a single convolutional neural network to process the entire image at once, enabling processing of 150+ FPS.
- **Efficient Detection**: Each grid cell predicts bounding boxes and object classes for fast and accurate detection.

---

##  Key Highlights

-  Used **XML-based datasets** for bounding box annotation — my first time with this format.
-  Clarified the difference between image classification and object detection:
  - **Image Classification**: What is in the image.
  - **Object Detection**: What + Where= via bounding boxes.

---

##  Project Objectives

1. Capture each frame from a video stream.
2. Detect and annotate traffic objects (cars, buses, pedestrians, etc.).
3. Display object labels with confidence scores.
4. Combine annotated frames back into a video for visualization.

---

##  Transfer Learning with YOLO

- Fine-tuned a **pre-trained YOLO model** on a custom traffic dataset.
- **Transfer learning** helped speed up convergence and improve detection accuracy.

---

##  Loss Functions in Object Detection

- **Classification Loss**: Handled using cross-entropy to detect correct object type.
- **Bounding Box Loss**: YOLO uses **CIoU (Complete IoU)** to improve box accuracy.
- **Focal Loss**: Used in imbalanced datasets to emphasize difficult examples.

---

## Data Augmentation Techniques

To combat limited labeled data, applied various augmentations:
- Flipping, rotation, scaling, and color adjustments.
- Leveraged YOLO's built-in augmentation tools to improve **generalization** and reduce **overfitting**.

---

##  Libraries Used

| Library | Use Case |
|--------|----------|
| `pathlib`, `os`, `shutil` | File and folder operations |
| `xml.etree.ElementTree` | Parsing XML for annotation |
| `pandas`, `matplotlib`, `PIL` | Data handling and visualization |
| `torch` | PyTorch backend for YOLO |
| `ultralytics`, `YOLO` | YOLO model training and inference |
| `tqdm`, `IPython.display` | Progress tracking and notebook display tools |

---

## ✅ Outcomes

The system can now:
- Detect objects in real-time videos.
- Annotate bounding boxes and object types accurately.
- Generate processed video outputs for traffic pattern insights.

This project provides a foundation for **smart city traffic monitoring**, **congestion analysis**, and **road safety planning**.

---

🔗 **Model**: YOLOv8 by Ultralytics  
🧪 **Framework**: PyTorch + Ultralytics  
🎥 **Input**: Real-time or recorded traffic video  
📁 **Annotations**: XML-based bounding boxes  

---



