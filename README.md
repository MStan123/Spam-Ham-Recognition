This project focuses on recognizing text messages as either Ham or Spam. Various classification algorithms, such as Logistic Regression, Random Forest, SGD and Naive Bayes, have been employed to tackle this problem, and their performance has been analyzed to determine the most effective approach. Also t-SNE method was applied to visualize the performance of these algorithms. 


| Algorithm             | Accuracy | Standard Scaler | Training Time  | Dataset Size | Hyperparameters |
|-----------------------|:--------:|:---------------:|:--------------:|:------------:|:----------------|
| SVM                   | 95%      | Yes             | 67 min         | 50K          | kernel='linear' |
| Logistic Regression   | 97%      | Yes             | 86.42 sec      | 193K         | -               |
| Random Forest         | 97%      | Yes             | 36 min 16 sec  | 193K         | n_estimators=30, random_state=42 |
| SGD                   | 97%      | Yes             | 5.13 sec       | 193K         | loss='log_loss', alpha=0.01, max_iter=1000, random_state=42 |
| MultinomialNB         | 96%      | No              | 1.63 sec       | 193K         | -               |
| BernoulliNB           | 88%      | No              | 1.73 sec       | 193K         | -               |
| ComplementNB          | 96%      | No              | 2.02 sec       | 193K         | -               |
| CatBoost              | 88%      | Yes             | 25 min         | 100K         | iterations=200, learning_rate=0.01, depth=6, l2_leaf_reg=3, early_stopping_rounds=10 |

The dataset was taken from [Kaggle](https://www.kaggle.com/datasets/meruvulikith/190k-spam-ham-email-dataset-for-classification/data).

# Algorithms Overview
## SVM
Support Vector Machine (SVM) is a supervised machine learning algorithm used for both classification and regression. SVMs can be used for a variety of tasks, such as 
1. text classification
2. image classification
3. spam detection
4. handwriting identification
5. gene expression analysis
6. face detection
7. anomaly detection

SVMs are adaptable and efficient in a variety of applications because they can manage high-dimensional data and nonlinear relationships. The main objective of the SVM
algorithm is to find the optimal hyperplane in an N-dimensional space that can separate the data points in different classes in the feature space.

### Types of Support Vector Machine
1. **Linear SVM:** use a linear decision boundary to separate the data points of different classes. When the data can be precisely linearly separated, linear SVMs are very suitable.
2. **Non-Linear SVM:** can be used to classify data when it cannot be separated into two classes by a straight line (in the case of 2D). By using kernel functions, nonlinear SVMs can handle nonlinearly separable data. The original input data is transformed by these kernel functions into a higher-dimensional feature space, where the data points can be linearly separated. A linear SVM is used to locate a nonlinear decision boundary in this modified space.

**Kernel functions:**
1. Linear: $w^{T}x + b$
2. Polynomial: $(\gamma w^{T}x + b)^{N}$
3. Gaussian RBF: $exp(-\gamma||x_i - x_j||^n)$
4. Sigmoid: $tanh(\alpha x_i^Tx_j + b)$
