# Data Science Salary Analysis  

## Introduction  

Building on my mission to provide market transparency, this project dives deep into the high-paying skills and regional trends of the Data Science industry. By moving beyond standard spreadsheets, I utilized an ETL (Extract, Transform, Load) workflow to analyze 32,000+ records, identifying exactly which technical proficiencies lead to the highest compensation in today's market.  

## Project File  

My final project is in [Data_Science_Salary_Analysis_Project.xlsx](Data_Science_Salary_Analysis_Project.xlsx)

## Questions to Analyze  
To understand the data science job market, I asked the following:  

1. Do more skills get you better pay?
2. What’s the salary for data jobs in different regions?
3. What are the top skills of data professionals?
4. What’s the pay for the top 10 skills?

## Excel Skills Used  

 The following Excel skills were utilized for analysis:

- 📊 Pivot Tables
- 📈 Pivot Charts
- 🧮 DAX (Data Analysis Expressions)
- 🔍 Power Query
- 💪 Power Pivot

## Data Jobs Dataset
The foundation of this project is a comprehensive dataset of 33,000+ real-world job postings from 2023, curated by Luke Barousse via DataNerd.ai. This high-volume dataset allows for a statistically significant analysis of the global data market, including:

- 👨‍💼 Job titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Skills

## 1️⃣ Do more skills get you better pay?
### 🔍 Skill: Power Query (ETL)  

**📥 Extract**
- I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:
  + 🗃️ First one with all the data jobs information.
  + 🔧 The second listing the skills for each job ID.
  
**🔄 Transform**
- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.

  + 📊 data_jobs_all

<img width="244" height="312" alt="2_Project_Analysis_Screenshot1" src="https://github.com/user-attachments/assets/bb1a501a-2fa0-410a-bb02-0cc749562ab5" />      


   + 🛠️ data_job_skills  


<img width="243" height="328" alt="2_Project_Analysis_Screenshot2" src="https://github.com/user-attachments/assets/ffdcaa3a-1cef-484c-95d2-1a684b6a18fe" />    

  **🔗 Load**
- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.
  + 📊 data_jobs_all

<img width="1916" height="649" alt="2_Project_Analysis_Screenshot3" src="https://github.com/user-attachments/assets/1ab23083-5b8e-495c-9284-39eb67a3917b" />    


  + 🛠️ data_job_skills  

<img width="1914" height="702" alt="2_Project_Analysis_Screenshot4" src="https://github.com/user-attachments/assets/0e17b45d-ece9-4286-8e9d-5e6788b861fa" />  

##  📊 Analysis
**💡 Insights**
- 📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.

- 💼 Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.

<img width="874" height="537" alt="2_Project_Analysis_Chart1" src="https://github.com/user-attachments/assets/a2d6ce95-ae6c-4b97-98d4-ba17b4fc1731" />    


**🤔 So What**
- This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.

## 2️⃣ What’s the salary for data jobs in different regions?
### 🧮 Skills: PivotTables & DAX
**📈Pivot Table**
- 🔢 I created a PivotTable using the Data Model I created with Power Pivot.
- 📊 I moved the job_title_short to the rows area and salary_year_avg into the values area.
- 🧮 Then I added new measure to calculate the median salary for United States jobs
`=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States")`  
### 🧮 DAX
- To calculate the median year salary I used DAX.
`Median Salary := MEDIAN(data_jobs_all[salary_year_avg])`

### 📊 Analysis
- 💡 Insights
- 💼 Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.

- 💰 The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.

<img width="1776" height="738" alt="2_Project_Analysis_Chart2" src="https://github.com/user-attachments/assets/3102706c-6cb6-4ec6-92c5-ad5c7e7abde3" />  

**🤔 So What**
- These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering geographical variations.

## 3️⃣ What are the top skills of data professionals?
### 🔧 Skill: Power Pivot
**💪 Power Pivot**
- 🔗 I created a data model by integrating the data_jobs_all and data_jobs_skills tables into one model.
- 🧹 Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.

**🔗 Data Model**
- I created a relationship between my two tables using the job_id column.

<img width="1788" height="1264" alt="2_Project_Analysis_Screenshot5" src="https://github.com/user-attachments/assets/cf6b2884-c038-4018-8584-deff07b853f2" />    

**📃 Power Pivot Menu**
- The Power Pivot menu was used to refine my data model and makes it easy to create measures.

<img width="1918" height="742" alt="2_Project_Analysis_Screenshot6" src="https://github.com/user-attachments/assets/47acbcdb-e063-452c-8247-9059c71c92dc" />  

### 📊Analysis
**💡Insights**
- 💻 SQL and Python dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.

- ☁️ Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.

<img width="759" height="513" alt="2_Project_Analysis_Chart3" src="https://github.com/user-attachments/assets/1cf46d6c-a580-4f64-85d3-b6ab1cfce77a" />  

**🤔So What**
- Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.

## 4️⃣ What’s the pay of the top 10 skills?
### 📊 Skill: Advanced Charts (Pivot Chart)
**📈 PivotChart**
- I created a combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.
+ 🪙 Primary Axis: Median Salary (as a Clustered Column)
+ 👍 Secondary Axis: Skill Likelihood (as a Line with Markers)
- To customize the chart, I added a title axis title, removed the lines (skill likelihood), and changed the markers to diamonds.
### 📊 Analysis
**💡Insights**
- 💰 Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.

- 📉 Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicating less specialization and demand in high-salary sectors.

<img width="862" height="452" alt="2_Project_Analysis_Chart4" src="https://github.com/user-attachments/assets/94d37551-b990-4476-96fb-d3ebc9288c5a" />  

**🤔So What**
This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.  

## 🏁 Conclusion
This analysis serves as a strategic roadmap for data professionals looking to optimize their career growth. By leveraging an advanced BI stack—Power Query, Power Pivot, and DAX—I transformed a massive dataset into a clear guide on which skills offer the highest market value.
This project demonstrates my ability to manage the entire data lifecycle: from building robust ETL pipelines to delivering deep-dive insights that drive career and business strategy.













