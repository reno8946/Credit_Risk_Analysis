# Credit_Risk_Analysis

## Overview of the analysis:

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. The objective is to flag as many high-risk loan outcomes as possible.

## Results: 

* Balanced Random Forest Classifier- While the balanced accuracy score was pretty solid at ~79%, the model was very precise at predicting low risk outcomes, but very unprecise at predicting high risk outcomes with only 3% precision. Overall, it was decent in terms of recall with over 70% for both outcomes

![image](https://user-images.githubusercontent.com/70483866/104131993-fc8bd680-533f-11eb-8cdd-7d6f0522e664.png)

* Easy Ensemble AdaBoost Classifier- While the balanced accuracy score was very high at ~93%, the model was very precise at predicting low risk outcomes, but very unprecise at predicting high risk outcomes with only 9% precision. In terms of recall, it was very high with over 90% for both outcomes

![image](https://user-images.githubusercontent.com/70483866/104132026-470d5300-5340-11eb-9c4d-0e8a9631fe75.png)

* Naive Random Oversampling- While the balanced accuracy score was not that great at only ~66%, the model was very precise at predicting low risk outcomes, but very unprecise at predicting high risk outcomes with only 1% precision. Overall, in terms of recall it was quite low with over 74% for high risk outcomes and 58% for low risk outcomes

![image](https://user-images.githubusercontent.com/70483866/104132060-9489c000-5340-11eb-8978-5b01ccea625e.png)

* Smote Oversampling- While the balanced accuracy score was not that great at only ~65%, the model was very precise at predicting low risk outcomes, but very unprecise at predicting high risk outcomes with only 1% precision. Overall, in terms of recall it was quite low with no greater tghan 68% for both outcomes

![image](https://user-images.githubusercontent.com/70483866/104132121-f4806680-5340-11eb-810c-94373ddfd86e.png)

* Cluster Centroids Undersampling- While the balanced accuracy score was quite low at only ~55%, the model was very precise at predicting low risk outcomes, but very unprecise at predicting high risk outcomes with only 1% precision. Overall, in terms of recall it was quite low with 68% for high risk outcomes and very low with only 41% for low risk outcomes

![image](https://user-images.githubusercontent.com/70483866/104132144-137ef880-5341-11eb-8144-b3a5c37a93ad.png)

* Smoteenn Sampling- While the balanced accuracy score was not that great at only ~68%, the model was very precise at predicting low risk outcomes, but very unprecise at predicting high risk outcomes with only 1% precision. Overall, in terms of recall it was quite not great with over 77% for high risk outcomes and much lower with 59% for low risk outcomes

![image](https://user-images.githubusercontent.com/70483866/104132181-3d381f80-5341-11eb-803d-f86df28a854a.png)

## Summary:

Because all 6 models had very low precision for predictng high risk loans (all under 10%), it would hard to recommend any of the models. However, if I had to pick, it would definitely be the 'Easy Ensemble AdaBoost Classifier' model due to it's high recall (over 90% for both outcomes), high balanced accuracy (over 90%), and high precision for predicting low risk outcomes at 100%. However, the one major drawback was that it's precision of predicting high risk outcomes was very low at 9%, although still higher than any of the other 5 models. A low precision and high recall or sensitivity ultimately means that there will be a large amount of false-positives (many low risk loans being marked as high risk loans).
