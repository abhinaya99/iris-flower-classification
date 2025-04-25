# iris-flower-classification
Iris flower classification using various machine learning models.

## Task Objectives

This project develops a machine learning model to accurately identify Iris flower species (Setosa, Versicolor, Virginica) based on sepal and petal measurements. The goal is to explore and evaluate different classification algorithms to achieve high species identification accuracy.

## Steps to Run Your Project

1. **Prerequisites:**
     Python 3.x
     Ensure the following Python libraries are installed:
        ```bash
        pip install pandas scikit-learn matplotlib seaborn
        ```
2.  **Execution:**
    * If you are using a Jupyter Notebook: "Open the `iris_classification_acc(1).ipynb` file and run all cells."
    * If you are using a Python script: "Navigate to the project directory in your terminal and run: `python iris_classification_acc(1).py`."

## Preprocessing Details

* The Iris dataset was loaded from `scikit-learn`.
* The data was split into training and testing sets using `train_test_split` with a `test_size` of 0.3 and `random_state` of 42 for reproducibility.
* Features (sepal length, sepal width, petal length, petal width) were scaled using `StandardScaler` to have zero mean and unit variance. This was important for algorithms like Logistic Regression, SVM, and MLP. Random Forest was also evaluated without explicit scaling as it is generally less sensitive to feature scales.

## Model Selection and Evaluation

The following machine learning models were implemented and evaluated:

* **Logistic Regression:** Achieved an accuracy of 0.9111 on the test set. The classification report and confusion matrix provide further details on the model's performance across different species. Feature importance analysis based on the model coefficients suggests that petal length and petal width were among the most influential features.
* **Support Vector Machine (SVM):** Achieved an accuracy of 1.0000 on the test set using an RBF kernel with C=1.0. The model perfectly classified all instances in the test set.
* **K-Nearest Neighbors (KNN):** Achieved an accuracy of 1.0000 on the test set with `n_neighbors` set to 5. The model perfectly classified all instances in the test set.
* **Random Forest:** Achieved an accuracy of 1.0000 on the test set with `n_estimators` set to 100. Feature importance analysis revealed that petal length and petal width were the most important features for this model.
* **Multilayer Perceptron (MLP):** Achieved an accuracy of 1.0000 on the test set with `hidden_layer_sizes` set to (10, 10) and `max_iter` of 300 using the 'adam' solver. The model perfectly classified all instances in the test set.

The models with the highest accuracy were Support Vector Machine (SVM), K-Nearest Neighbors (KNN), Random Forest, and Multilayer Perceptron (MLP), all achieving an accuracy of 1.0000.

## Feature Significance

Based on the analysis of Logistic Regression and Random Forest, petal length and petal width appear to be the most significant features influencing the Iris species classification. These features likely provide the clearest distinction between the different flower types.

## Code Quality

The code is structured into logical sections for data loading, preprocessing, model implementation, training, and evaluation. Comments are included to explain key steps and functionalities, aiming for readability and maintainability.
