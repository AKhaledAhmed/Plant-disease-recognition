# 🌱 Plant Disease Detection with CNNs and Transfer Learning

This project focuses on detecting plant leaf diseases using image classification.  
It compares different deep learning approaches, including a **Custom CNN**, **VGG16**, and **MobileNetV2**, trained on plant image datasets.

---

## 📌 Project Goals

- Classify plant leaves into different disease categories.  
- Compare performance of classical CNN vs. transfer learning models.  
- Use **data augmentation** to improve generalization.  
- Evaluate models with training/validation accuracy.  
- Save the best-performing model for deployment.

---

## 📂 Dataset

- Source: [PlantVillage Dataset (Kaggle)](https://www.kaggle.com/datasets/rashikrahmanpritom/plant-disease-recognition-dataset)  
- Images organized in `train/` and `test/` folders by class.  
- Example structure:


---

## 🛠️ Preprocessing

- Image resizing to **224x224** pixels.  
- Normalization of pixel values.  
- Data augmentation (rotation, zoom, flips, shifts) using `ImageDataGenerator`.  
- Class weighting to handle imbalanced data.  

---

## 🤖 Models Used

1. **Custom CNN**  
   - Sequential model with Conv2D, MaxPooling, Dropout, Dense layers.  

2. **VGG16 (Transfer Learning)**  
   - Pre-trained on ImageNet.  
   - Added fully connected layers for classification.  

3. **MobileNetV2 (Transfer Learning)**  
   - Lightweight and efficient.  
   - Fine-tuned with dense layers.  

All models trained with:  
- Optimizer: **Adam**  
- Loss: **Categorical Crossentropy**  
- Metric: **Accuracy**  
- Epochs: 25  
- Callbacks: **EarlyStopping** & **ModelCheckpoint**  

---

## 📊 Results

- Training vs Validation Accuracy plotted for all models.  
- **MobileNetV2** and **VGG16** achieved higher validation accuracy compared to the custom CNN.  
- Accuracy trends showed better generalization with transfer learning.  

---

## 💾 Model Saving

- Best models saved as `.h5` files using **ModelCheckpoint**.  
- Example: `model3.h5` for MobileNetV2.  

---

## 📚 Libraries Used

- **tensorflow / keras**  
- **pandas, numpy**  
- **matplotlib, seaborn**  
- **scikit-learn**  
- **opencv-python**  

---

## 🚀 Usage

1. Clone this repository:  
   ```bash
   git clone https://github.com/your-username/plant-disease-detection.git
   cd plant-disease-detection
