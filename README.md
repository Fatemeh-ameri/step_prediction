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

---

## Results

### Classification Results

The classification experiments were evaluated using confusion matrices for the following models:

- ROCKET  
- MiniRocket  
- MiniRocketVoting  
- Multi-Layer Perceptron (MLP)

Generated confusion matrices and training plots for both the **PMData** and **MOX** datasets are included in the repository.

---

### Step Prediction Results

The following table summarizes the forecasting performance of different deep learning models for daily step prediction.

#### PMData Dataset

| Model | RMSE | MAE | RSD | ET |
|------|------|------|------|------|
| CNN-1D | 1164 | 230 | 11656 | 1288 |
| Bidirectional GRU | 4468 | 3359 | 4470 | 1372 |
| Vanilla LSTM | 4633 | 3419 | 4636 | 1412 |
| Stacked LSTM | 4662 | 3461 | 4664 | 3219 |
| Stacked GRU | 4788 | 3546 | 4791 | 3706 |
| Vanilla GRU | 4815 | 3583 | 4818 | 1253 |
| Bidirectional LSTM | 5006 | 3776 | 5009 | 2252 |

#### MOX Dataset

| Model | RMSE | MAE | RSD | ET |
|------|------|------|------|------|
| CNN-1D | 1510 | 413 | 1513 | 108 |
| Stacked GRU | 4767 | 3534 | 4778 | 376 |
| Stacked LSTM | 4798 | 3569 | 4809 | 414 |
| Vanilla GRU | 4836 | 3578 | 4847 | 179 |
| Bidirectional LSTM | 4851 | 3585 | 4862 | 349 |
| Bidirectional GRU | 4865 | 3589 | 4867 | 310 |
| Vanilla LSTM | 4881 | 3619 | 4893 | 190 |

Lower values of RMSE and MAE indicate better prediction performance.

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

**[An automatic and personalized
recommendation modelling
in activity eCoaching with deep
learning and ontology](https://www.nature.com/articles/s41598-023-37233-7)**

The repository focuses on implementing parts of the data processing and modeling pipeline and experimenting with several machine learning models for activity classification and step prediction.
