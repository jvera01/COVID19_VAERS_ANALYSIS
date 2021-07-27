# COVID-19 VAERS ANALYSIS

<p align="center">
  <img width="950" height="400" src="Resources/Images/B5.PNG">
</p>

# Overview

## Purpose - Background & Topic Selection Reasoning

US Citizens are concerned about the risk factors of taking the COVID-19 Vaccines. We are playing the role of a team of data scientists hired by the government to analyze and assess the risk factors of receiving one of the three Emergency-Use Authorized COVID-19 vaccines. The outcome of the analysis is to help citizens make a more informed decision when taking the vaccine. We will use vaccine adverse event data provided by the government from the [Vaccine Adverse Event Reporting System.](https://vaers.hhs.gov/)

We will analyze and assess risk factors of taking the COVID19 Vaccine. We will determine the risk factors using adverse events based on age to predict life-threatening risk probability using a Machine Learning Classification Model. 

---

## Questions to Answer Based on this Data: [View Tableau - COVID-19 VAERS ANALYSIS](https://public.tableau.com/app/profile/lionshield.insurance.agency.corp./viz/COVID-19VAERSANALYSIS/COVID-19VAERSANALYSIS)

1. Total Number of Adverse Events by Vaccines
2. Total Number of Deaths by Vaccines
3. Total Number of Hospitalizations by Vaccines
4. Total Number of life-threatening Symptoms by Vaccines
5. Death vs. adverse events based on vaccine type/age/gender
6. Symptom vs. adverse events based on vaccine type/age/gender
7. Time of death after Vaccine
8. Number of deaths after vaccine
9. Hospitalization after vaccination
10. Number of life-threatening Symptoms 

---

## Data Description - VAERS Data

<p align="center">
  <img width="950" height="400" src="Resources/Images/B2.PNG">
</p>

We will be analyzing COVID19 Vaccines Adverse events. The VAERS data is accessible by downloading raw data in comma-separated value (CSV) files for import into a database, spreadsheet, or text editing program or by using the CDC WONDER online search tool. Information provided to VAERS that identifies a person who received the vaccine or vaccines will not be available to the public. De-identified VAERS data are available 4-6 weeks after the report is received. VAERS data change as new reports are received, so your results may change if you repeat the same search at a later date. 

- The data selected has three CSV files. We obtained the data from [Vaccine Adverse Event Reporting System.](https://vaers.hhs.gov/). 

  -   Data file # 1 - 2021VAERSVAX - The CSV file contains 389,323 rows and 8 columns of vaccines information.
  -   Data file # 2 - 2021VAERSSYMPTOMS - The CSV file contains 503,422 rows and 11 columns of patient symptoms information. 
  -   Data file # 3 - 2021VAERSDATA - The CSV File comtains 376,300 rows and 35 columns of patient detail information. 
- [VAERS DATA USE GUIDE.](https://vaers.hhs.gov/docs/VAERSDataUseGuide_November2020.pdf)

----
## Resources - The technologies used for this project includes:

<p align="center">
  <img width="950" height="400" src="Resources/Images/DataTech.jpeg">
</p>

- <img src="https://github.com/get-icon/geticon/raw/master/icons/postgresql.svg" alt="PostgreSQL" width="21px" height="21px"> PostgreSQL
- <img src="https://github.com/get-icon/geticon/raw/master/icons/python.svg" alt="Python" width="21px" height="21px"> Python 
- <img src="https://github.com/get-icon/geticon/raw/master/icons/pandas-icon.svg" alt="pandas" width="21px" height="21px"> Pandas library
- <img src="Resources/Images/brain.svg" alt="Machine_Learning" width="21px" height="21px"> Machine Learning Algorithm – Scikit-Learn
- <img src="Resources/Images/icons8-tableau-software.svg" alt="Tableau" width="21px" height="21px"> Tableau Public  

---

## Machine Learning Model: Random Forest Classifier

We will utilize Scikit-Learn's RandomForestClassifier, an ensemble learning model, to predict life-threatening events for people over the age of 60. Originally, we looked into predicting life-threatening events for people who either died, or were hospitalized but the data was too skewed to produce any usable results. The type of data provided ultimately led to this model and process. 

### Preliminary Data Preprocessing:
- Using LabelEncoder, we will take a list of the symptoms that were found from patients with life threatening events, and convert them each into unique numbers.
- After that, we use OneHotEncoder to encode the other categorical features as an array.
- Using StandardScaler, we use it to remove the mean and scaling to unit variance.

### Preliminary Feature Engineering and Selection:

- For our feature selection, we went with a plotly bar graph to show feature importance of the top 15 columns. We decided to use this over the SelectFromModel feature because it was visually easier to read and gave us the different levels of the least important columns.

### Training and Testing:
- Applying the Train_Test_Split method, it uses arrays or matrices into random train and test subsets to input data into a single call for splitting (and optionally subsampling) data in a one-liner. At this time, there is no need for additional training of this model.

### Model:
- We used RandomForestClassifier, an estimator that fits a number of decision tree classifiers on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting. Even though multiclass-multioutput is not supported, it was the best option because of reduced variance from combining diverse trees

### Accuracy Score:
- As of right now, the random forest predictive accuracy is 72%. With the dataset narrowed down to ids that only contained life-threatening symptoms, it is predicting the chance of these symptoms to happen to people over the age of 60.

### Conclusion:
- We were able to predict life-threatening events for people over the age of 60 by narrowing down to a DataFrame containing ID's that only had those filtered symptoms. There are further changes we can try, by doing slight adjustments to our model. We could run the prediction for each gender over 60, or even predict for each Covid-19 vaccine.




---

## Diagram DBD database structure

<p align="center">


  

 

  <img width="560" height="500" src="https://github.com/hira-ayub/COVID19_VAERS_ANALYSIS/blob/main/Resources/Images/COVID_VAERS_ERDs.png">

  

</p>

- The COVID-19 VAERS Analysis Database will be hosted locally and can run using PostgreSQL in PgAdmin (Instructions Below)

- **IMPORTANT** You will need to run your own instance in PgAdmin using the conection string provided in the SQL_DB_Connection.ipynb. Make sure to update the 'your password' section in the Config.py file with your actual password and run the code in SQL_Tables.sql.
  1. Find connection string in SQL_DB_Connection.ipynb. 
  2. Make sure to update the 'your password' section in the Config.py file with your actual password
  3. Name your SQL DataBase COVID19_VAERS_Analysis
  4. Run the code in SQL_Tables.sql.

---

## Team Members:

- Anna Stack
- Dakota Dusold
- Daniel Gandía
- Hira Ayub
- Jesus M Vera
- Justin Livingston

---

## Rules & Expectations 


- Rule # 1 Teamwork makes the dream work.
- Rule # 2 Team meetings will be scheduled, and invitations will follow.
- Rule # 3 Team Participation is required.
- Rule # 4 Team members must ask for help when stuck on an individual task.
- Rule # 5 Team members will complete the task on time for review and approval.
- Rule # 6 Team members must inform if the task will be completed late.
- Rule # 7 Team members must inform if an emergency presents itself and the team needs to complete the task.

---

## Covid-19 VAERS Analysis Project Presentation.

<p align="Left">
<h2>

[Presentation in Google Slide.](https://docs.google.com/presentation/d/e/2PACX-1vRiCvTFR6L8sFyxoEoADQ13ViT7dQJ9pPHQ5hpucSoV3fQHMJClQNkpvhKSxDZ_yozUTUaizYWZnPSR/pub?start=true&loop=false&delayms=30000)

</h2>
</p>
