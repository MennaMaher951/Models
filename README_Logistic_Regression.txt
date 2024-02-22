Logistic Regression Implementation from Scratch
This repository contains an implementation of Logistic Regression built from scratch in Python using NumPy. It includes functionalities for model fitting, prediction, and evaluation, along with comments and explanations for understanding the algorithm.

Features
Implements Logistic Regression with sigmoid function and gradient descent optimization.
Provides clear comments and explanations within the code for understanding.
Includes functionalities for model fitting, prediction, and accuracy evaluation.
Demonstrates how to use the model for prediction on new data.

Usage
Clone the repository: git clone https://github.com/your_username/logistic-regression-scratch.git
Install dependencies: pip install numpy
Import the Logistic_Regression class from logistic_regression.py.
Create an instance of the class with desired hyperparameters (learning rate, iterations).
Call the fit method with your training data (features and target variable).
Use the predict method to make predictions on new data.

Example Usage

Python
from logistic_regression import Logistic_Regression

# Hyperparameters
learning_rate = 0.01
no_of_iterations = 1000

# Load data (replace with your data)
dataset = pd.read_csv("diabetes.csv")
x = dataset.drop(columns='Outcome', axis=1)
y = dataset['Outcome']

# Train-test split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)

# Create and fit the model
model = Logistic_Regression(learning_rate, no_of_iterations)
model.fit(x_train, y_train)

# Evaluate on training and test data
train_accuracy = model.evaluate(x_train, y_train)
test_accuracy = model.evaluate(x_test, y_test)
print("Training accuracy:", train_accuracy)
print("Test accuracy:", test_accuracy)

# Make prediction on new data
new_data = [3, 102, 44, 20, 94, 30.8, 0.4, 26]  # Replace with your input data
prediction = model.predict(new_data)
if prediction == 0:
    print("The person is not diabetic.")
else:
    print("The person is diabetic.")

Further Exploration
Modify the hyperparameters and observe their impact on performance.
Experiment with different datasets and evaluate model accuracy using other metrics.
Compare this implementation with other Logistic Regression libraries for benchmarking.

Author
Menna Maher