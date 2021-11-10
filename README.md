# Credit-Risk-Analysis
Need to employ different techniques to train and evaluate models with unbalanced classes. oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.


### Naive Random Oversampling 
Our balanced accuracy test it 0.6547. Average Precision of 99% and recall of 59%. 

<img width="730" alt="Screen Shot 2021-11-09 at 11 32 28 PM" src="https://user-images.githubusercontent.com/57809798/141050222-a49451d3-4c6d-4570-ba10-cbcbf9fd3669.png">

### SMOTE oversampling
Accuracy of 66% and average precision of 99% and recall of 69%
<img width="737" alt="Screen Shot 2021-11-09 at 11 33 00 PM" src="https://user-images.githubusercontent.com/57809798/141050263-7f4d7ead-2ce3-46af-b99e-8dfdc902155b.png">

### Undersampling
Accuracy of 66% and average precision of 99% and recall of 40%, recall dropped by around 29%
<img width="719" alt="Screen Shot 2021-11-09 at 11 33 20 PM" src="https://user-images.githubusercontent.com/57809798/141050302-6e342d8b-7e85-4cc7-88da-0018546486bb.png">

### Over and undersampling
Accuracy of 54% and average precision of 99% and recall of 57%
<img width="736" alt="Screen Shot 2021-11-09 at 11 33 42 PM" src="https://user-images.githubusercontent.com/57809798/141050335-52bc9beb-b3fb-4a53-bf16-1ede1412d759.png">

### Balanced Random Forest Classifier
Accuracy of 76% and average precision of 99% and recall of 87%, recall increased by around 20%

<img width="734" alt="Screen Shot 2021-11-09 at 11 31 55 PM" src="https://user-images.githubusercontent.com/57809798/141050177-c3534786-1488-4efa-b6bd-a20610497adc.png">

### Easy Ensemble AdaBoost Classifier
Accuracy of 93% and average precision of 99% and recall of 94%, recall is the highest for this ensemable algorithm


<img width="738" alt="Screen Shot 2021-11-09 at 11 31 40 PM" src="https://user-images.githubusercontent.com/57809798/141050149-1b9a4763-4ab2-447b-b28c-30da4336943a.png">

## Summary
For the credit risk analysis, we compared different supervised machine learning algorithms which were undersampling, oversampling, a combination of undersampling, and oversampling, while the precision remained higher for all the above algorithms the recall was not high enough. We finally did ensemble classifiers, Random forest where we achieved all high precision, accuracy, and recall and the highest recall was received for the ensemble AdaBoost classifier



