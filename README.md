# 🧠 MRI Brain Tumor Detection using CNN

A Deep Learning project that uses a **Convolutional Neural Network (CNN)** to classify brain MRI images into two categories: **Tumor** and **Healthy**.

The project uses Python, TensorFlow, Keras, and OpenCV to preprocess MRI images, train a CNN model, evaluate its performance, visualize feature maps, and make predictions on individual MRI scans.

## 📌 Project Overview

Brain tumor detection through MRI scans is an important application of medical image analysis. This project explores how deep learning and CNNs can be used to identify tumor patterns in brain MRI images.

The model performs binary image classification:
- **Tumor (1):** MRI image classified as containing a tumor.
- **Healthy (0):** MRI image classified as healthy.

## 🚀 Features

- Automatic MRI dataset download using KaggleHub.
- MRI image loading and preprocessing using OpenCV.
- Image resizing to 128 × 128 pixels.
- RGB conversion and pixel normalization.
- Training and validation split (80:20).
- Custom CNN architecture using TensorFlow and Keras.
- Early stopping to reduce overfitting.
- Training and validation loss visualization.
- Model evaluation using accuracy and classification report.
- Confusion matrix visualization.
- CNN feature map visualization.
- Prediction on individual MRI images.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Programming language |
| TensorFlow | Deep learning framework |
| Keras | CNN model development |
| OpenCV | Image processing |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Confusion matrix visualization |
| Scikit-learn | Dataset splitting and evaluation |
| KaggleHub | Dataset download |

## 📂 Dataset

This project uses the **Brain Tumor MRI Dataset** by Masoud Nickparvar.

Dataset: [Brain Tumor MRI Dataset – Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)

The notebook downloads the dataset using KaggleHub.

The original dataset contains four categories:
- Glioma
- Meningioma
- Pituitary
- No Tumor

For this implementation, the classification task is binary: Tumor vs Healthy.

## 🧠 CNN Architecture

The project implements a custom CNN using Keras Sequential API.

| Layer | Configuration |
|---|---|
| Input | 128 × 128 × 3 |
| Conv2D | 6 filters, 5 × 5 kernel |
| Activation | Tanh |
| Average Pooling | 2 × 2 |
| Conv2D | 16 filters, 5 × 5 kernel |
| Activation | Tanh |
| Average Pooling | 2 × 2 |
| Flatten | Feature vector |
| Dense | 120 neurons, Tanh |
| Dense | 84 neurons, Tanh |
| Output | 1 neuron, Sigmoid |

**Model Configuration:**
- Optimizer: Adam
- Learning Rate: 0.0001
- Loss Function: Binary Crossentropy
- Evaluation Metric: Accuracy
- Batch Size: 32
- Maximum Epochs: 100
- Early Stopping Patience: 12

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/MRI-Brain-Tumor-Detection-CNN.git
```

### 2. Navigate to the project directory

```bash
cd MRI-Brain-Tumor-Detection-CNN
```

### 3. Install dependencies

```bash
pip install tensorflow numpy opencv-python matplotlib seaborn scikit-learn kagglehub jupyter
```

### 4. Run the notebook

```bash
jupyter notebook MRI_Brain_Tumor_Detection.ipynb
```

You can also open the notebook directly in Google Colab.

## 📊 Model Evaluation

The model is evaluated using:

- Training and validation accuracy.
- Training and validation loss.
- Classification report.
- Confusion matrix.

These evaluation methods help analyze the model's classification performance and identify potential errors.

## 🔍 Individual MRI Prediction

The notebook includes a prediction function that accepts an MRI image path and returns:

- Predicted class (Tumor or Healthy).
- Prediction probability.
- Visualization of the input MRI image with its predicted label.

## 📁 Project Structure

```text
MRI-Brain-Tumor-Detection-CNN/
│
├── MRI_Brain_Tumor_Detection.ipynb
├── README.md
└── data/                  # Dataset files (if stored locally)
```

## 🔮 Future Improvements

- Experiment with deeper CNN architectures.
- Apply data augmentation to improve generalization.
- Compare CNN performance with transfer learning models such as VGG16 and ResNet50.
- Improve model performance through hyperparameter tuning.
- Build a simple web interface using Streamlit.
- Extend classification to identify individual tumor types.


---

⭐ If you find this project interesting, consider giving the repository a star!
