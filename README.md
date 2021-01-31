# Get started:

- Download notebook files(.ipynb file) along with all the csv files.
- Upload it on Google colab and just run it 😊.

# Dataset:

For this implementation I have used three datasets from UCI- Machine Learning Repository.

1. Hayes- Roth dataset
2. Car Evaluation dataset
3. Breast Cancer dataset

I have implemented all the dataset in the KNN scratch code and get the accuracy measures from WEKA workbench. During both implementation 10-fold cross validation was used.

# KNN on Hayes-Roth dataset:

This dataset has only integers values which eases our modification requirements on it. I implemented six distance measures on it including scaling feature for Euclidean distance measure.

First, I tested my KNN using Euclidean distance and I found out the accuracies were lower. I used minmax scaling on my dataset. After applying minmax scaling onto all 10 folds I again tested my KNN using Euclidean distance and I achieved **83.141%** accuracy which was a very good output. After that I tried different k values so I can improve my accuracy even more and as a result I achieved **85.790%** accuracy for **k=3**. By doing minmax scaling and parameter tuning we can get robustness measures.

# Implementing Car Evaluation dataset:

This dataset consists of string values and integer values as well. So, before evaluation of algorithm, all the string values should be converted to integer or float values. For that, **str\_column\_to\_int** function is used.

Then, for 10-fold cross-validation, this dataset gave **96.427%** accuracy with k=7 using Manhattan distance measure

There are various methods by which we can improve accuracy. Removing some of the data is one of those but I do not think that is a better approach but of course you can do reasoning on deciding columns for classifications and remove some of columns which are less important which will definitely help with distance measures and predictions.

# Implementing Breast-cancer dataset:

This dataset has to be preprocessed as it contains some string values along with integer values.

For this dataset, KNN using Euclidean distance with k=7 performs **78.464%** accuracy which is best accuracy among all.

# References for KNN and k-fold cross validation:

[https://machinelearningmastery.com/tutorial-to-implement-k-nearest-neighbors-in-python-from-scratch/](https://machinelearningmastery.com/tutorial-to-implement-k-nearest-neighbors-in-python-from-scratch/)

[https://machinelearningmastery.com/k-fold-cross-validation/](https://machinelearningmastery.com/k-fold-cross-validation/)
