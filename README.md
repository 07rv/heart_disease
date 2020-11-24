# Heart_Disease

Predicting heart-disease using machine learning
# We're going to take the following approach:
1. Problem definition
2. Data
3. Evaluation
4. Features
5. Modelling

# 1. Problem Definition
 In a statement,<br/>
 Given clinic parameter about a patient, can we predict whether or not they have heart disease?<br/><br/>

# 2. Data
 The original data came from the Cleavaland data from the UCI Machine Learning Repository. https://archive.ics.uci.edu/ml/datasets/heart+disease
 There is also a version of it available on kaggle. https://www.kaggle.com/ronitf/heart-disease-uci <br/><br/>

# 3. Evaluation
 If we can reach 95% accuracy at predicting whether or not a patient has heart_disease during the proof of concept, we'll pursue the project.<br/><br/>

# 4. Features
 This is where you'll get differnet information about each of the features in your data.<br/>
 Create data dictionary<br/>
 age - age in years<br/>
 sex - (1 = male; 0 = female)<br/>
 cp - chest pain type<br/>
     0: Typical angina: chest pain related decrease blood supply to the heart<br/>
     1: Atypical angina: chest pain not related to heart<br/>
     2: Non-anginal pain: typically esophageal spasms (non heart related)<br/>
     3: Asymptomatic: chest pain not showing signs of disease<br/>
 trestbps - resting blood pressure (in mm Hg on admission to the hospital) anything above 130-140 is typically cause for concern<br/>
 chol - serum cholestoral in mg/dl<br/>
     serum = LDL + HDL + .2 * triglycerides<br/>
     above 200 is cause for concern<br/>
 fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)<br/>
     '>126' mg/dL signals diabetes<br/>
 restecg - resting electrocardiographic results<br/>
    0: Nothing to note<br/>
    1: ST-T Wave abnormality<br/>
        can range from mild symptoms to severe problems<br/>
        signals non-normal heart beat<br/>
    2: Possible or definite left ventricular hypertrophy Enlarged heart's main pumping chamber<br/>
 thalach - maximum heart rate achieved<br/>
 exang - exercise induced angina (1 = yes; 0 = no)<br/>
 oldpeak - ST depression induced by exercise relative to rest looks at stress of heart during excercise unhealthy heart will stress more<br/>
 slope - the slope of the peak exercise ST segment<br/>
    0: Upsloping: better heart rate with excercise (uncommon)<br/>
    1: Flatsloping: minimal change (typical healthy heart)<br/>
    2: Downslopins: signs of unhealthy heart<br/>
 ca - number of major vessels (0-3) colored by flourosopy<br/>
     colored vessel means the doctor can see the blood passing through<br/>
     the more blood movement the better (no clots)<br/>
 thal - thalium stress result<br/>
     1,3: normal<br/>
     6: fixed defect: used to be defect but ok now<br/>
     7: reversable defect: no proper blood movement when excercising<br/>
 target - have disease or not (1=yes, 0=no) (= the predicted attribute)<br/>
 
 # 5 Modelling
   Let's briefly go through each before we see them in action.<br/>
   Hyperparameter tuning - Each model you use has a series of dials you can turn to dictate how they perform. 
   Changing these values may increase or decrease modelperformance.<br/>
   Feature importance - If there are a large amount of features we're using to make predictions, do some have 
   more importance than others? For example, for predicting heart disease, which is more important, sex or age?<br/>
   Confusion matrix - Compares the predicted values with the true values in a tabular way, if 100% correct, all 
   values in the matrix will be top left to bottom right (diagnol line).<br/>
   Cross-validation - Splits your dataset into multiple parts and train and tests your model on each part and evaluates 
   performance as an average.<br/>
   Precision - Proportion of true positives over total number of samples. Higher precision leads to less false positives.<br/>
   Recall - Proportion of true positives over total number of true positives and false negatives. Higher recall leads to 
   less false negatives.<br/>
   F1 score - Combines precision and recall into one metric. 1 is best, 0 is worst.<br/>
   Classification report - Sklearn has a built-in function called classification_report() which returns some of the main <br/>
   classification metrics such as precision, recall and f1-score.<br/>
   ROC Curve - Receiver Operating Characterisitc is a plot of true positive rate versus false positive rate.<br/>
   Area Under Curve (AUC) - The area underneath the ROC curve. A perfect model achieves a score of 1.0.<br/>
 
 
