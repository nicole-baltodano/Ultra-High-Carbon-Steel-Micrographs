
# "Multimodal Classification of Microconstituents in Ultra High Carbon Steel"

## 📌 Overview  
This project applies a **multimodal deep learning approach** to classify microconstituents in high-carbon steel micrographs. It integrates **Convolutional Neural Networks (CNNs)** for image-based classification and a **Multilayer Perceptron (MLP)** for numerical/tabular data to improve prediction accuracy.

🔗 **Dataset**: [High Carbon Micrographs (Kaggle)](https://www.kaggle.com/datasets/safi842/highcarbon-micrographs/data)  

---

## 🔬 Project Motivation  
Heat treatment significantly impacts the microstructure of steel, influencing its mechanical properties. Accurately classifying microconstituents—such as **spheroidite, pearlite, and network**—is critical for quality control in metallurgy. This project explores the **feasibility of deep learning models** in predicting these microstructures using **image and numerical data**.

---

## 🛠️ Methodology  

### 1️⃣ Data Preprocessing  
- **Numerical Features**: Standardized **annealing temperature and time** using `StandardScaler()`.  
- **Categorical Features**: One-hot encoded **cooling method**.  
- **Image Processing**: Resized images and normalized pixel values.  

### 2️⃣ Model Architecture  
- **CNN for Image Processing**  
  - Convolutional layers extract features from steel micrographs.  
  - Max-pooling layers reduce dimensionality.  
  - Fully connected layers generate embeddings for classification.  

- **MLP for Numerical Features**  
  - Dense layers process annealing parameters and cooling methods.  
  - Integrated with CNN embeddings for final prediction.  

- **Final Classification**  
  - Softmax activation for multi-class classification (`spheroidite`, `pearlite`, `network`).  

---

## 📊 Results & Analysis  
- **Overall Model Accuracy**: **81%**  
- **Spheroidite Recall**: **0.95** (Excellent classification performance)  
- **Network Recall**: **0.30** (Struggled with identification)  
- **Pearlite Classification**: **Not predicted** due to extreme underrepresentation  

### Key Insights  
✔ CNN model **successfully classifies spheroidite** with high accuracy.  
⚠ **Underrepresented classes (pearlite, network) require augmentation** for better balance.  
❌ Model **fails to classify pearlite** due to lack of samples.  

---

## 📈 Classification report

![image](https://github.com/user-attachments/assets/74dcf4cc-66be-4cb4-aacf-5ceb7a9dcdd9)

