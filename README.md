
# PROJECT NAME: CognitiveQuest (Autism Prediction)

## Project Overview
This project aims to develop a classification model to predict Autism Spectrum Disorder (ASD) using machine learning techniques. The model will be trained on the Autistic Spectrum Disorder Screening Data for child and adult dataset, which contains influential features for detecting ASD traits in adults and children. By analyzing the dataset's behavioural features and individual characteristics, this project aims to build a robust screening method that can assist healthcare professionals in early autism diagnosis.

# **The Dataset**
**Short Description of the Data:**

The dataset contains information pertinent to the screening of autism spectrum disorder (ASD), comprising the following columns:

1. ID: Unique identifier for each patient
2. A1_Score to A10_Score: Scores derived from the Autism Spectrum Quotient (AQ) 10 item screening tool
3. age: Age of the patient in years
4. gender: Gender of the patient
5. ethnicity: Ethnicity of the patient
6. jaundice: Indicator of whether the patient experienced jaundice at birth
7. autism: Indication of whether an immediate family member has been diagnosed with autism
8. country_of_res: Country where the patient resides
9. used_app_before: Flag indicating if the patient has previously undergone a screening test
10. result: Aggregate score for AQ1-10 screening test
11. age_desc: Description of the patient's age
12. relation: Relationship of the individual who completed the test with the patient
13. Class/ASD: Binary classification of ASD presence, where 0 signifies No ASD and 1 indicates ASD presence (target column)

The dataset is divided into a training set (train.csv) and a test set (test.csv).

The primary objective is to forecast the probability of an individual having ASD based on the provided features, with the "Class/ASD" column serving as the target variable for prediction.

**Data Sources and Aggregation:**
    
***Data Sources***:

- **UC Irvine Machine Learning Repository (Autistic Spectrum Disorder Screening Data for Children)**:

This dataset contains information about individuals, including their scores on various screening questions for Autism Spectrum Disorder (ASD), demographic details such as age, gender, and ethnicity, as well as other factors like whether they have previously used ASD screening apps or if they have a family history of autism. Each individual is classified as either having ASD or not based on the screening results. [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/419/autistic+spectrum+disorder+screening+data+for+children)


- **UC Irvine Machine Learning Repository (Autistic Spectrum Disorder Screening Data for Adults)**:

This dataset contains information about adults and their scores on various screening questions for Autism Spectrum Disorder (ASD), along with demographic details such as age, gender, and ethnicity. It aims to facilitate the analysis of influential autistic traits and improve the classification of ASD cases. There are 704 instances and 21 attributes in the dataset, which includes missing values, and it is suitable for classification tasks in the medical, health, and social science domains. [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/426/autism+screening+adult)

***Necessity for Data Aggregation***

In reference to the provided data sources:

Data aggregation from multiple sources is necessary for comprehensive analysis as it allows for a broader coverage across different age groups (children and adults), enhances the sample size for statistical significance, validates findings through cross-verification, and addresses potential data gaps or biases present in individual datasets.

## Model Training

### Model 1: Randomforest
-**Training Results with hyperparameter tuning**:
Accuracy: 0.9467
Precision: 0.9375
Recall: 0.9000
F1 Score: 0.9184
Log Loss: 0.1792
AUC Score: 0.9928
Kappa Score: 0.8788
Error Rate: 0.0533

-**Training Results without hyperparameter tuning**:
Accuracy: 0.9400
Precision: 0.9184
Recall: 0.9000
F1 Score: 0.9091
Log Loss: 0.1710
AUC Score: 0.9922
Kappa Score: 0.8643
Error Rate: 0.0600


### Model 2: Adabooster Classifier
-**Training Results with hyperparameter tuning**:
Accuracy: 1.0000
Precision: 1.0000
Recall: 1.0000
F1 Score: 1.0000
Log Loss: 0.5607
AUC Score: 1.0000
Kappa Score: 1.0000
Error Rate: 0.0000

-**Training Results without hyperparameter tuning**:
Accuracy: 1.0000
Precision: 1.0000
Recall: 1.0000
F1 Score: 1.0000
Log Loss: 0.5481
AUC Score: 1.0000
Kappa Score: 1.0000
Error Rate: 0.0000


### Model 3: XCBoost Classifier
-**Training Results with hyperparameter tuning**:
-**Accuracy**: 0.9200
-**Precision**: 0.9750
-**Recall**: 0.7800
-**F1 Score**: 0.8667
-**Log Loss**: 0.3486
-**AUC Score**: 0.9836
-**Kappa Score**: 0.8105
-**Error Rate**: 0.0800

-**Training Results without hyperparameter tuning**:
Accuracy: 0.9600
Precision: 0.9231
Recall: 0.9600
F1 Score: 0.9412
Log Loss: 0.0636
AUC Score: 0.9978
Kappa Score: 0.9109
Error Rate: 0.0400


## Findings
Random Forest emerged as the most balanced choice among the three models, delivering consistently high performance with or without hyperparameter tuning. While AdaBoost Classifier showcased flawless accuracy, its computational demands may outweigh its benefits in specific contexts. XGBoost Classifier, although competitive, especially after tuning, requires additional optimization efforts compared to Random Forest, making it slightly less straightforward to implement.
---

### Setting up ML Deployment on Streamlit:

1. **Install Streamlit**:
   ```bash
   pip install streamlit
   ```

2. **Open Streamlit App Folder**
  
3. **Test Locally**:
   Run app.py locally
   ```bash
   streamlit run app.py
   ```

### Deploying App on Streamlit Server:

1. **Sign up for Streamlit**:
   - Go to https://share.streamlit.io/ and sign up for a Streamlit. Connect it with GitHub repo.

2. ***Deploy App**:
   - Click "New App" and fill in the required fields to configure app.
   - Connect Streamlit repo and click  "Deploy" to deploy the web app on Streamlit server.
   - Monitor the deployment and check for errors in the logs by clicking "Manage App".

3. **Access Deployed App**:
   Once deployed, web app will be accessible via a web page in the browser.

4. **Link to App**: https://cognitivequest123.streamlit.app/

