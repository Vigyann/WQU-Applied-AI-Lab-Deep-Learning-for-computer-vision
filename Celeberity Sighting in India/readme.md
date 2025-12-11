# 🎬 Celebrity Sighting in India  
### Deep Learning–Based Face Detection & Recognition Using MTCNN & Inception-ResNet V1

This project focuses on building an end-to-end deep learning pipeline capable of detecting and recognizing celebrities from images and video frames captured in India. The system uses **MTCNN** for face detection and **Inception-ResNet V1** for face recognition, enabling accurate identification of known personalities even in crowded or real-world scenarios. The project covers data exploration, face detection, face recognition, and deployment through a Flask API.

---

## 📁 Project Structure

├── data-exploration.ipynb (Initial exploration of images and frames)
├── face-detection.ipynb (Face detection using MTCNN)
├── face-recognition.ipynb ( Feature extraction & celebrity identification)
├── flask-api.ipynb ( API workflow for serving results)
└── README.md


---

##  Overview of the System

The workflow involves four major components:

### **1. Data Exploration**
Exploring the collected images and extracted video frames, checking quality, resolution, variations in lighting, angles, and facial visibility. This step ensures understanding of the dataset and prepares frames for further processing.

### **2. Face Detection**
Using **MTCNN (Multi-task Cascaded Convolutional Neural Network)**, the system performs:

- Detection of all faces present in an image or frame  
- Generation of bounding boxes  
- Prediction of detection probabilities  
- Extraction of facial landmarks (eyes, nose, mouth)  

This detection step is critical as it isolates relevant facial regions while filtering out non face objects, enabling efficient downstream processing for recognition.

### **How MTCNN Works**
MTCNN uses a **three-stage cascaded pipeline**:

- **P-Net (Proposal Network):** Quickly scans the image to propose potential face regions.  
- **R-Net (Refine Network):** Refines these candidate regions by removing false positives and improving bounding box accuracy.  
- **O-Net (Output Network):** Produces the final bounding boxes, face probabilities, and facial landmarks with higher precision.

The network simultaneously performs classification (face vs. non face), bounding box regression, and landmark regression, making it highly efficient and accurate for real world applications like celebrity detection.

---

##  Face Recognition

The face recognition component uses **Inception-ResNet V1**, pretrained on the VGGFace2 dataset. This model generates **128-dimensional embeddings** for each detected face. The workflow involves:

- Creating an embedding database using known celebrity images  
- Extracting face embeddings for each new frame  
- Computing similarity scores between new embeddings and stored embeddings  
- Identifying the closest match based on distance thresholds  

This embedding based approach ensures robustness to variations in lighting, pose, angle, and mild occlusions.

---

##  Multi Person Recognition

The pipeline supports recognizing multiple celebrities within a single image or video frame. Each detected face is evaluated independently, matched with stored embeddings, and labeled appropriately. Unknown individuals are marked as "Unrecognized" based on a configurable threshold.

---

##  Flask API Integration

A lightweight **Flask API** is included to operationalize the model, allowing:

- Image uploads via REST endpoints  
- Automatic face detection and recognition  
- Returning processed results including recognized identities and confidence scores  

This enables real-time celebrity sighting applications, mobile integrations, and scalable deployments.

---

##  Technologies & Libraries

This project uses the following major libraries and tools:

- **Python**
- **PyTorch**
- **Torchvision**
- **facenet-pytorch** (MTCNN & Inception-ResNet models)
- **Pillow (PIL)**
- **Matplotlib**
- **Flask** (for deployment)

---

##  Key Features

- Accurate face detection using MTCNN  
- Landmark extraction for finer detail and preprocessing  
- Embedding based face recognition using Inception-ResNet V1  
- Support for multi person detection and recognition  
- Handling of real world variations (lighting, angles, crowd)  
- Flask API for scalable use  
- Modular structure with clear separation between detection, recognition, and deployment  

---

##  Applications

- Celebrity spotting from events, airports, media clips  
- Automated tagging of personalities in video content  
- Crowd-analysis systems  
- Face-based search engines for entertainment media  
- Real-time face recognition for security or monitoring systems  

---

##  Conclusion

This project demonstrates a complete deep learning solution for face detection and celebrity recognition in Indian contexts. By combining MTCNN’s robust face detection capabilities with the powerful representation learning of Inception-ResNet V1, the system achieves high accuracy in challenging, real-world scenarios. The included API ensures that the solution is ready for practical deployment and further expansion.

---
