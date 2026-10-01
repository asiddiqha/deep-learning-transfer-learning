# Deep Learning Transfer Learning

A portfolio repository demonstrating **transfer learning, feature extraction, fine-tuning, and pretrained-model inference** across multiple computer-vision tasks and architectures.

The projects progress from task-specific image classification using VGG16 to transfer learning with MobileNetV2 and pretrained ImageNet inference with ResNet50.

## Projects

### 01 — Cats vs Dogs

Binary image classification using **VGG16 pretrained on ImageNet**.

- Feature extraction with a frozen convolutional base
- Selective fine-tuning from `block5_conv1`
- Comparison of feature extraction and fine-tuning workflows

**Architecture:** VGG16  
**Task:** Binary image classification

---

### 02 — Emotion Detection

Seven-class facial emotion classification using **FER2013** and VGG16.

- Feature extraction using pretrained VGG16
- Selective fine-tuning from `block5_conv1`
- Multi-class facial emotion classification

**Architecture:** VGG16  
**Dataset:** FER2013  
**Task:** 7-class image classification

---

### 03 — MobileNetV2 ImageNet Transfer Learning

Multi-class mammal image classification using **MobileNetV2 pretrained on ImageNet**.

- Transfer learning using ImageNet pretrained weights
- Classification across 45 mammal categories
- Partial fine-tuning of the pretrained network
- Evaluation using training and validation performance

**Architecture:** MobileNetV2  
**Dataset:** 45-class mammal image dataset  
**Task:** Multi-class image classification

---

### 04 — ResNet50 ImageNet Inference

Pretrained image classification using **ResNet50 with ImageNet weights**.

- Loads a pretrained ResNet50 model
- Applies the required image preprocessing
- Generates ImageNet predictions
- Displays the top-3 predicted classes and confidence scores

**Architecture:** ResNet50  
**Dataset:** ImageNet  
**Task:** Pretrained image classification inference

> This project demonstrates pretrained-model inference rather than custom training or fine-tuning.

---

## Project Structure

```text
deep-learning-transfer-learning/
│
├── 01_cats_vs_dogs/
│   ├── 01_feature_extraction.ipynb
│   └── 02_fine_tuning.ipynb
│
├── 02_emotion_detection/
│   ├── 01_feature_extraction.ipynb
│   └── 02_fine_tuning.ipynb
│
├── 03_mobilenetv2_imagenet/
│   └── 01_transfer_learning.ipynb
│
├── 04_resnet50_imagenet/
│   └── 01_pretrained_inference.ipynb
│
├── requirements.txt
└── README.md