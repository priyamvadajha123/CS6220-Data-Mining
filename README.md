# CS 6220 - Data Mining

This repository contains homework assignments for CS 6220: Data Mining.

The assignments are developed using Python and JupyterLab and are run locally on Windows using a Python virtual environment.

## Environment

- Operating System: Windows
- Python: 3.13.9
- JupyterLab: 4.6.3
- NumPy: 2.5.3
- pandas: 3.0.5
- scikit-learn: 1.9.1
- matplotlib: 3.11.2
- seaborn: 0.13.2
- Virtual Environment: Python `venv`



## Setup Instructions

### 1. Clone the Repository

Clone the repository:

```bash
git clone https://github.com/priyamvadajha123/CS6220-Data-Mining
```

Move into the project folder:

```bash
cd CS6220-Data-Mining
```

### 2. Create a Virtual Environment

Create a Python virtual environment inside the project folder:

```bash
python -m venv .venv
```

### 3. Activate the Virtual Environment

On Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

After activation, `(.venv)` should appear at the beginning of the terminal.

### 4. Install the Required Packages

Install the project dependencies from `requirements.txt`:

```bash
python -m pip install -r requirements.txt
```

The current dependencies are:

```text
jupyterlab==4.6.3
numpy==2.5.3
pandas==3.0.5
scikit-learn==1.9.1
matplotlib==3.11.2
seaborn==0.13.2
```

### 5. Start JupyterLab

With the virtual environment activated, start JupyterLab:

```bash
jupyter lab
```

JupyterLab will open in a web browser and run locally on the computer.

## Homework 1

The notebook for Homework 1 is:

`homework_1.ipynb`

Homework 1 uses the Iris flower dataset to build a supervised machine learning pipeline using scikit-learn to predict the flower class.

## Homework 2

The notebook for Homework 2 is:

`homework_2.ipynb`

Homework 2 focuses on implementing and evaluating linear regression and regression trees from scratch using synthetic regression datasets.

The synthetic datasets are generated using known true functions with added random noise.

The main true functions used are:

```text
Linear: f(x) = 2x + 1
Cubic:  f(x) = 0.5x^3 - x^2 + x
f(x) = sin(2πx)
```

## Homework1 Dataset

The Iris dataset used for this homework is from the UCI Machine Learning Repository:
https://archive.ics.uci.edu/dataset/53/iris

The dataset files are stored inside:
```text
data/iris/
```

The folder should contain:

```text
iris.data
iris.names
bezdekIris.data
Index
```

The notebook reads the main dataset from:

`data/iris/iris.data`

The `iris.data` file does not contain a header row, so the following column names are assigned when the file is loaded using pandas:

- `sepal_length`
- `sepal_width`
- `petal_length`
- `petal_width`
- `class`

The first four columns are used as input features and the `class` column is used as the target variable.

## Homework 1 Workflow

The notebook performs the following steps:

1. Import the required Python libraries.
2. Load the Iris dataset using pandas.
3. Assign column names to the dataset.
4. Inspect the dataset.
5. Check the shape of the data.
6. Check the data types.
7. Check for missing values.
8. View descriptive statistics of numerical columns.
9. Check the distribution of the target classes.
10. Separate the input features (`X`) and target (`y`).
11. Split the dataset into 80% training data and 20% test data.
12. Use stratification to maintain the class distribution in both sets.
13. Create a scikit-learn pipeline using `StandardScaler` and `LogisticRegression`.
14. Train the pipeline using the training data.
15. Measure the training time.
16. Make predictions on the test data.
17. Measure the testing time.
18. Calculate the prediction accuracy.

## Running Homework 1

To run Homework 1:

1. Activate the virtual environment.
2. Start JupyterLab.
3. Open `homework_1.ipynb`.
4. Run the notebook cells from top to bottom.

## Homework 2 Workflow

The notebook performs the following steps:
1. Generate synthetic noisy regression datasets.
2. Split each dataset into training and test sets.
3. Implement linear regression from scratch using the closed-form solution.
4. Evaluate linear regression using RMSE.
5. Compare models using only x with models using x, x^2, and x^3.
6. See how increasing polynomial degree affects training and test RMSE.
7. Implement a regression tree from scratch using recursive binary splits.
8. Generate candidate split thresholds using midpoints between consecutive unique feature values.
9. Select the best tree split using variance reduction.
10. se the mean target value of the records in a leaf as the regression-tree prediction.
11. Control tree growth using the min_records hyperparameter.
12. Visualize regression-tree predictions and split locations.
13. Compare regression-tree RMSE with linear-regression RMSE.
14. Analyze the effect of additional polynomial features on regression-tree performance.
15. Analyze tree size using the number of nodes, leaves, and records per leaf.
16. Study the effect of tree size and noise level on model performance.
17. Generate a sinusoidal dataset using f(x) = sin(2πx) with noise level 0.2.
18. Train regression trees using different min_records values.
19. Compare training and test RMSE to study overfitting.
20. Identify the best tree based on test RMSE.
21. Analyze bias and variance for simple and complex regression trees.

## Running Homework 2

To run Homework 2:
1. Activate the virtual environment.
2. Start JupyterLab.
3. Open homework_2.ipynb.
4. Run the notebook cells from top to bottom.