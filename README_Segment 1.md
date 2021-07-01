# COVID19_VAERS_ANALYSIS

![](Resources/B5.PNG)

# Overview of the COVID19 VAERS_ANALYSIS

## Purpose - Background & Reason for topic selection

US Citizens are concerned about the risk factors of taking the COVID19 Vaccines. We are playing the role of a team of data scientists hired by the government to analyze and assess the risk factors of taking a covid vaccine. The outcome of the analysis is to help citizens make a more informed decision when taking the vaccine. We will use vaccine adverse event data provided by the government from the [Vaccine Adverse Event Reporting System.](https://vaers.hhs.gov/)

We will analyze and assess risk factors of taking the COVID19 Vaccine. We will determine the risk factors using adverse events based on age and gender to predict life-threatening risk probability using a Machine Learning Classification Model. 

## The Analisys will answer the following questions:

1. Total Number of Adverse Events by Vaccines
2. Total Number of Deaths by Vaccines
3. Total Number of Hospitalizations by Vaccines
4. Total Number of life-threatening Symptoms by Vaccines
5. Death vs. adverse events based on vaccine type/age/gender
6. Symptom vs. adverse events based on vaccine type/age/gender
7. Time of death after Vaccine
8. Number of deaths after vaccine
9. Hospitalization because of vaccination(?)
10. Number of life-threatening Symptoms 


## Data Description - VAERS Data
![](Resources/B2.PNG)

We will be analyzing COVID19 Vaccines Adverse events. The VAERS data is accessible by downloading raw data in comma-separated value (CSV) files for import into a database, spreadsheet, or text editing program or by using the CDC WONDER online search tool. Information provided to VAERS that identifies a person who received the vaccine or vaccines will not be available to the public. De-identified VAERS data are available 4-6 weeks after the report is received. VAERS data change as new reports are received, so your results may change if you repeat the same search at a later date. 

- The data selected has three CSV files. We obtained the data from [Vaccine Adverse Event Reporting System.](https://vaers.hhs.gov/). 
  -   Data file # 1 - 2021VAERSVAX - The CSV file contains 389323 rows and 8 columns of vacinnes infomation.
  -   Data file # 2 - 2021VAERSSYMPTOMS - The CSV file contains 503422 rows and 11 columns of patient symptoms information. 
  -   Data file # 3 - 2021VAERSDATA - The CSV File comtains 376300 rows and 35 columms of patient detail information. 



## Resources - The technologies used for this project includes:
![](Resources/DataTech.jpeg)

- Python & Pandas library
- Pg Admin PostgresSQL
- Machine Learning Algorithm – Scikit-Learn
- Tableau Public

## Machine Learning Classification:
- Predict Risk Factors the chances of a patient to get (X) symptoms for (Y) Vaccine
- Take a limited list of the most common symptoms, and convert them into numbers
- Catagorize them based off of which vaccine
- Find the most dense amount of cases based on age
- Predict for male/female/other

## Diagram DBD database structure

![](https://github.com/hira-ayub/COVID19_VAERS_ANALYSIS/blob/main/Resources/COVID_VAERS_%20ERDs.png)

## Team Members - Rules and Expectations:

- Anna Stack
- Dakota Dusold
- Daniel Gandia
- Hira Ayub
- Jesus M Vera
- Justin Livingston

## Rules & Expectations - Description of the communication protocols 


- Rule # 1 Teamwork makes the dream works
- Rule # 2 Team meetings will be scheduled, and invitations will follow.
- Rule # 3 Team Participation is required 
- Rule # 4 Team members must ask for help when stuck on an individual task.
- Rule # 5 Team members will complete the task on time for review and approval
- Rule # 6 Team members must inform if the task will be completed late.
- Rule # 7 Team members must inform if an emergency presents itself and the team needs to complete the task.

