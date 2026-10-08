# Iris Flower Classification 🌸

## Project Overview

This project focuses on classifying Iris flowers into three different species using **Machine Learning with Python**. The classification is performed using the measurements of the flower's sepal and petal dimensions.

The project uses **Logistic Regression** to predict the species of an Iris flower based on four numerical features.

## Dataset

The dataset contains **150 records** and the following columns:

* `Id`
* `SepalLengthCm`
* `SepalWidthCm`
* `PetalLengthCm`
* `PetalWidthCm`
* `Species`

The target variable contains three classes:

* Iris-setosa
* Iris-versicolor
* Iris-virginica

The notebook confirms that all 150 records contain non-null values and there are no duplicate rows.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Machine Learning Workflow

The project follows these steps:

1. Import required libraries
2. Load the Iris dataset
3. Explore the dataset
4. Check data types and missing values
5. Check for duplicate records
6. Select input features and target variable
7. Split the dataset into training and testing sets
8. Create the Logistic Regression model
9. Train the model
10. Make predictions
11. Evaluate model accuracy
12. Generate a classification report
13. Generate a confusion matrix

## Features

The following four features are used for prediction:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

The `Species` column is used as the target variable.

## Train-Test Split

The dataset is divided into:

* **80% Training Data**
* **20% Testing Data**

The split uses `random_state=42` and stratification based on the target classes.

## Machine Learning Model

### Logistic Regression

The project uses Logistic Regression for multiclass classification.

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression(max_iter=200)
model.fit(X_train, y_train)
```

The trained model is then used to predict the species of flowers in the test dataset.

## Model Evaluation

The model achieved:

**Accuracy: 96.67%**

The test set contains 30 observations.

### Classification Report

| Class           | Precision | Recall | F1-Score |
| --------------- | --------: | -----: | -------: |
| Iris-setosa     |      1.00 |   1.00 |     1.00 |
| Iris-versicolor |      1.00 |   0.90 |     0.95 |
| Iris-virginica  |      0.91 |   1.00 |     0.95 |

Overall accuracy is approximately **97%** on the test set.

### Confusion Matrix

```text
[[10  0  0]
 [ 0  9  1]
 [ 0  0 10]]
```

The confusion matrix shows that most test samples were correctly classified, with only one `Iris-versicolor` sample classified differently.

## Results

The Logistic Regression model performed well on the Iris classification task, achieving **96.67% test accuracy**.

The model correctly identifies all tested `Iris-setosa` and `Iris-virginica` samples, while one `Iris-versicolor` sample was misclassified.

## Project Structure

```text
Iris-Flower-Classification/
│
├── Iris Flower Classification.ipynb
├── Iris.csv
├── README.md
└── requirements.txt
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the project folder

```bash
cd Iris-Flower-Classification
```

### 3. Create a virtual environment

```bash
python -m venv .venv
```

### 4. Activate the virtual environment

**Windows:**

```bash
.venv\Scripts\activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Start Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Iris Flower Classification.ipynb
```

## Conclusion

This project demonstrates an end-to-end machine learning classification workflow using the Iris dataset. Logistic Regression successfully classified the three Iris species with **96.67% accuracy**, demonstrating that the selected sepal and petal measurements provide useful information for species classification.

## Author

**Seelam Anil Reddy**

Aspiring Data Scientist | Python Developer

GitHub: [anilreddy-043](https://github.com/anilreddy-043)
