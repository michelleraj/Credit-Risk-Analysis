# Credit Risk Prediction Model Report
Objective: Improve high-risk loan detection using imbalanced machine learning techniques.
## Resampling Techniques

1. Naive Random Oversampling: Duplicates minority class instances

2. SMOTE Oversampling: Generates synthetic minority samples using k-nearest neighbors

3. Cluster Centroids Undersampling: Reduces majority class through cluster centroids

4. SMOTEENN Combination: Hybrid approach using SMOTE oversampling and Edited Nearest Neighbor undersampling

Ensemble Models

5. Balanced Random Forest: Bootstrap sampling with undersampled majority class
   
6. Easy Ensemble AdaBoost: Sequential learning with boosted decision trees

## 🚀 Key Results
| Method                      | Accuracy | Precision | Recall |  
|-----------------------------|----------|-----------|--------|  
| Naive Random Oversampling   | 65.47%   | 99%       | 59%    |  
| SMOTE Oversampling          | 66.00%   | 99%       | 69%    |  
| Cluster Centroids           | 66.00%   | 99%       | 40%    |  
| SMOTEENN                    | 54.00%   | 99%       | 57%    |  
| Balanced Random Forest      | 76.00%   | 99%       | 87%    |  
| **Easy Ensemble AdaBoost**  | **93%**  | **99%**   | **94%**|  

Need to employ different techniques to train and evaluate models with unbalanced classes. oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.


**Table Descriptions**  
| Table Name     | Description                          | Sample Fields                          |
|----------------|--------------------------------------|-----------------------------------------|
| `Loans`        | Original loan data                   | `loan_amnt`, `int_rate`, `loan_status` |
| `ModelResults` | Predictions and actual outcomes      | `predicted_risk`, `actual_risk`, `prob_high_risk` |
| `Performance`  | Metrics by resampling technique      | `technique`, `recall`, `precision`, `balanced_accuracy` |
| `CostSavings`  | Financial impact calculations        | `high_risk_caught`, `avg_loan_amt`, `default_rate` |

### Data Flow Diagram
graph TD
    A[Raw Loans] --> B{Preprocessing}
    B --> C[Resampled Data]
    C --> D[Model Training]
    D --> E[Risk Predictions]


### Naive Random Oversampling 
Our balanced accuracy test is 0.6547. Average Precision of 99% and recall of 59%. 

<img width="730" alt="Screen Shot 2021-11-09 at 11 32 28 PM" src="https://user-images.githubusercontent.com/57809798/141050222-a49451d3-4c6d-4570-ba10-cbcbf9fd3669.png">

### SMOTE oversampling
Accuracy of 66% average precision of 99% and recall of 69%
<img width="737" alt="Screen Shot 2021-11-09 at 11 33 00 PM" src="https://user-images.githubusercontent.com/57809798/141050263-7f4d7ead-2ce3-46af-b99e-8dfdc902155b.png">

### Undersampling
Accuracy of 66% and average precision of 99% and recall of 40%, recall dropped by around 29%
<img width="719" alt="Screen Shot 2021-11-09 at 11 33 20 PM" src="https://user-images.githubusercontent.com/57809798/141050302-6e342d8b-7e85-4cc7-88da-0018546486bb.png">

### Over and undersampling
Accuracy of 54% average precision of 99% and recall of 57%
<img width="736" alt="Screen Shot 2021-11-09 at 11 33 42 PM" src="https://user-images.githubusercontent.com/57809798/141050335-52bc9beb-b3fb-4a53-bf16-1ede1412d759.png">

### Balanced Random Forest Classifier
With accuracy of 76% and average precision of 99% and recall of 87%, recall increased by around 20%

<img width="734" alt="Screen Shot 2021-11-09 at 11 31 55 PM" src="https://user-images.githubusercontent.com/57809798/141050177-c3534786-1488-4efa-b6bd-a20610497adc.png">

### Easy Ensemble AdaBoost Classifier
Accuracy of 93% average precision of 99% and recall of 94%, recall is the highest for this ensemble algorithm


<img width="738" alt="Screen Shot 2021-11-09 at 11 31 40 PM" src="https://user-images.githubusercontent.com/57809798/141050149-1b9a4763-4ab2-447b-b28c-30da4336943a.png">

## Summary
For the credit risk analysis, we compared different supervised machine learning algorithms which were undersampling, oversampling, a combination of undersampling, and oversampling, while the precision remained higher for all the above algorithms the recall was not high enough. We finally did ensemble classifiers, Random forest where we achieved all high precision, accuracy, and recall and the highest recall was received for the ensemble AdaBoost classifier



MIT License

Copyright (c) [2025] [Michelle Raj]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.



