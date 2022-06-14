# Fake Job Posting Classifier

### 🙋‍♂️ Goals
- Classify fake job posts using deep learning classifier
- Compare stem vs non-stem jobs' fake posts 

### 𝌞 Data Preprocessing
* Stem vs Non-Stem 
  - Stem (95.6% normal, 4.4% fraud)/ Non-stem (94.7% normal, 5.3% fraud)
                                                                             
   <img width="655" alt="Screen Shot 2022-06-13 at 10 30 59 PM" src="https://user-images.githubusercontent.com/98932859/173364929-9b46d157-44f8-430c-ac26-4bf4d0972210.png">  
* Kaggle dataset explanation   
  - Used 'fake_job_postings.csv' on Kaggle
  - Data based on 866 fake job postings
  - 16 independent variables & 1 dependent variable ('Fraudulent')
* Preprocessing (여기서부터 수정)
  - Through one-hot encoder, I transformed categorical variables ('location', 'employment type', 'required experience', 'required education')
     <img width="969" alt="Screen Shot 2022-06-14 at 10 27 53 PM" src="https://user-images.githubusercontent.com/98932859/173588765-d0a5d360-f72f-4aca-b84b-e07a50de586c.png">
  - Preprocessed Textual Data
     + ‘title’, ‘benefits’, ‘descriptions’, ‘company profile’, ‘function’, ‘industry’, ‘department’, ‘requirements’, ‘benefits’
     + Using simple imputer, null values were removed 
    
### ⌨️ Models
* Model
  - Train set: 75%, Test set: 25%
  - Logisitic Regression, Decision Tree, Random Forest Classifier, Neural Network were the selected models
    
* Model Performance  
    <img width="515" alt="Screen Shot 2022-06-14 at 10 33 59 PM" src="https://user-images.githubusercontent.com/98932859/173589965-90edb809-bac9-4fcf-8ad9-f9da33993e9e.png">  
      |Model|Accuracy|
    |------|---|
    |Decision Tree|0.986|
    |Random Forest Classifier|0.984|
    |Logistic Regression|0.981|
    |Neural Network|0.950|
* Model Performance after K-fold cross validation    
     |Model (with CV)|Accuracy|
    |------|---|
    |Decision Tree|0.986 → 0.989|
    |Random Forest Classifier|0.984 → 0.982|
    |Logistic Regression|0.981 → 0.978|
    |Neural Network|0.950 → 0.950| 
### 📍 Takeaway
* In deep learning model, Random Forest Regressor scored the lowest RMSE
* In time series model, LSTM scored the lowest RMSE

