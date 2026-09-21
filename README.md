Iris ML Classification

A machine learning classification project for predicting Iris flower species using different classification algorithms.

Project Overview

In this project, the goal is to classify Iris flowers into three species based on four numerical features:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

The target classes are:

* Setosa
* Versicolor
* Virginica

Dataset

The dataset contains 150 Iris flower samples with:

* 4 input features
* 3 target classes
* 50 samples per class

The target variable (species) was encoded using LabelEncoder:

setosa → 0
versicolor → 1
virginica → 2

Data Preprocessing

The following preprocessing steps were performed:

1. Separated features (X) and target (y)
2. Encoded the categorical target using LabelEncoder
3. Split the dataset into training and testing sets
4. Used stratify=y to preserve class proportions
5. Applied StandardScaler to the input features
6. Used the same fitted scaler when predicting new samples

The dataset was split into:

* 80% Training → 120 samples
* 20% Testing → 30 samples

Models

Several classification algorithms were trained and evaluated:

* Logistic Regression
* Random Forest
* Gradient Boosting
* MLP Classifier

For the models, GridSearchCV with 5-fold cross-validation was used to search for suitable hyperparameters.

Hyperparameter Tuning

Logistic Regression

The C parameter was tuned using:

[0.01, 0.1, 1, 10, 100]

Best parameter:

C = 1

Best cross-validation accuracy:

96.67%

Random Forest

The following hyperparameters were tuned:

* n_estimators
* max_depth
* min_samples_split
* min_samples_leaf

The final test accuracy was:

96.67%

Gradient Boosting

The following hyperparameters were tuned:

* n_estimators
* learning_rate
* max_depth

The final test accuracy was:

96.67%

MLP Classifier

The following hyperparameters were tuned:

* hidden_layer_sizes
* activation
* alpha
* learning_rate_init

Best parameters:

activation = relu
hidden_layer_sizes = (10,)
alpha = 0.0001
learning_rate_init = 0.01

Best cross-validation accuracy:

97.5%

Final test accuracy:

100%

The final test set contained 30 samples.

Model Evaluation

The models were evaluated using:

* Accuracy
* Confusion Matrix
* Classification Report
* Cross-Validation
* ROC-AUC

For Logistic Regression, ROC-AUC was also calculated using the One-vs-Rest approach.

New Sample Prediction

After training the models, a prediction function was created to classify completely new Iris samples.

Example:

predict_zanbagh(5.1, 3.5, 1.4, 0.2)

Example output:

Predicted species: setosa
setosa: 99.12%
versicolor: 0.87%
virginica: 0.01%

The prediction function:

1. Receives the four flower measurements
2. Applies the same scaler used during training
3. Uses the trained MLP model for prediction
4. Converts the predicted class number back to the original species name
5. Displays the predicted probability for each class

Technologies & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

Main Scikit-learn components used:

* LabelEncoder
* StandardScaler
* train_test_split
* GridSearchCV
* LogisticRegression
* RandomForestClassifier
* GradientBoostingClassifier
* MLPClassifier
* accuracy_score
* classification_report
* confusion_matrix
* roc_auc_score

Project Workflow

Raw Dataset
     ↓
Feature / Target Separation
     ↓
Label Encoding
     ↓
Train / Test Split
     ↓
Feature Scaling
     ↓
Model Training
     ↓
5-Fold Cross-Validation
     ↓
GridSearchCV
     ↓
Best Model Selection
     ↓
Test Set Evaluation
     ↓
New Sample Prediction

Results

Model	Cross-Validation / GridSearch	Test Accuracy
Logistic Regression	96.67%	96%
Random Forest	—	96.67%
Gradient Boosting	—	96.67%
MLP Classifier	97.5%	100%

Note: The reported test results are based on a single 80/20 train-test split of the Iris dataset. The Iris dataset is small and relatively easy to classify, so these results should not be interpreted as evidence of equivalent real-world performance on more complex datasets.

What I Practiced

This project was used to practice an end-to-end machine learning classification workflow, including:

* Data preprocessing
* Train/Test Split
* Feature Scaling
* Label Encoding
* Cross-Validation
* Hyperparameter Tuning
* GridSearchCV
* Classification Metrics
* Model Comparison
* Probability Prediction
* Prediction on New Data

Future Improvements

Possible next steps include:

* Testing SVM / SVC
* Visualizing the decision boundaries
* Improving the project structure
* Saving the trained model
* Building a simple prediction interface
* Applying the same workflow to a larger real-world dataset
