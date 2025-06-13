# 🐾 Image Segmentation with TensorFlow (Oxford-IIIT Pet Dataset)

This project performs **semantic image segmentation** using a deep learning model built with TensorFlow and trained on the **Oxford-IIIT Pet Dataset**. The goal is to classify each pixel in the image into one of three categories: pet, pet border, or background.

---

## 📌 Overview

This notebook-based project walks through:

- Downloading and preprocessing the Oxford-IIIT Pet dataset
- Building a U-Net style segmentation model
- Training the model with TensorFlow/Keras
- Visualizing predictions and evaluating results

---

## 🐶 Dataset

- **Name**: Oxford-IIIT Pet Dataset
- **Source**: [TensorFlow Datasets](https://www.tensorflow.org/datasets/catalog/oxford_iiit_pet)
- **Labels**:
  - Class 1: Pet
  - Class 2: Border of the pet
  - Class 3: Background (surroundings)

---

## 🧰 Requirements

Install the required libraries:

```bash
pip install tensorflow tensorflow_datasets git+https://github.com/tensorflow/examples.git -U keras
```

## 🧠 Model Architecture

- **Type**: U-Net (encoder-decoder)
- **Input Size**: 128 × 128 RGB images
- **Output**: Segmentation mask with 3 classes
- **Layers**:
  - Convolutional layers with ReLU
  - MaxPooling for downsampling
  - UpSampling and skip connections in the decoder
  - Final layer with `softmax` activation

---

## 📥 Data Preprocessing

- Images and masks are resized to **128×128**
- Pixel values normalized to **[0, 1]**
- Mask labels are shifted to **0, 1, 2** format
- Data is **batched and shuffled** for training

## 📊 Evaluation

- **Visual Output**: Side-by-side plots of the input image, true mask, and predicted mask
- **Metrics**:
  - Pixel-wise accuracy
  - *(Optionally extend with IoU, Dice coefficient)*

---

## 🖼️ Sample Results
![download](https://github.com/user-attachments/assets/7d1c8b1f-8af6-49c4-bda0-dfcdffafa39c)


