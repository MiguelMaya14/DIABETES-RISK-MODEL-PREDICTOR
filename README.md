# DIABETES-RISK-MODEL-PREDICTOR

An Artificial Neural Network (ANN) engineered to analyze clinical data and predict the probability of diabetes risk in pregnant women. This project leverages deep learning techniques to process health indicators and provide binary classification outputs.

---

##  Project Overview

Early detection of diabetes risk during pregnancy is crucial for preventative healthcare. This project focuses on building, training, and evaluating a **second-generation multi-layer perceptron** using clinical data sourced from **Kaggle**. The goal is to classify whether a patient falls into a high-risk or low-risk category based on multiple physiological variables.

---

##  Technical Architecture & Logic

The neural network is built with a custom architecture optimized for binary classification and stable error propagation:

- **Input Layer:** Processes clinical features extracted and normalized from the Kaggle health dataset.
- **Hidden Layer (32 Neurons):** Configured with 32 hidden units utilizing **ReLU (Rectified Linear Unit)** activation functions across training epochs. 
  > *Design Note:* ReLU was selected because its constant gradient ($\frac{d}{dx}\text{ReLU}(x) = 1$ for $x > 0$) prevents the vanishing gradient problem, ensuring that error updates flow back cleanly through preceding layers during backpropagation.
- **Output Layer (1 Neuron):** Utilizes a **Sigmoid** activation function. This scales the final output strictly between `0` and `1`, representing the exact probability of diabetes risk.

---

##  Key Features

- **Data Preprocessing:** Thorough Exploratory Data Analysis (EDA) to handle missing data, normalize features, and remove anomalies from raw Kaggle data.
- **Optimized Backpropagation:** Custom tuning of activation functions to maintain structural learning consistency.
- **Probability Modeling:** Clear, probabilistic risk analysis instead of a rigid binary threshold.

---

##  Tech Stack

- **Language:** Python
- **Libraries:** NumPy, Pandas (Data Manipulation), Scikit-Learn / TensorFlow / Keras (Model Building & Math operations)
- **Dataset Source:** Kaggle Clinical Records

---

##  Repository Structure

```text
├── data/               # Raw and processed datasets
├── notebooks/          # Jupyter notebooks for EDA and model training
├── src/                # Python scripts for model architecture
├── README.md           # Project documentation
└── requirements.txt    # Dependencies
