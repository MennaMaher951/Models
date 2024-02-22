SVM Classifier Implementation
This repository contains an implementation of a Support Vector Machine (SVM) classifier in Python using NumPy. It offers functionalities for model fitting, prediction, and evaluation.

Features:

Implements SVM classifier with hinge loss and L2 regularization.
Employs gradient descent optimization for learning.
Includes functions for fitting, predicting, and evaluating model performance.
Demonstrates how to use the model for prediction on new data.
Usage:

Clone the repository: git clone https://github.com/your_username/svm-classifier-scratch.git
Install dependencies: pip install numpy
Import the SVM_classifier class from svm_classifier.py.
Create an instance of the class with desired hyperparameters (learning rate, iterations, lambda).
Call the fit method with your training data (features and target variable).
Use the predict method to make predictions on new data.
Example Usage:

Python
# Import and create the classifier
from svm_classifier import SVM_classifier

# Hyperparameters
learning_rate = 0.001
no_of_iterations = 1000
lambda_parameter = 0.01

# Load data (replace with your data)
dataset = pd.read_csv("diabetes.csv")
x = dataset.drop(columns="Outcome", axis=1)
y = dataset["Outcome"]

# Train-test split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)

# Create and fit the model
model = SVM_classifier(learning_rate, no_of_iterations, lambda_parameter)
model.fit(x_train, y_train)

# Evaluate on training and test data
train_accuracy = model.evaluate(x_train, y_train)
test_accuracy = model.evaluate(x_test, y_test)
print("Training accuracy:", train_accuracy)
print("Test accuracy:", test_accuracy)

# Predict on new data
new_data = [3, 102, 44, 20, 94, 30.8, 0.4, 26]  # Replace with your data
prediction = model.predict(new_data)
print("Prediction:", prediction)

Explanation:

The SVM_classifier class initializes with hyperparameters (learning_rate, no_of_iterations, and lambda_parameter).
The fit method iteratively performs gradient descent to update the model weights and bias based on the training data.
The predict method uses the learned weights and bias to classify new data points.
The evaluate method calculates the accuracy of the model on a given dataset.

Further Exploration:

Modify the hyperparameters and observe their impact on performance.
Experiment with different datasets and evaluate model accuracy using other metrics.
Compare this implementation with other SVM libraries for benchmarking.

Author
Menna Maher