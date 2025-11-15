# SegDINO_medical
# SegDINO-Medical: Transformer-Based Image Segmentation

This repository contains a simple and effective implementation of a **SegDINO-inspired image segmentation model** using a pretrained **Vision Transformer (ViT-B/16)**. The goal of this project is to perform **binary segmentation** using multi-scale transformer features combined with a lightweight decoder.

The model was trained and tested on the **Face Mask Segmentation Dataset** from Kaggle and achieves strong performance even with a small dataset.

---

## 🚀 Features
- Uses **pretrained ViT-B/16** as a frozen backbone  
- Extracts multi-scale features from layers **2, 5, 8, 11**  
- Lightweight decoder for fast and efficient segmentation  
- Designed for **Colab GPU (T4)**  
- Achieved **Dice Score: 0.7992**  

---

## 📁 Dataset
The project uses the Kaggle Face Mask Segmentation dataset.  
Images and masks must be stored in:


Filenames of images and masks should match.

---

## 🧠 Model Overview
- ViT backbone extracts patch-based global features  
- Decoder projects, reshapes, upsamples, and fuses multi-scale features  
- Final 1×1 convolution produces pixel-wise segmentation mask  

---

## 🛠 Usage

### 1️⃣ Clone the repository
```bash
git clone https://github.com/swethavasireddi12/SegDINO_medical.git
cd SegDINO_medical
pip install -r requirements.txt
Train the model (Colab recommended)

Open training.ipynb and run all cells.

4️⃣ Run inference

Use inference.ipynb to test the model on new images.
