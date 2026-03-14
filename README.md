# Physical Activity Classification and Step Prediction

This repository contains part of the implementation developed during my thesis work.
The project focuses on implementing and experimenting with several machine learning and deep learning models for **physical activity classification** and **daily step prediction**.

---

## Project Overview

The project explores two related tasks using physical activity time-series data.

### 1. Physical Activity Classification

Different time-series classification models are used to classify activity patterns.

Implemented models include:

* ROCKET
* MiniRocket
* MiniRocketVoting
* Multi-Layer Perceptron (MLP)

### 2. Daily Step Prediction

Time-series forecasting models are used to predict future daily step counts.

Implemented models include:

* Bidirectional LSTM
* GRU
* 1D Convolutional Neural Network (CNN-1D)

---

## Dataset

The experiments use physical activity datasets derived from the **PMData** and the **MOX2-5 dataset**.

Main features used in the experiments include:

* `steps` — daily step count
* `sedentary` — sedentary time (minutes)
* `LPA` — light physical activity (minutes)
* `MPA` — moderate physical activity (minutes)
* `VPA` — vigorous physical activity (minutes)

Additional sleep-related features such as sleep duration and sleep score are also used.

Processed datasets used in the experiments are included in this repository.

---

## Repository Structure

0/  
Data preprocessing for the PMData dataset. Raw Fitbit activity and sleep data are aggregated at the daily level and saved as a processed dataset.

1/  
Label generation for the classification task. Activity labels are created based on step counts and activity intensity features.

2/  
Exploratory data analysis and feature analysis including correlation analysis, class distribution visualization, feature selection, PCA, and feature importance analysis.

3/  
Implementation and evaluation of classification models including ROCKET, MiniRocket, MiniRocketVoting, and MLP. Results include confusion matrices and training performance plots.

4/  
Time-series forecasting experiments for daily step prediction using deep learning models such as LSTM, GRU, Bidirectional LSTM/GRU, stacked architectures, and a 1D CNN.

ploting/  
Visualization and exploratory analysis of the datasets including feature distributions, activity level distributions, and participant-level analysis.

## Requirements

Python 3 is required.

Install dependencies with:

pip install -r requirements.txt

Main libraries used include:

* pandas
* numpy
* scikit-learn
* tensorflow / keras
* sktime

---

## Reference

This project was developed as part of my thesis work and includes implementation and experimentation based on methods described in the following research paper:

**An automatic and personalized
recommendation modelling
in activity eCoaching with deep
learning and ontology**

The repository focuses on implementing parts of the data processing and modeling pipeline and experimenting with several machine learning models for activity classification and step prediction.
