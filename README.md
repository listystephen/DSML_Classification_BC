# DSML_Classification_BC
Classification Problem using breast cancer dataset from sklearn 

**preprocessing steps performed**

Loaded the Dataset Step: Loaded the breast cancer dataset using load_breast_cancer() from sklearn. Reason: The dataset is readily available in sklearn and contains 569 samples, 30 features, and a binary target variable (0: benign, 1: malignant).

Checked for Missing Values Step: Used isnull() to check for missing values in the dataset. No missing values were found. Reason: Missing values can cause errors or biases during model training and evaluation. While this dataset had no missing values, it is a critical step in data preprocessing.

Feature Scaling Step: Scaled the features using StandardScaler, transforming them to have a mean of 0 and a standard deviation of 1.

Reason: Features in the dataset have varying scales. For instance, mean radius has values ranging from 6 to 30, while mean fractal dimension ranges from 0.05 to 0.2. Scaling ensures that all features contribute equally to the model and improves the performance of distance-based algorithms (e.g., KNN) and gradient-based optimizers (e.g., Logistic Regression, SVM).


**Algorithms used :  how it works and why it might be suitable for this dataset?**

Logistic Regression Description Logistic Regression is a linear model that predicts probabilities of binary outcomes using the logistic function. It models the relationship between input features and the probability of the target class. The dataset is relatively small and balanced, making Logistic Regression a good baseline model. Logistic Regression works well with linearly separable data, and this dataset might have linearly separable classes after scaling.

Decision Tree Classifier Description Decision Trees split the data into subsets based on feature thresholds, forming a tree-like structure. At each node, the algorithm chooses the split that minimizes impurity (e.g., Gini index or entropy).

Decision Trees handle non-linear relationships well. They can work with unscaled data, although scaling is not a drawback.

Random Forest Classifier Description Random Forest is an ensemble learning method that builds multiple Decision Trees and combines their outputs (voting for classification). It reduces overfitting compared to a single Decision Tree.
Random Forest performs well on structured/tabular data. It handles both linear and non-linear relationships effectively and is robust to noise.

Support Vector Machine (SVM) Description SVM finds a hyperplane that maximizes the margin between two classes. It uses kernel functions to handle non-linear data.
SVM is effective in high-dimensional spaces and works well for datasets with a clear margin of separation. Scaling is crucial for SVM, and the dataset has already been scaled.

k-Nearest Neighbors (k-NN) Description k-NN is a non-parametric algorithm that classifies a data point based on the majority class of its k nearest neighbors. Distance metrics (e.g., Euclidean) are used to find the neighbors.
k-NN is simple and effective for smaller datasets. It benefits from feature scaling, which ensures fair distance calculations.

**comparing the accuracy of each algorithms**

Logistic Regression: 0.9561
Decision Tree: 0.9474
Random Forest: 0.9649
Support Vector Machine: 0.9561
k-Nearest Neighbors: 0.9561

Best Performing Model: Random Forest (0.9649)
least Performing Model: Decision Tree (0.9474)
