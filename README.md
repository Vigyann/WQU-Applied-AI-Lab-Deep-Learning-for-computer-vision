# Applied AI Lab: Deep Learning for Computer Vision  
**Issued by WorldQuant University**  
![Applied AI Lab: Deep Learning for Computer Vision Badge](https://github.com/Vigyann/WQU-Applied-AI-Lab-Deep-Learning-for-computer-vision/raw/main/Screenshot%20(362).png)  

[![View Badge on Credly](https://img.shields.io/badge/View%20Credly%20Badge-FF6F00?style=for-the-badge&logo=credly&logoColor=white)](https://www.credly.com/earner/earned/badge/3029119c-bc74-4c5d-a7d9-55cb667da846)

This repository contains **six end-to-end PyTorch computer vision projects** completed as part of the **Applied AI Lab: Deep Learning for Computer Vision** program by WorldQuant University.  

The projects cover the full deep learning workflow — from **data preparation, cleaning, and transformation pipelines** to mastering **MLPs, CNNs, and Transformers** — while tackling real-world tasks such as **image classification, object detection, and generative AI**.  

We applied **transfer learning**, **self-regulated learning**, and explored leading AI software libraries, while also considering **core values, ethical considerations, and environmental concerns** faced by AI scientists.  

---

## 📂 Projects Overview

### 1. Wildlife Conservation in Côte d'Ivoire  
**Goal:** Assist conservationists in identifying wildlife from **camera trap images** to monitor biodiversity.  
**Dataset:** Wildlife camera trap images, multiple species + empty frames.  
**Approach & Technologies:**  
- Preprocessing images (resizing, normalization, augmentation).  
- Built **Convolutional Neural Networks (CNNs)** for multi-class classification.  
- Used **Transfer Learning** with pre-trained models (ResNet, EfficientNet).  
- Implemented **data augmentation** to improve generalization.  
- Evaluated model with precision, recall, and confusion matrices to handle class imbalance.  
**Outcome:** A robust classifier capable of identifying multiple animal species or detecting empty frames.  

---

### 2. Crop Disease Detection in Uganda  
**Goal:** Detect and classify diseases affecting crops to support local farmers.  
**Dataset:** Cassava leaf disease dataset (5 classes: 4 diseases + healthy).  
**Approach & Technologies:**  
- Built a custom **CNN** architecture in PyTorch.  
- Fine-tuned **MobileNetV2** and **ResNet50** for higher accuracy.  
- Implemented **Callbacks** like EarlyStopping and ReduceLROnPlateau for optimal training.  
- Applied **data augmentation** to handle varied lighting and leaf orientations.  
- Used **cross-entropy loss** with Adam optimizer.  
**Outcome:** Achieved high accuracy for disease classification, providing a potential tool for early intervention.  

---

### 3. Traffic Monitoring in Bangladesh  
**Goal:** Detect and track objects (vehicles, pedestrians) from traffic CCTV feeds for urban planning and traffic law enforcement.  
**Dataset:** Real-world traffic video frames from Dhaka, Bangladesh.  
**Approach & Technologies:**  
- Used **Ultralytics YOLOv8** pre-trained weights for object detection.  
- Extended detection classes to include **custom objects** (rickshaws, buses).  
- Processed video frames in real-time with **OpenCV**.  
- Applied **non-max suppression (NMS)** for precise bounding box detection.  
- Optimized model for GPU inference using PyTorch’s CUDA acceleration.  
**Outcome:** A real-time object detection system capable of identifying traffic patterns and congestion levels.  

---

### 4. Celebrity Sightings in India  
**Goal:** Detect and recognize specific celebrities in images and videos.  
**Dataset:** Video interview of boxer Mary Kom + extracted frames.  
**Approach & Technologies:**  
- Used **MTCNN** for face detection.  
- Generated **face embeddings** with Inception-ResNet (FaceNet).  
- Built a **facial recognition pipeline** to match embeddings with known faces.  
- Developed a **Flask web app** allowing users to upload images for recognition.  
- Optimized for different lighting and angles using embedding distance thresholds.  
**Outcome:** A functional celebrity recognition system deployable as a web service.  

---

### 5. Medical Data Generation in Spain  
**Goal:** Use AI to generate realistic medical imagery for training healthcare AI models without compromising patient privacy.  
**Dataset:** X-ray, MRI sample images (anonymized).  
**Approach & Technologies:**  
- Implemented **Generative Adversarial Networks (GANs)** from scratch.  
- Fine-tuned a **MediGAN** pre-trained model for better output quality.  
- Deployed a **Streamlit app** allowing users to generate synthetic images on demand.  
- Used **PIL** and **Matplotlib** for visualization and quality checks.  
- Version-controlled using **GitHub** for collaborative development.  
**Outcome:** A tool for generating synthetic but realistic medical datasets for research purposes.  

---

### 6. Social Media Marketing in the United States  
**Goal:** Create a meme generator for marketing campaigns using AI-driven image generation.  
**Dataset:** Text + meme template prompts for Stable Diffusion.  
**Approach & Technologies:**  
- Used **HuggingFace Diffusers** to implement **Stable Diffusion**.  
- Built a **Streamlit application** allowing users to enter text prompts and generate memes.  
- Supported multiple meme templates and custom captions.  
- Optimized model for inference speed using mixed precision (`torch.float16`).  
- Integrated **HuggingFace Hub** for sharing generated content.  
**Outcome:** An AI-powered creative tool for content marketing, capable of generating unique visuals in seconds.  

---

## 🛠️ Skills & Technologies
- **Deep Learning**: CNNs, MLPs, Transformers, GANs  
- **Computer Vision**: Image Classification, Object Detection, Image Generation  
- **Libraries & Tools**:  
  - PyTorch, HuggingFace Transformers & Diffusers, Ultralytics YOLOv8  
  - OpenCV, Pandas, NumPy, Scikit-learn, Matplotlib  
  - Flask, Streamlit  
- **Specialized Models**: Facenet, MTCNN, MediGAN, Stable Diffusion  
- **Techniques**: Transfer Learning, Supervised Learning  

---

