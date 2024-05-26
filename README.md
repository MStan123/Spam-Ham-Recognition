This project focuses on recognizing text messages as either Ham or Spam. Various classification algorithms, such as Logistic Regression, Random Forest, SGD and Naive Bayes, have been employed to tackle this problem, and their performance has been analyzed to determine the most effective approach. Also t-SNE method was applied to visualize the performance of these algorithms. 


| Algorithm             | Accuracy | Standard_Scalar() |
|         :---          | :---: |    ---:     |
| Logistic Regression   | 97%   |      +      |
| Random Forest         | 97%   |      +      |
| SGD                   | 97%   |      +      |
| MultinomialNB         | 96%   |      -      |
| BernoulliNB           | 88%   |      -      |
| ComplementNB          | 96%   |      -      |

The dataset was taken from [Kaggle](https://www.kaggle.com/datasets/meruvulikith/190k-spam-ham-email-dataset-for-classification/data).
