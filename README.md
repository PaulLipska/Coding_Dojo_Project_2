# Coding_Dojo_Project_2
Independent project analyzing dataset for Heart Disease

### Business Problem
How to successfully predict the onset of heart disease

##### Source:
https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

##### Audience
The audience for this study would be both medical practitioners and their patients and how their personal stats match this data

##### Data Dictionary

*  Age: age of the patient [years]
*  Sex: sex of the patient [M: Male, F: Female]
*  ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
*  RestingBP: resting blood pressure [mm Hg]
*  Cholesterol: serum cholesterol [mm/dl]
*  FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
*  RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
*  MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
*  ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
*  Oldpeak: oldpeak = ST [Numeric value measured in depression]
*  ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]
*  HeartDisease: output class [1: heart disease, 0: Normal]

##### Insights
From reviewing the data we can find two different correlations.  Old peak in the range of 0-2 is a strong indication of Heart Disease and Heart Disease tends to occur with greater frequency for 50 year olds and drops off dramatically either due to people dieing or due to excessive number of 50 year olds in this investigation

![alt text](https://github.com/PaulLipska/Coding_Dojo_Project_2/blob/main/data/oldpeak_age.png)
*  Per our observation you can see those in their 50s have the highest incidence of Heart Disease

![alt text](https://github.com/PaulLipska/Coding_Dojo_Project_2/blob/main/data/oldpeak_level.png)
*  Looking at strictly Heart Disease as it occurs in relation to old peak we can identify several markers where Heart Disease and this measurement are set to coincide. 0.0, 1.0, 1.5, and 2.0. 

##### Finding the Correct Model
Researching this issue I used Random Forest and XGBoost.  Both models were optimized with GridsearchCV and PCA.  The resulting best fit model used XGBoost with PCA.  The results returned were:

Accuracy score on XGBoost with PCA train set:  0.9200581395348837
Accuracy score on XGBoost with PCA test set:  0.8913043478260869

These scores were identical to the score for XGBoost with GridsearchCV, but were arrived at with fewer steps making for a more effecient model.  

![alt text](https://github.com/PaulLipska/Coding_Dojo_Project_2/blob/main/data/conf_.png)

### Summary
Based on this investigation there is promise in focusing on key metrics like oldpeak and its corelation to Heart Disase and Age.  This model had a heavy target audince of those in their early 50s.  It might be useful to break off the study into age groups to more effectively catalog data from those groups.  Perhaps just focus on 50 year olds.
