# 🧠 Alzheimer’s Disease Diagnosis using CNN (PyTorch)

This project implements a **Convolutional Neural Network (CNN)** using **PyTorch** to classify brain MRI images for **Alzheimer’s Disease diagnosis**.  
The model learns visual patterns from MRI scans to distinguish between different stages of Alzheimer’s.

---

## 📌 Project Overview

Alzheimer’s Disease is a progressive neurological disorder affecting memory and cognitive abilities.  
Early and accurate diagnosis is critical for effective treatment planning.

In this project:
- MRI brain images are preprocessed and transformed
- A CNN model is built and trained using **PyTorch**
- Model performance is evaluated using **accuracy, classification report, and confusion matrix**

---

## 🚀 Key Features

- CNN-based image classification
- MRI image preprocessing using `torchvision.transforms`
- Training and validation using PyTorch
- Model evaluation with:
  - Accuracy
  - Classification Report
  - Confusion Matrix visualization
- Implemented entirely in **Jupyter Notebook**

---

## 🛠 Tech Stack

- **Python**
- **PyTorch**
- Torchvision
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 📂 Project Structure
```md
Alzheimer_Diagnosis_CNN/
│
├── Alzheimer_project_CNN.ipynb
├── README.md
└── dataset/ (not included in repository)
```

---

## 📊 Dataset

The dataset consists of **MRI brain images** categorized into multiple classes representing different stages of Alzheimer’s Disease, such as:

- Non Demented  
- Very Mild Demented  
- Mild Demented  
- Moderate Demented  

> ⚠️ The dataset is **not included** in this repository due to size limitations.  
> Please place the dataset in the appropriate directory before running the notebook.

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
   - Activation functions
   - Fully connected layers

4. **Training**
   - Loss function: CrossEntropyLoss
   - Optimizer: Adam / SGD
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
