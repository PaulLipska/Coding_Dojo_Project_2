# Coding_Dojo_Project_2
Independent project analyzing dataset for Heart Disease


2 analytical insights from your data analysis.  
You can use the 2 plots from Project 2, part 3 for this!
They should include visualizations AND written interpretations
The metrics for your best model
A description of how well your model would solve your business problem
A summary with at least 2 recommendations for your stakeholders, based on your model performance AND analytical findings.

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
From reviewing the data we can find two different correlations.  One is that Oldpeak tends to measure higher in those who are older and that it also tends to predict a higher instance of heart disease than alomst any other factor measured in this study.  

![alt text](https://github.com/PaulLipska/Coding_Dojo_Project_2/blob/main/data/oldpeak_age.png)
*  Notice the spikes in this measure as they occur roughly in the middle of each decade starting around age 38 this trend continues unabated until about 70

![alt text](https://github.com/PaulLipska/Coding_Dojo_Project_2/blob/main/data/oldpeak_level.png)
*  Here as we look at the incidence 
