# Bike Sales Dashboard  

<img width="858" height="685" alt="bsd ss 1" src="https://github.com/user-attachments/assets/1bfadeb3-837a-423b-bd8b-cebe6d856225" />  


## Introduction  

This project was developed to provide a comprehensive view of customer purchasing patterns for a bicycle retail business. By analyzing customer demographics such as age, commute distance, and occupation, this dashboard identifies the key drivers behind bike sales.  
While inspired by the foundations of Alex the Analyst's Excel project, I significantly enhanced the UI/UX design, implementing custom color palettes and specialized chart types to improve data readability and professional aesthetics.  

## 📊 Project Files  

My final dashboard is in [Bike_Sales_Dashboard_project.xlsx](Bike_Sales_Dashboard_project.xlsx)  

## 🛠️ Excel Skills Utilized
- Data Cleaning
- Analysis
- Pivot Table
- Picot Chart
- UI/UX Design

## 📉 Dashboard Highlights  

### 1. Income Analysis per Purchase  

<img width="1315" height="433" alt="bsd chart 1" src="https://github.com/user-attachments/assets/f58b8d5f-278e-477a-8b7a-e2868ed4ed8b" />  


- Features: A clustered column chart comparing the average income of customers who bought bikes versus those who didn't.

- Design Choice: Used high-contrast colors to quickly distinguish between "Yes" and "No" purchase categories.

- Key Insight: Higher-income individuals show a slightly higher propensity for bike purchases, though the gap is narrower in specific occupations.

### 2. Customer Commute Trends  

<img width="1308" height="450" alt="bsd chart 2" src="https://github.com/user-attachments/assets/cb827170-8319-45a5-968c-78170c6451b8" />  


- Features: A line chart visualizing the relationship between commute distance and purchase volume.

- Design Choice: Simplified the X-axis categories to show clear trends from "0-1 Miles" to "10+ Miles."

- Key Insight: Customers with shorter commutes (0-1 miles) are the primary buyers, suggesting bikes are used more for local transit than long-distance commuting.

### 3. Age Group Segmentation  

<img width="1323" height="457" alt="bsd chart 3" src="https://github.com/user-attachments/assets/12098857-6262-4342-a3a6-a7a175715c6a" />  


- Features: Binned customer ages into "Adolescent," "Middle Age," and "Senior" categories using nested logic.

- Design Choice: A clean line chart to show peak purchasing years.

- Key Insight: The "Middle Age" bracket is the most profitable segment for this business.

## 🧮 Logic & Data Transformation
- 🧹 The "Age Brackets" Logic
To make the data more useful for marketing, I transformed raw age numbers into categorized groups using this logic:

`=IF(L2>54,"Senior",IF(L2>=31,"Middle Age",IF(L2<31,"Adolescent","Invalid")))`  

- Purpose: This allowed for a higher-level view of the customer base, moving away from "noisy" individual ages to actionable demographic segments.

## 🔗 Dashboard Interactivity
- Slicers: Integrated Slicers for Region, Education, and Occupation.

- Pivot Connections: All charts are linked to these slicers, allowing users to filter the entire dataset with a single click for deep-dive regional analysis.

## 🏁 Conclusion
The Bike Sales Dashboard showcases my ability to take a raw dataset and convert it into a polished, interactive business tool. By focusing on both data accuracy and visual design, I created a dashboard that not only reports numbers but tells a clear story about who the customer is and why they buy.

This project serves as the foundation of my data journey, demonstrating my core proficiency in Excel data cleaning and my eye for professional dashboard aesthetics.

