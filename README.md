# unstructured-corona
# 🩺 COVID-19 Image Classification using CNN

## 📌 Project Overview

This project demonstrates how to process unstructured image data and apply Convolutional Neural Networks (CNNs) to classify chest X-ray/CT scan images into three categories:

* COVID
* Normal
* Viral Pneumonia

The goal is to explore how deep learning can assist in healthcare image analysis and to provide insights into classification performance.

## 📂 Dataset

* Dataset: COVID-19 Chest X-ray/CT Scan Image Dataset (from Kaggle).
* Structure:

  Covid19-dataset/
      ├── train/
      │   ├── Covid/
      │   ├── Normal/
      │   └── Viral Pneumonia/
      └── test/
          ├── Covid/
          ├── Normal/
          └── Viral Pneumonia/

* Training images: 251
* Testing images: 66

## ⚙️ Methodology

1. Data Upload & Extraction – Loaded the dataset in Google Colab and extracted images.
2. Preprocessing – Resized images to 128×128 pixels, normalized pixel values, and one-hot encoded labels.
3. Modeling (CNN) –
   * Convolution + MaxPooling layers
   * Fully connected Dense layers
   * Softmax activation for multi-class output
4. Training & Validation – Trained on the train set and validated on the test set.
5. Evaluation – Used accuracy, confusion matrix, and visual predictions for performance analysis.

## 📊 Results & Insights

* CNN achieved ~80–90% accuracy (varies by run).
* Normal cases were classified with high accuracy.
* Some COVID cases were misclassified as Pneumonia due to image similarity.
* Confusion matrix revealed the model’s strength in detecting Normal vs Pneumonia but highlighted the challenge in distinguishing COVID from other viral infections.

## 📌 Sample Predictions

* Below are examples of model predictions compared with true labels:

Predicted: Normal | True: Normal
Predicted: Viral Pneumonia | True: Viral Pneumonia
Predicted: Covid | True: Covid

## 🚀 How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/covid19-image-classification.git
   cd covid19-image-classification
   ```

2. Open the notebook in Google Colab.

3. Upload dataset zip file (from Kaggle) into Colab or mount Google Drive.

4. Run preprocessing, training, and evaluation cells.

## 📌 Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy & Pandas
* Matplotlib / Seaborn

## 🙌 Acknowledgements

* Kaggle: [COVID-19 Chest X-ray/CT Scan Dataset](https://www.kaggle.com/)
* TensorFlow/Keras for deep learning framework.

