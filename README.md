**Programming Assignment**

**Name: Neel Jayeshkumar Suthar**

**UTA ID: 1001807983**

**AIM:**  In this programming assignment I implemented the KNN algorithm from scratch and the functions to evaluate it with a k-fold cross validation (also from scratch). We are supposed to try different distance measures and techniques to get better results from KNN obtained from Weka. Also, I focused on some basic parameters tuning for my KNN.

**Dataset**** :**

For this implementation I have used three datasets from UCI- Machine Learning Repository.

1. Hayes- Roth dataset
2. Car Evaluation dataset
3. Breast Cancer dataset

I have implemented all the dataset in the KNN scratch code and get the accuracy measures from WEKA workbench. During both implementation 10-fold cross validation was used.

**KNN on Hayes-Roth dataset:**

This dataset has only integers values which eases our modification requirements on it. I implemented six distance measures on it including scaling feature for Euclidean distance measure.

First, I tested my KNN using Euclidean distance and I found out the accuracies were lower. I used minmax scaling on my dataset. After applying minmax scaling onto all 10 folds I again tested my KNN using Euclidean distance and I achieved **83.141%** accuracy which was a very good output. After that I tried different k values so I can improve my accuracy even more and as a result I achieved **85.790%** accuracy for **k=3**. By doing minmax scaling and parameter tuning we can get robustness measures.

![](RackMultipart20210131-4-1u1hyna_html_d4e81aec851641e7.png)

I also have tried different distance methods for getting neighbors. I got average accuracies with all other distance measures. I also have tried k-tuning on all different distance measures. You can see results below.

Best accuracy using Normalized Euclidean distance measure.

![](RackMultipart20210131-4-1u1hyna_html_ea8c29c98e534227.png)

Best accuracy using Cosine similarity measur.

![](RackMultipart20210131-4-1u1hyna_html_438edd696d18db0d.png)

Best accuracy using Manhattan distance measure.

![](RackMultipart20210131-4-1u1hyna_html_eaea7b0da65c5133.png)

Best accuracy using Minkowski distance measure.

![](RackMultipart20210131-4-1u1hyna_html_79337fe91f23c9eb.png)

Best accuracy using Hamming distance measure.

![](RackMultipart20210131-4-1u1hyna_html_55dee58713f1e1fe.png)

KNN from Weka gives accuracy shown below.

![](RackMultipart20210131-4-1u1hyna_html_2779a8b2a27df79f.png)

**Implementing Car Evaluation dataset:**

This dataset consists of string values and integer values as well. So, before evaluation of algorithm, all the string values should be converted to integer or float values. For that, **str\_column\_to\_int** function is used.

Then, for 10-fold cross-validation, this dataset gave **96.427%** accuracy with k=7 using Manhattan distance measure

![](RackMultipart20210131-4-1u1hyna_html_eecb59754314fc17.png)

With Minkowski distance measure algorithm was time consuming and because of that I was able to get accuracies for k=1 and k=3

![](RackMultipart20210131-4-1u1hyna_html_1d73ab81c9dfcb02.png)

With hamming distance there was not much difference in accuracy.

![](RackMultipart20210131-4-1u1hyna_html_3b645cb569b2eb41.png)

There are various methods by which we can improve accuracy. Removing some of the data is one of those but I do not think that is a better approach but of course you can do reasoning on deciding columns for classifications and remove some of columns which are less important which will definitely help with distance measures and predictions.

KNN from Weka gives accuracy shown below.

![](RackMultipart20210131-4-1u1hyna_html_a90776f5d2fe7f23.png)

**Implementing Breast-cancer dataset:**

This dataset has to be preprocessed as it contains some string values along with integer values.

For this dataset, KNN using Euclidean distance with k=7 performs **78.464%** accuracy which is best accuracy among all.

![](RackMultipart20210131-4-1u1hyna_html_9be325eea276d0af.png)

Best accuracy using Manhattan Distance and parameter tuning.

![](RackMultipart20210131-4-1u1hyna_html_7a0ffc7753e004d9.png)

Best accuracy using Minkowski Distance and parameter tuning.

![](RackMultipart20210131-4-1u1hyna_html_9f1238b64d613bfa.png)

Best accuracy using Hamming Distance and parameter tuning.

![](RackMultipart20210131-4-1u1hyna_html_13459beb1eb22d20.png)

KNN from Weka gives accuracy shown below.

![](RackMultipart20210131-4-1u1hyna_html_cb960162ce15c96c.png)

**References for KNN and k-fold cross validation:**

[https://machinelearningmastery.com/tutorial-to-implement-k-nearest-neighbors-in-python-from-scratch/](https://machinelearningmastery.com/tutorial-to-implement-k-nearest-neighbors-in-python-from-scratch/)

[https://machinelearningmastery.com/k-fold-cross-validation/](https://machinelearningmastery.com/k-fold-cross-validation/)

With this document file I have attached following python files.

1. Hayes-Roth.ipynb
2. Car.ipynb
3. Breast-Cancer.ipynb