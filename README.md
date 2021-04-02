# Identifying Populations at Risk for CHD
by: Zachary Greenberg & Jonathan Silverman

<p align="center"><img src="https://github.com/zachagreenberg/Cardiovascular_Disease/blob/main/Images/Readme_Cover.jpg" width="400" height="250" /></p>

## Overview

Coronary Heart Disease, also grimly known as the 'silent killer', is the number one leading cause of death among Americans. This project explores the potential risk factors for CHD. With this knowledge, hoepfully preventative actions can be taken. The findings come from patient data in a longterm cardiovascular health study. 

## Business Problem

CHD is a costly disease. It not only costs the US billions of dollars annually, it costs many families their loved ones. We are seeking to identify the top risk factors for CHD to promote awareness and aid in the recognition of specific populations at risk. This will encourage intervention efforts so that we may improve overall patient health and lower healthcare costs down the line. 

## Data

The data comes from a longterm cardiovascular health study in Framingham, Massachusetts. Patients have provided some medical information in the form of variables that are believed to contribute to the onset of CHD. This data is publicly available on Kaggle. The following variables are included:

• Sex: male or female("M" or "F")    
• Age: Age of the patient    
• is_smoking: whether or not the patient is a current smoker    
• Cigs Per Day: the number of cigarettes that the person smoked on average in one day    
• BP Meds: whether or not the patient was on blood pressure medication    
• Prevalent Stroke: whether or not the patient had previously had a stroke   
• Prevalent Hyp: whether or not the patient was hypertensive   
• Diabetes: whether or not the patient had diabetes   
• Tot Chol: total cholesterol level   
• Sys BP: systolic blood pressure   
• Dia BP: diastolic blood pressure   
• BMI: Body Mass Index  
• Heart Rate: heart rate  
• Glucose: glucose level  

TARGET
• 10 year risk of coronary heart disease CHD

## Exploratory Data Analysis

We began our process by evaluating specific variables and their relations with the target. One of the most powerful discoveries was the exponential relationship between age and risk of CHD.

<p align="center"><img src="https://github.com/zachagreenberg/Cardiovascular_Disease/blob/main/Images/CHDbyAge.png" width="800" height="300" /></p>

After our study of individual variables we looked at the possibility of polynomial combinations together.

<p align="center"><img src="https://github.com/zachagreenberg/Cardiovascular_Disease/blob/main/Images/Data__Relations.png" width="600" height="200" /></p>

By doing so we were able to identify a large percentage of the population at risk for CHD. This inspired us to engineer new features.

## Methods

We attempted various Classification techniques to create an inferential model, narrowing it down between three models:

<p align="center"><img src="https://github.com/zachagreenberg/Cardiovascular_Disease/blob/main/Images/Models.png" width="500" height="200" /></p>



The best model for our case was a Decision Tree for its high recall score and ease of interpretability. We used built in methods from the scikit package including feature_importance to get an idea of the most serious risk factors.  We also used plot_tree to get a visualization of the tree which made drawing inferences easy.  

## Results
The algorithm identified the most important factors being Systolic BP, BMI, Cholesterol, Age, Heart rate, and Glucose Levels. These findings speak volumes as 5 out the 6 are ones in our control. 

<p align="center"><img src="https://github.com/zachagreenberg/Cardiovascular_Disease/blob/main/Images/DecTree17Magnitude.png" width="500" height="300" /></p>

Additionally with the visualization of the first few branches, we were not only able to see those factors, we were able to identify the algorithm's cut-off values for sorting the data.

<p align="center"><img src="https://github.com/zachagreenberg/Cardiovascular_Disease/blob/main/Images/dtree17.png" width="600" height="400" /></p>



## Conclusion

Our findings lead us to the following thoughts:

- Interventions for CHD prevention should be recommended for individuals who are over the age of 46, have a systolic blood pressure greater that 147mmHg, are male, and have a glucose level greater than 92.5mg/dl. 

- It is important to focus on the factors we can control. For example, in the above mentioned population,  monitoring glucose could be a first step taken as lowering glucose will help lower blood pressure and decrease the risk of CHD.

## Next Steps

- Further research on the habits of the healthier individuals in the study for comparison.

- Find more detailed medical information for more comprehensive evaluation.


### Repository Structure
|_ Data  
|_ Images    
|_ CHDPowerpointPresentation.pdf   
|_ Project_Notebook.ipynb   
|_ README.md



