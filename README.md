# Deep Learning Transfer Learning with VGG16

A portfolio project demonstrating **transfer learning, feature extraction, and selective fine-tuning** with VGG16 across two computer-vision tasks.

## Projects

### 01 — Cats vs Dogs
Binary image classification using:
- VGG16 pretrained on ImageNet
- Feature extraction with a frozen convolutional base
- Selective fine-tuning from `block5_conv1`

### 02 — Emotion Detection
Seven-class facial emotion classification using FER2013:
- VGG16 feature extraction
- Selective fine-tuning from `block5_conv1`

## Project Structure

```text
deep-learning-transfer-learning/
├── 01_cats_vs_dogs/
│   ├── 01_feature_extraction.ipynb
│   └── 02_fine_tuning.ipynb
├── 02_emotion_detection/
│   ├── 01_feature_extraction.ipynb
│   └── 02_fine_tuning.ipynb
├── requirements.txt
└── README.md
```

## Methodology

```text
                 VGG16
                   │
        ImageNet pretrained weights
                   │
          ┌────────┴────────┐
          │                 │
   Feature Extraction    Fine-Tuning
   Freeze backbone       Unfreeze deeper layers
          │                 │
     ┌────┴────┐       ┌────┴────┐
     │         │       │         │
 Cats/Dogs  Emotion  Cats/Dogs  Emotion
```

## Training Configuration

For quick, reproducible portfolio demonstrations:

- Image size: `150 × 150`
- Batch size: `32`
- Epochs: **2**
- Backbone: VGG16
- Pretrained weights: ImageNet
- Feature extraction: frozen convolutional base
- Fine-tuning: layers from `block5_conv1` onward

> The 2-epoch setting is intentionally lightweight. Increase `EPOCHS` when running a full experiment.

## Dataset Setup

The datasets are **not included in this repository**.

### Cats vs Dogs

The notebooks expect:

```text
dogsvscats_dataset/
├── train/
│   ├── cats/
│   └── dogs/
└── test/
    ├── cats/
    └── dogs/
```

### FER2013

The emotion notebooks expect:

```text
fer2013_dataset/
├── train/
│   ├── angry/
   ...
└── test/
    ├── angry/
    ...
```

The notebooks contain optional Kaggle/Colab download commands. Configure Kaggle credentials separately before using them.

## Why Two Approaches?

**Feature extraction** provides a fast baseline by keeping pretrained visual features fixed.

**Fine-tuning** allows deeper pretrained layers to adapt to the target dataset. Comparing the two approaches helps demonstrate how transfer learning can be progressively adapted to a new computer-vision problem.

## Technologies

Python • TensorFlow • Keras • VGG16 • NumPy • Matplotlib • Transfer Learning • Computer Vision

## Portfolio Note

These notebooks are structured as reproducible learning/portfolio experiments. Results may vary with dataset versions, hardware, TensorFlow versions, random seeds, and training duration.
