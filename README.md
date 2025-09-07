# Comparing Classification and Prediction Models

The project compares different machine learning models for two main tasks: classification and time series prediction.

---

## 📋 About The Project

1.  **Classification:** I use several common classifiers and a Multi-Layer Perceptron (MLP) neural network to classify physical activity levels.
2.  **Prediction:** I use common forecasting models and a 1D Convolutional Neural Network (CNN-1D) to predict future daily steps.

---

## 🛠️ Models Implemented

### Classification Models
* Common classifiers like **Rocket**, **MiniRocket** and **MiniRocketVoting** for time series classification.
* A **Multi-Layer Perceptron (MLP)** neural network built with Keras/TensorFlow.

### Prediction (Forecasting) Models
* Common time series models like **Bidirectional LSTM / GRU**.
* A **1D Convolutional Neural Network (1D-CNN)** for time series prediction.

---

## 📊 Dataset

This project uses a physical activity dataset from the `PMData` collection and a private dataset called MOX2-5. The main features include:
* `steps`: Daily step count
* `sedentary`: Time spent being sedentary (in minutes)
* `LPA`: Light Physical Activity (in minutes)
* `MPA`: Moderate Physical Activity (in minutes)
* `VPA`: Vigorous Physical Activity (in minutes)

The dataset file (`PMData_features_vector.csv`) is included in this repository.
The dataset file (`MOX2_5_data_labelled.csv`) is included in this repository.

---

## 🚀 Getting Started

Make sure you have Python 3 installed. You will also need install whatever are in the requiremnt.text.
