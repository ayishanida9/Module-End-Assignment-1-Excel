# Module-End-Assignment-1-Excel
##Project Title: Healthcare Data Analysis and Insights
Problem Statement:
The healthcare industry generates vast amounts of data daily, providing valuable insights for
healthcare providers and policymakers to improve patient care, allocate resources effectively,
and manage healthcare costs. This project aims to analyze a comprehensive healthcare dataset
comprising medical examinations, hospitalization details, and customer profiles to extract
insights into patient health profiles, medical histories, and healthcare costs. By exploring
relationships between various health metrics, identifying trends, and visualizing key patterns, we
aim to deliver actionable insights to healthcare stakeholders for informed decision-making
through rigorous data cleaning, transformation, exploration, and analysis.

#Project Steps and Objectives:
##Data Cleaning: (5 marks)
1) Check for the number of missing values marked with '?' in each column of the “Medical
Examinations” Table and "Hospitalization Details" Table.
Ans:1. Identified and counted missing values (?) in each column of the Medical Examinations and Hospitalization Details tables.

2( Fill in the missing values of ‘month’ with Sep and ‘year’ with its average rounded to the
nearest integer.
Ans:    Replaced missing values in the Month column with Sep and missing Year values with the average year rounded to the nearest integer.

3)Determine the most frequently occurring values in the ‘smoker’
, 'Hospital tier' and 'City
tier' columns, and fill in the missing values accordingly.
Ans:    Identified the mode of the Smoker, Hospital Tier, and City Tier columns and used it to fill missing values.

4)If any 'State ID' values are missing, consider filling them with 'Unknown' or using another
appropriate strategy.
Ans:    Replaced missing State ID values with Unknown where the correct state could not be determined.

##Data Transformation: (8 marks)
1) Split the ‘names’ column in the “Customer Names” Table into 3 meaningful columns:
‘Title’, ‘First Name’, and ‘Last Name’.
Ans:Excel method:

1. Select the names column.
2. Go to Data → Text to Columns.
3. Select Delimited → Next.
4. Tick Space.
5. Click Next → Finish.
6. Rename the resulting columns:
    * Title
    * First Name
    * Last Name

Make sure the columns to the right are empty before using Text to Columns.

2)Convert the "NumberOfMajorSurgeries" column in the “Medical Examinations” Table to
numerical data by replacing non-numeric characters with meaningful numerical values.
Ans:The NumberOfMajorSurgeries column was checked for non-numeric characters. The non-numeric values were replaced with appropriate numerical values, and the column was converted to numerical data type.

3)Check for inconsistencies in the 'Heart Issues' and 'smoker' columns and propose
corrective actions if necessary.
Ans:The Heart Issues and smoker columns were checked for inconsistent entries such as different capitalization and abbreviations. The values were standardized into consistent Yes and No categories.

4) Create a new column named “Weight Status” that categorizes BMI into different
categories as below:
BMI Weight Status
Below 18.5 Underweight
18.5 – 24.9 Normal Weight
25.0 – 29.9 Overweight
30.0 and Above Obesity
Ans:=IF(B2<18.5,"Underweight",IF(B2<25,"Normal Weight",IF(B2<30,"Overweight","Obesity")))

5) Create a new column named “Diabetes Status” and fill it as per the information given
below:
HbA1C Diabetes Status
Below 5.7 Normal
5.7 – 6.4 Prediabetes
6.5 and Above Diabetes
Ans:=IF(C2<5.7,"Normal",IF(C2<6.5,"Prediabetes","Diabetes"))

6)Merge ‘year’
, ‘month’ and ‘date’ columns in the “Hospitalization Details” Table into one
column named ‘Date of Birth’ and format it in ‘DD-MMM-YYYY’ custom format.
Ans:=DATE(A2,B2,C2)
Custom to DD-MMM-YYYY

7) Calculate the ‘Age’ of each customer based on their ‘Date of Birth’ and the date of
collection of the dataset, which is 8thJune 2023.
Ans:=DATEDIF(D2,DATE(2023,6,8),"Y")
The age of each customer was calculated using the Date of Birth and the dataset collection date (8-Jun-2023).

8) Format ‘charges’ column as currency ($)
   Ans:Format charges as currency ($)

1. Select the charges column.
2. Go to Home → Number.
3. Select Currency.
4. Choose the $ (USD) symbol.

Or:

Ctrl + 1 → Currency → Symbol: $ → OK
