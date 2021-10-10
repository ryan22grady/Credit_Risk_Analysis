# Credit_Risk_Analysis

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

### 1. Naive
<img width="804" alt="Screen Shot 2021-10-10 at 5 49 10 PM" src="https://user-images.githubusercontent.com/84995704/136714109-7c30b1fe-b1af-4abe-a8a7-2a58e35504e1.png">

### 2. SMOTE
<img width="810" alt="SMOTE" src="https://user-images.githubusercontent.com/84995704/136714111-e9d5eb66-f799-4b9e-932f-f4fa1d3b0f0d.png">

### 3. Clustercentroids
<img width="792" alt="Clustercentroids" src="https://user-images.githubusercontent.com/84995704/136714114-d99987cb-5df4-466e-a4bb-a18c0cfe44f7.png">

### 4. SMOTEENN
<img width="799" alt="SMOTEENN" src="https://user-images.githubusercontent.com/84995704/136714117-445cad70-b81d-4705-9e67-b8d7951e6cb0.png">

### 5. EasyEnsemble
<img width="634" alt="easyesemble" src="https://user-images.githubusercontent.com/84995704/136714122-be53f883-ea3a-4333-a69d-55e0effea220.png">

### 6. BalancedRandom
<img width="801" alt="Balanced" src="https://user-images.githubusercontent.com/84995704/136714124-c39fa813-87b3-4f8c-869a-c341d6f6ecfc.png">

## Summary
As shown by the summary dataframes and individual model testing, both Ensemble Classifiers outperformed the Resampling techniques in accurately predicted high-risk credit card applicants and low-risk applicants, given the features used to classify each group of potential loanees. In the case of screening for high-risk individuals, high sensitivty outweighs precision performance of the model--it is better to minimize false negatives and let those high-risk indivudals slip through the test undetected, in the instance of protecting the interests of the loaning companies.

Machine learning produced a 9% reliability that those that were identified as high-risk were actually high risk. With a 91% chance of a False Positive result, where a low-risk applicant is lableed as high-risk, it is difficult to recommend any of the models tested in this project for implementation--regardless of high sensitivity, financial institutions risk losing 91% of future customers and revenues of low-risk applicants when they are rejected for a credit-card. Many potential customers would take their business elsewhere and be unwilling to take on the headache of disputing the decision with the credit card company.
