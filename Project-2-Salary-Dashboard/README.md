# Data Science Salary Calculator Dashboard  

<img width="800" height="333" alt="1_Salary_Dashboard_Final_Dashboard" src="https://github.com/user-attachments/assets/b80c080f-f909-4f03-a213-e78f7fa4faec" />  

## Introduction  

I developed this interactive Salary Calculator to promote market transparency within the Data Science field. By analyzing a dataset of 32,000+ real-world job postings, this tool empowers individuals to accurately comprehend their market value. It allows users to filter by role, location, and schedule type to ensure they are being compensated fairly based on current industry standards.  

## Dashboard File  

My final dashboard is in [Data_Science_Salary_Calculator_Dashboard_Project.xlsx](Data_Science_Salary_Calculator_Dashboard_Project.xlsx)   

## Excel Skills Used  

The following Excel skills were utilized for analysis:

- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation

## Data Jobs Dataset  

The foundation of this project is a comprehensive dataset of 33,000+ real-world job postings from 2023, curated by Luke Barousse via DataNerd.ai. This high-volume dataset allows for a statistically significant analysis of the global data market, including:  
- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

## Dashboard Build  

## 📉 Charts  

### 📊 Data Science Job Salaries - Bar Chart  

<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/ca5234ae-e160-4962-a865-0884e21cbd4f" />  

- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

### 🗺️ Country Median Salaries - Map Chart  

<img width="800" height="430" alt="1_Salary_Dashboard_Country_Map" src="https://github.com/user-attachments/assets/c74a2d86-2816-4afd-834c-7f02f1141c0b" />  

- 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
- 📊 Data Representation: Plotted median salary for each country with available data.
- 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
- 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.

## 🧮 Formulas and Functions  

### 💰 Median Salary by Job Titles  

`=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)`  


- 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
- 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
- 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
- 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table  
<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/730b3b17-b08c-4add-a8ef-d4935d3463b6" />  

📉 Dashboard Implementation  
<img width="1148" height="1214" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/b082552f-c546-45a4-9db3-288c3251d490" />  

### ⏰ Count of Job Schedule Type  

`=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))`  
- 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
- 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table  
<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/07b4cef6-61a9-4b36-9515-663e19f178a1" />  

📉 Dashboard Implementation  
<img width="942" height="1212" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/e9cfafc3-04df-4024-b69b-2fd5f73c1aee" />  

## ❎ Data Validation  

- 🔍 Filtered List
- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
- 🎯 User input is restricted to predefined, validated schedule types
- 🚫 Incorrect or inconsistent entries are prevented
- 👥 Overall usability of the dashboard is enhanced

<img width="624" height="602" alt="1_Salary_Dashboard_Data_Validation" src="https://github.com/user-attachments/assets/ca623b9b-2ee7-4c98-920f-25cb74cf1a4a" />  

## Conclusion  

This dashboard transforms 32,000+ records into a functional tool for market transparency, allowing professionals to accurately determine their market value. By bridging the gap between raw data and career strategy, it empowers users to make data-driven decisions regarding their compensation and professional future.








