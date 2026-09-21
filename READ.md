Iris Classification

This is a small Machine Learning project I built to practice classification.

The goal is to predict the species of an Iris flower based on its measurements.

Dataset

The Iris dataset contains 150 samples from 3 different species:

* Setosa
* Versicolor
* Virginica

Each sample has 4 features:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

I split the data into:

* 80% training data
* 20% test data

I also used a stratified split to keep the class distribution balanced.

Data Preparation

First, I separated the features and target.

Then I used LabelEncoder to convert the target classes into numbers:

setosa → 0
versicolor → 1
virginica → 2

I also used StandardScaler to scale the features.

Models

I tested several classification models:

* Logistic Regression
* Random Forest
* Gradient Boosting
* MLP Classifier

I used GridSearchCV with 5-fold cross-validation for hyperparameter tuning.

Results

Test set results:

Model	Test Accuracy
Logistic Regression	96%
Random Forest	96.67%
Gradient Boosting	96.67%
MLP	100%

The MLP model achieved 100% accuracy on the test set in this project.

Since the Iris dataset is small and relatively simple, this result should not be considered as 100% performance on real-world data.

New Sample Prediction

After training the model, I created a function for predicting new samples.

For example:

predict_zanbagh(5.1, 3.5, 1.4, 0.2)

Output:

Predicted species: setosa
setosa: 99.12%
versicolor: 0.87%
virginica: 0.01%

What I Practiced

* Train/Test Split
* Label Encoding
* Feature Scaling
* Cross-Validation
* GridSearchCV
* Logistic Regression
* Random Forest
* Gradient Boosting
* MLP
* Accuracy
* Confusion Matrix
* Classification Report
* ROC-AUC
* Prediction on New Data

Libraries

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib

This project was mainly built to practice a complete classification workflow. I plan to apply the same workflow to larger and more realistic datasets in future projects.