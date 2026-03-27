# Privacy-Preserving Facial Emotion Detection using CNN

## 📌 Overview

This repository contains the implementation of a **Convolutional Neural Network (CNN)-based facial emotion detection system** developed as part of an undergraduate research project.

The system focuses on:

* Accurate facial emotion classification
* Privacy preservation by avoiding storage of raw facial images
* Secure emotion logging using a blockchain-inspired mechanism

The model is trained using grayscale facial images and optimized for real-time inference.

---

## 🎯 Objectives

* Develop a CNN model for facial emotion recognition
* Improve classification performance on multi-class emotion datasets
* Ensure **privacy-preserving predictions**
* Log only emotion labels instead of sensitive image data

---

## 🧠 Model Architecture

The model is based on **ResNet18** with custom modifications:

* Transfer learning backbone: `ResNet18`
* Custom fully connected layers
* Activation: **ReLU**
* Dropout regularization
* Softmax output for multi-class classification

---

## 📂 Dataset

The model is trained on a structured dataset similar to FER-style datasets:

```
dataset/
   train/
      angry/
      happy/
      sad/
      neutral/
      ...
   test/
      angry/
      happy/
      sad/
      neutral/
      ...
```

* Images are converted to grayscale
* Resized to 224 × 224
* Data augmentation applied to improve generalization

---

## ⚙️ Training Details

* Framework: **PyTorch**
* Loss Function: CrossEntropyLoss
* Optimizer: Adam
* Learning Rate Scheduler: ReduceLROnPlateau
* Batch Size: 128
* Image Size: 224 × 224
* Epochs: 10–25 (with early stopping)

---

## 📊 Performance

* Validation Accuracy: ~68%
* Test Accuracy: ~66–69%
* Strong performance on:

  * Happy
  * Surprise
* Moderate performance on:

  * Sad, Neutral, Angry

---

## 🔐 Privacy-Preserving Mechanism

This project ensures privacy by:

* ❌ Not storing facial images
* ✅ Storing only:

  * Predicted emotion label
  * Timestamp
  * Hashed identifier

This aligns with ethical AI and data protection principles.

---

## 🔗 Blockchain-Based Logging (Concept)

A lightweight blockchain-inspired structure is used to ensure data integrity:

Each record contains:

* Emotion label
* Timestamp
* Previous hash
* Current hash

This ensures:

* Tamper resistance
* Traceability
* Secure logging

---

## 📁 Project Structure

```
├── emotion_model.ipynb     # Main training notebook
├── best_emotion_model.pth # Trained model (output)
├── class_names.json       # Label mapping
├── train_history.json     # Training metrics
└── README.md              # Project documentation
```

---

## 🚀 How to Run

1. Open the notebook:

```
emotion_model.ipynb
```

2. Run all cells sequentially in **Google Colab or Jupyter Notebook**

3. Ensure dataset is structured correctly in:

```
train/ and test/ folders
```

---

## 📌 Key Features

* CNN-based emotion classification
* Transfer learning with ResNet18
* Real-time readiness
* Privacy-aware design
* Blockchain-based logging concept

---

## 📚 Future Improvements

* Improve accuracy using advanced architectures (EfficientNet, ViT)
* Add attention mechanisms
* Enhance performance on minority classes
* Deploy as a real-time web application
* Integrate full blockchain network

---

## 👨‍💻 Author

Undergraduate Research Project
Management Information Systems (MIS)

---

## 📜 License

This project is for academic and research purposes.
