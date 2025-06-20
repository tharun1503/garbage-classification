# 🗑️ Garbage Classification using EfficientNetV2B2

This project is part of the **Summer of AI Internship Program 2025 by Edunet Foundation and IBM SkillsBuild**. The goal is to build an intelligent image classifier that identifies types of garbage from images using deep learning.

---

## 📌 Problem Statement

Efficient garbage classification is essential for environmental sustainability. Manual sorting is inefficient and error-prone. This project leverages deep learning to automate classification of waste into categories such as **plastic, cardboard, metal, paper, glass, and trash**.

---

## 📂 Dataset

- **Source:** [TrashType Image Dataset on Kaggle](https://www.kaggle.com/datasets/farzadnekouei/trash-type-image-dataset)
- **Classes:** `cardboard`, `glass`, `metal`, `paper`, `plastic`, `trash`
- **Total Images:** 2527

We manually split the dataset into:
- `train/`
- `val/`
- `test/`

---

## 🧠 Model Architecture

- Base Model: **EfficientNetV2B2** (pretrained on ImageNet)
- Layers Added:
  - `GlobalAveragePooling2D`
  - `Dense(128, ReLU)`
  - `Dropout`
  - `Dense(6, Softmax)`
- Fine-tuning: First 200 layers frozen, rest trainable

---

## 📈 Performance

| Metric       | Value     |
|--------------|-----------|
| ✅ Accuracy (Test) | 88.67%    |
| ✅ Validation Accuracy | ~87%    |
| 🔍 Classes | 6         |
| 📦 Model Size | ~34MB    |

---

## 🚀 How to Use (Gradio App)

This project includes a simple Gradio-based interface to test predictions:

### ▶️ Launch Interface

```bash
iface.launch()

