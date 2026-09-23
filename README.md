# 🧠 Alzheimer’s Disease Diagnosis using CNN (PyTorch)

This project implements a **Convolutional Neural Network (CNN)** using **PyTorch** to classify brain MRI images into four categories related to Alzheimer’s disease.

The project focuses on building CNN models from scratch and systematically studying the effect of different techniques such as **Batch Normalization, Dropout, Data Augmentation, CNN architecture tuning, and Transfer Learning using ResNet-18** on model performance.

---

## 📌 Project Overview

Alzheimer’s Disease is a progressive neurological disorder that affects memory and cognitive abilities.

In this project:

- MRI brain images are preprocessed and transformed.
- CNN models are built and trained using **PyTorch**.
- Different CNN configurations and techniques are experimentally evaluated.
- A pretrained **ResNet-18** model is also evaluated using transfer learning.
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
- CNN architecture and hyperparameter tuning
- Transfer learning using pretrained ResNet-18
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
   - Images are loaded using torchvision.datasets.ImageFolder.
   - Images are divided into training, validation, and test sets.
   - Batches are created using DataLoader.

2. **Preprocessing**
   - Images are resized to 224 × 224.
   - Images are converted to tensors.
   - Image normalization is applied using ImageNet normalization values.

3. **Model Architecture**
   - Convolutional layers
   - Activation functions (ReLU)
   - Pooling layers (Max Pooling)
   - Flattening
   - Fully connected layers
   - Four output classes

4. **Training**
   - Loss function: CrossEntropyLoss
   - Optimizer: Adam
   - Training is performed for 10 epochs for each experiment.
   - GPU acceleration is used when CUDA is available

5. **Evaluation**
   - Accuracy calculation
   - Macro F1 score
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

4. Add the dataset

Place the dataset inside the dataset/ directory using the structure described above.

5. Launch Jupyter Notebook:
```bash
jupyter notebook
```

6. Run the experiments

Open the notebooks inside the experiments/ directory:
```bash
experiments/
├── 01_baseline_cnn.ipynb
├── 02_batch_normalization.ipynb
├── 03_dropout.ipynb
├── 04_data_augmenttaion.ipynb
├── 05_cnn_tuning.ipynb
└── 06_resnet_18.ipynb
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
