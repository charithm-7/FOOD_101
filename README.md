# 🍱 Food Detection and Calorie Prediction

This project uses **deep learning and computer vision** to automatically detect food items in images and predict their **nutritional values**, including **calories, proteins, fats, and carbohydrates**. It is built using **PyTorch** and trained on the **Food-101 dataset**, one of the largest food image datasets publicly available.

---

## 🔬 Project Motivation

Manually tracking food intake is time-consuming and prone to errors. This project solves that by building an AI model that:

- Detects the type of food from an image
- Predicts its approximate nutritional content
- Helps in **health tracking**, **diet planning**, and **calorie monitoring**

---

## 🧠 Model Architecture

- **Backbone**: `DenseNet201` pre-trained on ImageNet
- **Custom Classifier Head**:
  - `Linear(1920 → 1024)`
  - `LeakyReLU()`
  - `Linear(1024 → 101)` (for 101 food classes)
- **Loss Function**: CrossEntropyLoss
- **Optimizer**: Adam
- **Learning Rate**: 0.001
- **Epochs**: 5 (with early stopping if accuracy > 95%)

---

## 📊 Training Insights

- Dataset: [Food-101](https://www.kaggle.com/datasets/dansbecker/food-101)
- Augmentations:
  - Random Rotation
  - Resized Crop
  - Horizontal Flip
  - AutoAugment (ImageNet policy)
- Batch Size: 128
- Image Size: 224x224
- Device: Trained on CPU/GPU based on availability

---

## 🧪 Evaluation Approach

- **Accuracy & Loss**: Tracked per epoch to monitor overfitting
- **Confusion Matrix**: 101x101 comparison of true vs predicted labels
- **ROC Curve**: For selected classes to analyze performance
- **Nutritional Prediction**: Based on class → calorie mapping using a lookup dictionary

---

## 🧩 Challenges Solved

- 🔁 Balanced learning across **101 diverse food classes**
- 🖼️ Real-time food image classification
- 🧮 Mapping food to nutrition using a **custom-built calorie dictionary**
- ⚖️ Achieving high accuracy without overfitting by using **transfer learning**

---

## 📈 Visual Outputs

### 📊 Accuracy & Loss Graph

- Shows training accuracy and loss per epoch

### 📉 ROC Curve

- For classes like: Apple Pie, Baby Back Ribs, Pizza, Hamburger, Baklava

### 📊 Confusion Matrix

- 101x101 matrix showing performance for each class