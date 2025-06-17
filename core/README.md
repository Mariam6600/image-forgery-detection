# Image Forgery Detection using Deep Learning

This project detects forged images using a dual-input convolutional neural network that analyzes both RGB and Error Level Analysis (ELA) representations to uncover manipulation traces.

## 📁 Dataset
- CASIA 2.0 Image Tampering Dataset

## 🧠 Model Architecture
The architecture consists of:
- **Dual ResNet50V2 inputs**: One for RGB, one for ELA.
- **Shared Dense classification head** with BatchNorm & Dropout for robustness.

## 📈 Training & Performance

### Stage 1: Head Training
- ResNet50V2 layers frozen.
- Results:
  - Accuracy: **86.17%**
  - AUC: **0.9468**
  - Forged Recall: **89.37%**

### Stage 2: Fine-Tuning
- Unfrozen top ResNet50V2 layers.
- Learning Rate: `5e-6`
- Improved Accuracy: **87.88%**

## 🚀 How to Run
- Open the notebook in **Google Colab**
- Run all cells sequentially
- ELA images are generated automatically from RGB
