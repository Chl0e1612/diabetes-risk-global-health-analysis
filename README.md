# Diabetes-risk-global-health-analysis
Data analysis project exploring diabetes risk predictions and global health indicators using Excel, Python, SQL, Power BI, and Tableau

## Suggested portfolio structure
1. introduction
2. data source and context of the files
3. data preperation and cleaning
4. exploratory analaysis of predicted diabetes dataset (file 1)
5. exploratory anlysis of the global health datset (file 2)
6. linking the two datasets
7. visualisations and key findings
8. limitations and future work
9. reflection of skills what you have learned

### Explaining each step
1. explain why i should care about this topic and how it is affected by global health, get them to understand what my project is trying to uncover?
2. describe each dataset, its origin and key variables
3. how did you check quality, remove issues and prepare the data
4. describe the relationships and any patterns i saw in the predicted data set
5. summarise the global patterns in the health/economic data that are relevant for diabetes
6. explain what type of files/datasets these are and what that means for the portfolio, then mention what connections can be made
7. show the description with images or try to upload the work
8. limitations to the study, dataset, connections missing due to...
9. short reflection that makes it feel like a portfolio, not just a report


## Excel cleaning programme performed
### Dataset 1: Predicted Diabetes
1. Download and open the origional file from Kaggle in excel and save as diabetes_raw: https://www.kaggle.com/datasets/anthonytherrien/diabetes-prediction-vault
2. Open another copy of this file and rename it as diabetes_clean
3. Within the diabetes_clean file, change the range into an excel table with headers (select all the columns and Ctrl + T)
4: Fix the data by removing the issue with text to numerical (issues with certain data displaying ' before the value ('0.978654), select entire diagnosed_diabetes column, go to data then text to columns then next then finish, then go to home then number and make it 3 decimal places (this tidies up the numbers and makes them real numbers)
5: rename and add useful columns: rename diagnosed_diabetes to predicted_probability (clearer) and id to person_id. in column C add the header risk_category and enter the code:
=IF([@predicted_probability]<0.33,"Low Risk",
   IF([@predicted_probability]<0.66,"Medium Risk","High Risk"))
6: Quality check: check if there are any blanks (none), are there any values over 1 (none), can also add conditional formatting into the tables to show colour-based evidence and trends in the data, add add a PivotTable to show how many low/medium/high risk people there are (shows you validated the data and gives nice summary for the report:
insert then PivotTable then Table/Range, then put risk_category in rows and sum of id in Values
7: save diabetes_clean for evidence in google sheets and excel

### Dataset 2: Global health

1: Download and open the origional file from Kaggle in excel and save as global_health_raw: https://www.kaggle.com/datasets/miguelroca/global-health-nutrition-mortality-economic-data
2. Open another copy of this file and rename it as global_health_clean
3. Within the diabetes_clean file, change the range into an excel table with headers (select all the columns and Ctrl + T)
4: Remove irrelevant columns inside global_health_clean. What i have deleted:
government expenditure on military/ education, homocide rates, conflict and terrosism death, % injruy deaths, battle related deaths, clean fuel and technology, basic hand washing rural/ urban/ washing total, safely sanitation rural/ urban/total, basic sanitation services rural/urban/total, basic drinking wayer services, pharmacists, dentists, nurses and midwives, doctors, universal hea;th care coverage, adolescent birth rate, reproductive age women, road traffic deaths, invention against NTDs, CI value hepititis B/ TB/ malaria/ maternal mortality ratio, % birth attended by skilled personal, poisoning mortality rate, unsafe wash mortality rate, CI Value Air Pollution Death Rate Trachea Bronchus Lung Cancers Age Standarized/ cancers/ chronic ostructive pulmonary disease age/ lower respiratory infections age, suicides rate, under 5 mortality rate, infant mortality, 
This is so there is less noise, faster analysis and it shows that I have made informed choices, focusing mainly on diabetes related lifestyle factors
5: clean columm names such as % death - caridovascular disease to cardio_death_%. this allows it to be easier for readability
6: 

## Python analysis
### Dataset 1: Predicted Diabetes

