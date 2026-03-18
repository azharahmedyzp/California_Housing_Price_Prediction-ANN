# California Housing Price Prediction using ANN

This repository contains a project that implements an **Artificial Neural Network (ANN)** to predict housing prices in California using the **California Housing dataset**. The model demonstrates key deep learning concepts such as data preprocessing, feature scaling, hidden layers, activation functions, dropout regularization, and early stopping.

---

## 🏗️ Project Overview

The goal of this project is to build a neural network that can accurately predict median house prices based on features like income, house age, number of rooms, and more. 

The project highlights:
- **Data preprocessing** (scaling features and target variable)
- **ANN design and training**
- **Evaluation using Mean Squared Error (MSE)**
- **Visualization of training and validation loss**

---

## 🧰 Technologies Used

- Python 3.x  
- [NumPy](https://numpy.org/) – numerical computations  
- [scikit-learn](https://scikit-learn.org/) – dataset loading, preprocessing, scaling, and evaluation  
- [TensorFlow / Keras](https://www.tensorflow.org/) – building and training the ANN  
- [Matplotlib](https://matplotlib.org/) – visualization of training progress  

---

## 🔹 Data Preprocessing

1. **Loading Dataset:** California Housing dataset from `sklearn.datasets`.
2. **Train-Test Split:** 80% training, 20% testing.
3. **Feature Scaling:** Standardization of features and target variable using `StandardScaler`.
4. **Handling Missing Values:** Dataset contains no missing values.
5. **Encoding:** Not required as all features are numeric.

---

## 🧠 ANN Architecture

The neural network is designed as follows:

| Layer | Neurons | Activation | Notes |
|-------|---------|-----------|-------|
| Input | 8       | –         | 8 features from dataset |
| Hidden Layer 1 | 128     | ReLU      | Captures complex patterns |
| Dropout 1 | –       | –         | 10% neurons dropped |
| Hidden Layer 2 | 64      | ReLU      | Refines learned patterns |
| Dropout 2 | –       | –         | Regularization |
| Output Layer | 1       | Linear    | Predicts continuous house price |

**Highlights:**
- **ReLU** used in hidden layers for non-linearity and fast convergence
- **Linear activation** in output layer for regression
- **Dropout layers** prevent overfitting

---

## ⚡ Training Details

- **Loss Function:** Mean Squared Error (MSE)  
  \[
  MSE = \frac{1}{n} \sum (y_{true} - y_{pred})^2
  \]
- **Optimizer:** Adam – adaptive learning with momentum
- **Batch Size:** 32  
- **Epochs:** 200 (with EarlyStopping to prevent overfitting)  
- **Validation Split:** 20%

---

## 📊 Evaluation

- **Metric:** Mean Squared Error (MSE) on test set  
- The model shows steady learning with minimal overfitting, as observed in training vs validation loss curves.  
- Dropout and early stopping contributed to good generalization.

---

## ✅ Conclusion

This project demonstrates how an ANN can be used for **regression tasks on tabular data**.
Key takeaways:

* Data scaling improves training efficiency.
* Dropout and early stopping help prevent overfitting.
* Proper ANN design with suitable activation functions and optimizers can achieve reliable predictions.

---

## 📖 References

* [California Housing Dataset – scikit-learn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_california_housing.html)
* [Keras Sequential API](https://www.tensorflow.org/guide/keras/sequential_model)
* [Dropout Regularization in Neural Networks](https://www.tensorflow.org/tutorials/keras/regression)

```

---
