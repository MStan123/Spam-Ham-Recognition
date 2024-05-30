This project focuses on recognizing text messages as either Ham or Spam. Various classification algorithms, such as Logistic Regression, Random Forest, SGD and Naive Bayes, have been employed to tackle this problem, and their performance has been analyzed to determine the most effective approach. Also t-SNE method was applied to visualize the performance of these algorithms. 


| Algorithm             | Accuracy | Standard_Scalar() | Training Time | Dataset Size |
|         :---          | :---: |    :---:    | :---:  | :---: | ---:|
| SVM                   | 95%   |      +      | 67 min | 50K |
| Logistic Regression   | 97%   |      +      | 86.42 sec.| 193K 
| Random Forest         | 97%   |      +      | 36 min. 16 sec. | 193K |
| SGD                   | 97%   |      +      | 5.13 sec. | 193K |
| MultinomialNB         | 96%   |      -      | 1.63 sec. | 193K |
| BernoulliNB           | 88%   |      -      | 1.73 sec. | 193K |
| ComplementNB          | 96%   |      -      | 2.02 sec. | 193K |

The dataset was taken from [Kaggle](https://www.kaggle.com/datasets/meruvulikith/190k-spam-ham-email-dataset-for-classification/data).
