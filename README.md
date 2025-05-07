# Human-Activity-Recognition-using-WISDM-Dataset

**This project focuses on classifying different human activities (like walking, jogging, sitting, etc.) using sensor data from the WISDM dataset. The dataset contains accelerometer data collected from smartphones carried in users' pockets while performing various physical activities.**

## 📁 Dataset
The dataset used is from the Wireless Sensor Data Mining (WISDM) lab:

Source: WISDM 

Format: CSV

Attributes:

- User_ID: Identifier of the user

- Activity_Label: Label of the performed activity (Walking, Jogging, etc.)

- Timestamp: Time when reading was captured

- X, Y, Z: Accelerometer readings in three axes

## 🧹  Data Preprocessing
✔️ Steps:
- Removed unnecessary columns (Timestamp, User_ID)

- Cleaned the Z column (removed semicolons and converted to float)

- Handled missing values by replacing with column means

- Normalized X, Y, and Z using Z-score normalization

## 📊  Exploratory Data Analysis (EDA)
📌 Highlights:

- Distribution of activity classes

- Line plots of X, Y, Z accelerations over time for each activity

- Statistical summaries (mean, median, std deviation) for each activity

- Computed acceleration magnitude and visualized its statistics

## 🤖 Model 1 - K-Nearest Neighbors (KNN)
- Implemented KNN classifier using only 3 features: X, Y, and Z

- Achieved maximum accuracy using optimal k (tested from k=4 to k=22)

- Plotted accuracy vs. k to find best performance

- Visualized actual vs predicted classes using scatter plots

## 📦 Model 2 - K-Means Clustering
- Used unsupervised KMeans algorithm to cluster activity types

- Number of clusters = number of activity labels (6)

- Compared clustering results with true labels using confusion matrix

## ⚙️ Model 3 - Support Vector Machine (SVM)
✔️ Steps:
- Used three SVM kernels: linear, polynomial, and rbf

- Due to dataset size, trained on a reduced subset for speed

# Evaluated using:

- Accuracy

- Precision, Recall, F1 Score

- Confusion matrix

- Hyperparameter tuning for RBF kernel using RandomizedSearchCV

## 📈 Performance Metrics
- Compared models using accuracy and classification reports

# Plotted:

- Sigmoid decision boundaries (for logistic regression example)

- Accuracy vs. different k values (KNN)

- Confusion matrix heatmap (for SVM and KMeans)

## 🛠️ Tech Stack

**Language:**  
![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)

**Libraries Used:**  
![Pandas](https://img.shields.io/badge/-Pandas-150458?logo=pandas&logoColor=white)  
![NumPy](https://img.shields.io/badge/-NumPy-013243?logo=numpy&logoColor=white)  
![Matplotlib](https://img.shields.io/badge/-Matplotlib-333?logo=python&logoColor=white)  
![Seaborn](https://img.shields.io/badge/-Seaborn-2E8BC0?logo=python&logoColor=white)  
![Scikit-learn](https://img.shields.io/badge/-Scikit--Learn-F7931E?logo=scikit-learn&logoColor=white)

