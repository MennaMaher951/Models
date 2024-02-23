## Lasso Regression Implementation from Scratch
* This repository contains an implementation of Lasso Regression built from scratch in Python using NumPy. It includes functionalities for model fitting and prediction, along with comments and explanations for understanding the algorithm.

*Features*
1. Implementations of both model fitting and prediction functionalities.
2. Utilizes gradient descent algorithm for optimization.
3. Includes clear comments and explanations within the code.
4. Easy to understand and modify for further exploration.

*Usage*
1. Clone the repository: git clone https://github.com/your_username/lasso-regression-scratch.git
2. Install dependencies: pip install numpy
3. Import the Lasso_Regression class from lasso_regression.py.
4. Create an instance of the class with desired hyperparameters (learning rate, iterations, lambda parameter).
5. Call the fit method with your training data (features and target variable).
6. Use the predict method to make predictions on new data.

*Example*

from lasso_regression import Lasso_Regression

# Hyperparameters
learning_rate = 0.01
no_of_iterations = 1000
lambda_parameter = 0.1

# Load data (replace with your data)
X = ...  # Features
y = ...  # Target variable

# Create and fit the model
model = Lasso_Regression(learning_rate, no_of_iterations, lambda_parameter)
model.fit(X, y)

# Make predictions
predictions = model.predict(X_new)

*Author*
Menna Maher
