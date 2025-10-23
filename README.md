# Housing

# Linear Regression Analysis Project

## Project Goal

The primary objective of this project was to implement and evaluate a **Simple Linear Regression** model using a small, structured dataset. The goal was to understand the fundamental steps of the machine learning pipeline: data preparation, model training, performance evaluation, and result interpretation.

## Technology Stack

This project relies on the following core Python libraries:

* **Pandas:** For data loading, manipulation, and preprocessing.
* **Scikit-learn (`sklearn`):** For splitting the data, fitting the Linear Regression model, and calculating performance metrics.
* **NumPy:** For numerical operations and array handling.
* **Matplotlib:** For visualizing the data and the final regression line.

## Data and Features

The model was built using the following relationship:

| Variable | Type | Role in Model |
| :--- | :--- | :--- |
| **`Feature_X`** | Continuous | **Independent Variable (Predictor)** |
| **`Target_Y`** | Continuous | **Dependent Variable (Target)** |

*Initial data inspection confirmed **zero missing values** for both features, allowing us to proceed directly to the train-test split.*

## Model Implementation Steps

1.  **Import & Preprocess:** Loaded the data into a Pandas DataFrame and confirmed data cleanliness (no missing values).
2.  **Train-Test Split:** The dataset was split into training and testing sets using an **80% (Training) / 20% (Testing)** ratio.
3.  **Model Fitting:** An instance of `sklearn.linear_model.LinearRegression` was created and trained (`.fit()`) on the training data (`X_train` and `y_train`).
4.  **Prediction:** Predictions were generated on the unseen test data (`X_test`).
5.  **Evaluation & Interpretation:** Calculated performance metrics and extracted model coefficients.

## Results and Analysis

### **1. Model Performance**

The model was evaluated on the test set (20 samples) using standard regression metrics.

| Metric | Value | Interpretation |
| :--- | :--- | :--- |
| **R-squared Score ($R^2$)** | **0.8072** | The model explains **~80.72%** of the variance in the Target\_Y, indicating a strong fit. |
| **Mean Absolute Error (MAE)** | **0.5913** | On average, predictions were off by **0.59 units**. |
| **Mean Squared Error (MSE)** | **0.6537** | Used to penalize larger errors more heavily. |

### **2. Model Equation and Interpretation**

The fitted Linear Regression model yielded the following parameters, defining the line of best fit:

| Parameter | Value |
| :--- | :--- |
| **Intercept ($\mathbf{b_0}$)** | **4.1429** |
| **Coefficient ($\mathbf{b_1}$)** | **2.7993** |

The final model equation is:

$$\mathbf{Target\_Y} = 4.1429 + 2.7993 \times \mathbf{Feature\_X}$$

**Interpretation:**
For every **1-unit increase in Feature\_X**, the Target\_Y is predicted to increase by **2.7993 units**.

## Visual Output

<img width="687" height="547" alt="image" src="https://github.com/user-attachments/assets/fd7516dd-a761-496e-8d88-48583fbb00e5" />




The plot visually confirms that the model's regression line successfully captures the positive, linear trend between the two variables.
