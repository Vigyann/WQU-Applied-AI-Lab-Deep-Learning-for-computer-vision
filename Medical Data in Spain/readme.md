# Medical Data Generation in Spain – Synthetic Medical Imaging Using GANs & MediGAN

This project focuses on generating **realistic synthetic medical images** (X-ray and MRI) using a combination of **custom built Generative Adversarial Networks (GANs)** and **fine tuned MediGAN models**. The goal is to support healthcare AI research teams in Spain by enabling privacy preserving dataset expansion while complying with strict EU/GDPR medical data regulations.

---

##  Project Overview

The objective of this project is to build a full synthetic image generation pipeline that:

- Generates **synthetic X-ray and MRI images** using GANs built from scratch in PyTorch.
- Fine tunes **MediGAN**, a specialized medical image generation model.
- Deploys a **Streamlit based application** to generate synthetic medical images on demand.
- Ensures complete patient anonymity while supporting model training, experimentation, and augmentation.

This project aims to enhance medical imaging datasets without exposing sensitive medical records.

---

##  Motivation

Healthcare datasets are difficult to collect and share due to:

- Strict GDPR guidelines on patient privacy  
- Limited access to labelled diagnostic datasets  
- Ethical concerns regarding identifiable patient imagery  

Synthetic data provides a safe alternative by generating image samples that preserve structural medical patterns **without containing real patient information**.

---

##  Dataset

- Anonymized **X-ray** and **MRI** sample images.
- Preprocessing steps:
  - Conversion to **grayscale**
  - Resizing to **64 × 64**
  - Normalization and tensor conversion
- Loaded using **PyTorch ImageFolder** and `DataLoader`.

---

##  Libraries Used

- **PyTorch**, **Torchvision**  
- **NumPy**, **PIL**, **Matplotlib**  
- **Streamlit** for deployment  
- `datetime`, `os`, `pathlib`, `tqdm` for utilities and workflow  
- GitHub for version control and collaboration

---

##  How GANs Work (Generative Adversarial Networks)

GANs consist of two neural networks that train in opposition:

### **1. Discriminator**
A binary classifier that decides whether an image is **real** or **synthetic**.

- Input: Flattened 1×64×64 image  
- Architecture:
  - Linear layers: **4096 → 1024 → 512 → 256 → 1**
  - Activation: **LeakyReLU (negative_slope = 0.25)**
  - Output activation: **Sigmoid**  
- Goal: Improve at detecting fake images.

### **2. Generator**
Creates synthetic images from noise vectors (latent dimension = 128).

- Upsampling using **Linear → BatchNorm1d → LeakyReLU**  
- Final activation: **Tanh**
- Output reshaped using **Unflatten** to 1×64×64  
- Goal: Fool the discriminator by creating realistic medical images.

### **Training Cycle**
Each batch involves:

1. Training discriminator on **real** images  
2. Training discriminator on **fake** images  
3. Training generator to **fool** the discriminator  
4. Checkpointing models after each epoch  
5. Saving generated sample images  

Both networks use the **AdamW** optimizer with tuned `lr` and `betas`.

---

##  MediGAN ( Domain Specialized Medical Image Generator )

MediGAN is a generative model designed specifically for medical imaging.  
Unlike standard GANs, MediGAN:

- Uses loss functions tailored for pixel level clarity  
- Produces modality consistent outputs (e.g., chest X-rays, brain MRIs)  
- Generates structurally accurate medical images  
- Achieves significantly higher realism

In this project, MediGAN was **fine-tuned** on anonymized Spanish medical data samples to further improve modality specific realism.

---

## Output Evaluation

Model outputs were evaluated using:

- Visual sample grids  
- Pixel intensity distribution analysis  
- Generator/discriminator loss curves  
- Sharpness and structural consistency checks  

### Sample Synthetic Output  
![Synthetic Sample 1](https://raw.githubusercontent.com/Vigyann/WQU-Applied-AI-Lab-Deep-Learning-for-computer-vision/main/Medical%20Data%20in%20Spain/ss.png)


---

##  Streamlit App - Interactive Synthetic Image Generator

A **Streamlit interface** was developed to:

- Select imaging modality (X-ray / MRI)
- Choose model:
  - Custom GAN  
  - Fine-tuned MediGAN  
- Generate synthetic images instantly  
- View and download generated samples  

This enables medical researchers to experiment with synthetic data without requiring coding experience.


---

##  Key Outcomes

- A fully functional **synthetic medical image generator**  
- GAN & MediGAN models working end to end  
- Streamlit based image generation tool  
- 100% anonymized, privacy preserving dataset creation  
- High quality images suitable for dataset augmentation and AI research  

---

##  Future Improvements

- Upgrade to diffusion models (e.g., Stable Diffusion Medical)  
- Increase resolution (128×128 → 512×512)  
- Add anomaly synthesis (tumors, lesions, abnormalities)  
- Add evaluation metrics  

---

##  Support the Project

If you find this project valuable, **please drop a ⭐ on GitHub** 

---


