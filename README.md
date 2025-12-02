# SOEN 321 Project: Attacks on Machine Learning Models

**Course:** SOEN 321: Information Systems Security (Concordia University)  
**Term:** Fall 2025  
**Topic:** Adversarial Attacks on CNN-based Intrusion Detection Systems using the NSL

## Collaborators:

| Avatar | Name | Student ID | GitHub |
|:------:|------|:----------:|:------:|
| <img src="https://github.com/7awraaa.png" width="36" alt="7awraaa"/> | Hawraa Al-Adilee | 40246450 | [7awraaa](https://github.com/7awraaa) |
| <img src="https://github.com/Ikramkamal.png" width="36" alt="Ikramkamal"/> | Ikram Kamal  | 40248477 | [Ikramkamal](https://github.com/Ikramkamal) |
| <img src="https://github.com/hibamai.png" width="36" alt="hibamai"/> | Hiba Maifi | 40289223 | [hibamai](https://github.com/hibamai) |
| <img src="https://github.com/carmoucha.png" width="36" alt="carmoucha"/> | Carmen Derderian | 40244084 | [carmoucha](https://github.com/carmoucha) |
| <img src="https://github.com/jdplao.png" width="36" alt="jdplao"/> | Jidapa Laopikanon | 40263947 | [jdplao](https://github.com/jdplao) |
| <img src="https://github.com/y-mouatif.png" width="36" alt="y-mouatif"/> | Yasmine Mouatif | 40249967 | [y-mouatif](https://github.com/y-mouatif) |

## Project Overview
Machine learning models used in cybersecurity (like Intrusion Detection Systems) are vulnerable to adversarial attacks. This project investigates the robustness of a **Convolutional Neural Network (CNN)** trained on the **NSL-KDD** dataset.

We trained a model to classify network traffic as **Malicious** or **Benign** and then evaluated its performance against two gradient-based adversarial attacks:
1.  **FGSM** (Fast Gradient Sign Method)
2.  **PGD** (Projected Gradient Descent)

## Dataset
We used the **NSL-KDD** dataset (Kaggle), a refined version of the KDD'99 dataset used for intrusion detection tasks.
* **Classes:** Malicious vs. Benign
* **Preprocessing:** Categorical encoding, normalization, and reshaping for 1D-CNN input.

## Attacks Implemented
We implemented two specific attack scenarios to disrupt the model's classification:

| Attack | Parameters Used | Description |
| :--- | :--- | :--- |
| **FGSM** | $\epsilon = 0.05$ | Single-step gradient attack. Fast but less powerful. |
| **PGD** | $\epsilon = 0.05, \alpha = 0.01, iter = 20$ | Iterative attack. Slower but significantly more destructive. |

## How to run the project
### To run data preprocessing
Open and run `preprocessing.ipynb`.  
This notebook prepares and saves the cleaned dataset for model training.

### To run the CNN model and attacks
Open and run `cnn_model.ipynb`.  
This notebook trains the CNN and executes the attack experiments.
