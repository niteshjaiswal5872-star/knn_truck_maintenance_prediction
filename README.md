# Truck Maintenance Prediction: Logistic Regression vs KNN

## Project Overview

This project uses supervised Machine Learning to predict whether a truck requires maintenance based on information about the truck and its operating conditions.

Two classification algorithms are implemented and compared:

* Logistic Regression
* K-Nearest Neighbors (KNN)

The purpose of the project is to understand how different classification algorithms perform on the same dataset.

## Objective

The objective is to predict whether maintenance is required for a truck.

The target variable is:

`Maintenance_Needed`

It contains two classes:

* `Yes` = 1
* `No` = 0

## Dataset

The dataset contains information about truck usage and maintenance.

### Features

* `Mileage_km`
* `Engine_Hours`
* `Truck_Age_Years`
* `Previous_Repairs`
* `Load_Weight_Tons`
* `Average_Speed_kmh`
* `Days_Since_Last_Service`
* `Fuel_Type`

### Target

`Maintenance_Needed`

## Data Preprocessing

The raw dataset contains missing values and duplicate records.

The following preprocessing steps were performed:

1. Loaded the dataset using Pandas.
2. Checked for missing values.
3. Removed rows where the target variable was missing.
4. Filled missing numerical values using the mean.
5. Filled missing `Fuel_Type` values using the mode.
6. Removed duplicate rows.
7. Converted `Maintenance_Needed` from `Yes/No` to `1/0`.
8. Converted `Fuel_Type` into numerical values using one-hot encoding.
9. Removed `Truck_ID` because it is only an identifier.
10. Split the data into training and testing sets.
11. Applied feature scaling using `StandardScaler` for KNN.

## Machine Learning Models

### 1. Logistic Regression

Logistic Regression is a supervised classification algorithm used to predict categorical outcomes.

In this project, it predicts whether:

* `0` = Maintenance is not needed
* `1` = Maintenance is needed

Logistic Regression provides a simple baseline model for comparison.

### 2. K-Nearest Neighbors

KNN is a classification algorithm that makes predictions based on the nearest data points.

The model uses:

`n_neighbors = 5`

This means that the model considers the 5 nearest training examples when making a prediction.

Feature scaling is important for KNN because it uses distance calculations.

## Train-Test Split

The dataset is divided into:

* 80% training data
* 20% testing data

The training data is used to train the models, while the testing data is used to evaluate their performance.

## Model Evaluation

Both models are evaluated using:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1 Score

## Model Comparison

After running both models, their performance can be compared using their test accuracy.

| Model               |        Accuracy |
| ------------------- | --------------: |
| Logistic Regression | Add your result |
| KNN                 | Add your result |

The model with the better performance on the test dataset can be considered the better model for this particular dataset.

However, accuracy alone should not be used to select a model. Precision, recall, F1-score, and the confusion matrix should also be considered.

## Logistic Regression vs KNN

| Feature              | Logistic Regression        | KNN                     |
| -------------------- | -------------------------- | ----------------------- |
| Type                 | Classification             | Classification          |
| Learning approach    | Learns a decision boundary | Uses nearby data points |
| Distance calculation | No                         | Yes                     |
| Feature scaling      | Usually not required       | Important               |
| Easy to understand   | Yes                        | Yes                     |
| Main parameter       | Model coefficients         | Number of neighbors (K) |

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
Truck-Maintenance-Prediction/
│
├── truck_maintenance_dataset.csv
├── logistic_regression.ipynb
├── knn_model.ipynb
├── README.md
└── requirements.txt
```

## How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open the Jupyter notebooks.
4. Make sure the CSV dataset is in the correct folder.
5. Run the preprocessing and Machine Learning cells.
6. Check the model evaluation results.
7. Compare Logistic Regression and KNN.

## Future Improvements

The project can be extended by testing additional classification algorithms, such as:

* Decision Tree
* Random Forest
* Support Vector Machine
* Naive Bayes

The models can then be compared using multiple evaluation metrics.

Hyperparameter tuning can also be performed to find the best value of K for KNN.

## Conclusion

This project demonstrates how supervised Machine Learning can be used to predict truck maintenance requirements.

Logistic Regression and KNN were implemented on the same dataset and evaluated using multiple classification metrics.

The comparison helps understand how different Machine Learning algorithms perform on the same classification problem.
