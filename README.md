# 🧠 Alzheimer’s Disease Diagnosis using CNN (PyTorch)

This project implements a **Convolutional Neural Network (CNN)** using **PyTorch** to classify brain MRI images into four categories related to Alzheimer’s disease.

The project focuses on building a CNN from scratch and systematically studying the effect of different techniques such as **Batch Normalization, Dropout, and Data Augmentation** on model performance.

---

## 📌 Project Overview

Alzheimer’s Disease is a progressive neurological disorder that affects memory and cognitive abilities.

In this project:

- MRI brain images are preprocessed and transformed
- A CNN model is built and trained using **PyTorch**
- Different CNN configurations and regularization techniques are experimentally evaluated
- Model performance is evaluated using:
  - Accuracy
  - Precision
  - Recall
  - F1-score
  - Confusion Matrix

The project is organized as a series of experiments, with the **Baseline CNN** serving as the reference model.

---

## 🚀 Key Features

- CNN-based MRI image classification
- Image preprocessing using `torchvision.transforms`
- Training and validation using PyTorch
- GPU-accelerated training using CUDA when available
- Evaluation using:
  - Accuracy
  - Classification Report
  - Confusion Matrix
  - Macro F1-score
- Systematic comparison of different CNN techniques
- Experiments implemented using Jupyter Notebooks

---

## 🛠 Tech Stack

- **Python**
- **PyTorch**
- **Torchvision**
- **NumPy**
- **Matplotlib**
- **Scikit-learn**
- **Jupyter Notebook**

---

## 📂 Project Structure

```text
Alzheimer_Diagnosis_CNN/
│
├── dataset/                         # Dataset (not included in repository)
│
├── experiments/
│   ├── 01_baseline_cnn.ipynb
│   ├── 02_batch_normalization.ipynb
│   ├── 03_dropout.ipynb
│   ├── 04_data_augmenttaion.ipynb
│   ├── 05_cnn_tuning.ipynb
│   └── 06_resnet_18.ipynb
│
├── results/
│   ├── 01_baseline_cnn.txt
│   ├── 02_batch_normalization.txt
│   ├── 03_dropout.txt
│   ├── 04_data_augmenttaion.txt
│   ├── 05_cnn_tuning.txt
│   └── 06_resnet_18.txt
│
├── README.md
└── .gitignore
```

---

## 📊 Dataset

The dataset consists of brain MRI images divided into four classes:

- Mild Impairment
- Moderate Impairment
- No Impairment
- Very Mild Impairment

The dataset is loaded using torchvision.datasets.ImageFolder.

⚠️ The dataset is not included in this repository due to its size.

The expected directory structure is:
```text
dataset/
│
├── train/
│   ├── Mild Impairment/
│   ├── Moderate Impairment/
│   ├── No Impairment/
│   └── Very Mild Impairment/
│
└── test/
    ├── Mild Impairment/
    ├── Moderate Impairment/
    ├── No Impairment/
    └── Very Mild Impairment/
```

---

## ⚙️ Model Workflow

1. **Data Loading**
   - Images loaded using `torchvision.datasets`
   - Batched using `DataLoader`

2. **Preprocessing**
   - Image resizing
   - Normalization
   - Tensor conversion

3. **Model Architecture**
   - Convolutional layers
   - Activation functions (ReLU)
   - Pooling layers (Max Pooling)
   - Flattening
   - Fully connected layers

4. **Training**
   - Loss function: CrossEntropyLoss
   - Optimizer: Adam 
   - Epoch-based training loop

5. **Evaluation**
   - Accuracy calculation
   - Classification report
   - Confusion matrix visualization

---

## ▶️ How to Run

1. Clone the repository:
```bash
git clone https://github.com/Himanshimittal051104/Alzheimer_Diagnosis_CNN.git
```

2. Navigate to the project folder:
```bash
cd Alzheimer_Diagnosis_CNN
```

3. Install dependencies::
```bash
pip install torch torchvision numpy matplotlib scikit-learn
```

4. Launch Jupyter Notebook:
```bash
jupyter notebook
```

5. Open and run:
```bash
Alzheimer_project_CNN.ipynb
```

---

## 📈 Results

The trained CNN model is evaluated using:

- Accuracy score
- Precision, Recall, F1-score (Classification Report)
- Confusion Matrix for class-wise performance analysis

---

## 🔮 Future Improvements

- Apply Transfer Learning (ResNet, VGG, EfficientNet)
- Hyperparameter tuning
- Add model checkpoint saving
- Deploy using Flask / FastAPI
- Build a web interface for real-time predictions

---

## 👩‍💻 Author

Himanshi Mittal

---
