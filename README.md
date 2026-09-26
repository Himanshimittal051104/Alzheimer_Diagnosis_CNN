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
│   ├── 04_data_augmentation.ipynb
│   ├── 05_cnn_tuning.ipynb
│   └── 06_resnet_18.ipynb
│
├── results/
│   ├── 01_baseline_cnn.txt
│   ├── 02_batch_normalization.txt
│   ├── 03_dropout.txt
│   ├── 04_data_augmentation.txt
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
Each notebook contains the corresponding model implementation, training process, evaluation metrics, and visualizations.

---

## 🧪 Experiments

The project contains six experiments.

### Experiment 1 — Baseline CNN

- A basic CNN architecture was implemented as the reference model for the project.
- The model consists of three convolutional blocks, each containing a convolutional layer, ReLU activation, and max pooling, followed by fully connected layers for four-class classification.
- This experiment establishes the baseline against which the subsequent experiments are compared.
  
### Experiment 2 — Batch Normalization

- Batch Normalization was added after the convolutional layers to investigate its effect on training stability and model performance.
- The experiment also used Adaptive Average Pooling before the fully connected layers to reduce the number of parameters in the classifier.
- Different Batch Normalization configurations were investigated, including batch size and BatchNorm momentum.

### Experiment 3 — Dropout

- Dropout was introduced into the fully connected layers to investigate its effect on overfitting and generalization.
- A dropout probability of 0.5 was used during training. Dropout randomly deactivates a portion of neurons during each training step, encouraging the network to learn more robust features.

### Experiment 4 — Data Augmentation

- Random Rotation and Random Horizontal Flip were applied to the training images.
- The experiment also investigated the effect of the transformation order.

### Experiment 5 — CNN Tuning

- The CNN architecture and training hyperparameters were modified to investigate their effect on model performance.
- The experiment was conducted in three stages:
  - **Additional Convolutional Layer:** A deeper CNN architecture was tested by adding an extra convolutional layer.
  - **Batch Size Tuning:** The batch size was increased from 16 to 32 to study its effect on training and generalization.
  - **Learning Rate Tuning:** The learning rate was reduced from 0.001 to 0.0001 to investigate its effect on convergence and performance.

### Experiment 6 — ResNet-18

- A pretrained ResNet-18 model was evaluated using transfer learning for the four-class MRI classification task.
- The model was initialized with pretrained ImageNet weights, and the original final classification layer was replaced with a new fully connected layer containing four output classes.
- No data augmentation was applied in this experiment so that the effect of the pretrained ResNet-18 architecture could be evaluated separately.

---

## 📈 Results and Comparison

| Experiment | Modification | Test Accuracy | Macro F1 |
|------------|--------------|---------------|----------|
| 1 | Baseline CNN | 96.17% | 0.9684 |
| 2 | Batch Normalization | 35.03% | 0.1297 |
| 3 | Dropout | 96.09% | 0.9714 |
| 4 | Data Augmentation | 60.44% | 0.6061 |
| 5 | CNN Tuning | 94.14% | 0.9384 |
| 6 | ResNet-18 | 93.90% | 0.9575 |

The experiments demonstrate how changes in CNN architecture, regularization, data transformations, hyperparameters, and transfer learning can produce substantially different results on the same dataset.

---

## 🔮 Future Improvements

- Experiment with additional transfer learning architectures such as VGG and EfficientNet.
- Perform more extensive hyperparameter tuning.
- Add model checkpoint saving and loading.
- Evaluate models using additional datasets.
- Deploy the trained model using Flask or FastAPI.
- Build a web interface for MRI image classification.
- Investigate class imbalance and additional evaluation strategies.

---

## 👩‍💻 Author

Himanshi Mittal

---
