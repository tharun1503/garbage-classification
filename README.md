
# 🗑️ Garbage Classification using EfficientNetV2B2

## 📌 Problem Statement
Classify images of garbage into 6 categories: cardboard, glass, metal, paper, plastic, and trash using a deep learning model.

## 📁 Dataset Used
[Kaggle - Trash Type Image Dataset](https://www.kaggle.com/datasets/farzadnekouei/trash-type-image-dataset)  
Total images: 2527  
Split: 80% Train, 20% Validation, and Test

## 🧠 Model Architecture
- **Base Model:** EfficientNetV2B2 (pretrained on ImageNet)
- **Added Layers:**
  - GlobalAveragePooling2D
  - Dropout(0.2)
  - Dense(128, ReLU)
  - Dense(6, Softmax)

## 📊 Performance
- ✅ **Test Accuracy**: 88.67%
- 🧪 **Test Loss**: 0.3321

## 💻 How to Use
1. Upload an image to the Gradio interface
2. The model will classify it into one of the 6 garbage categories
3. Displays predicted class and confidence score

## 🌐 Gradio Screenshot
(Add your screenshot here if needed)

## 📂 Files Included
- `Garbage_Classification.ipynb`
- `garbage_classifier_model.keras`
- `README.md`
