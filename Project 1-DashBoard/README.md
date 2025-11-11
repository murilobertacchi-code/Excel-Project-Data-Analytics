# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/b0587ffb-f76a-4db8-bab1-2360d7733642)

## Introduction

Hi everyone! 👋  
I'm Murilo, a student passionate about Data Analytics and Excel.  
This dashboard was developed as part of my learning journey to analyze real data, practice professional Excel skills, and transform insights into clear visualizations.

The **Excel Salary Dashboard** was designed to help job seekers explore salaries across different positions, countries, and job types — allowing anyone to understand how compensation varies in the data industry.

### Dashboard File
You can open the project file here:  
[📊 Project-1 DashBoard.xlsx](https://github.com/murilobertacchi-code/Excel-Project-Data-Analytics/blob/main/Project%201-DashBoard/Project-1%20DashBoard.xlsx)

### Excel Skills Used

Throughout this project, I applied the following Excel tools and techniques:

- **📉 Charts** — to visualize data and trends clearly  
- **🧮 Formulas and Functions** — to automate calculations and generate insights  
- **❎ Data Validation** — to ensure clean and consistent data inputs  

### Data Jobs Dataset

The dataset used for this dashboard contains real-world data from 2023, focused on data-related jobs.  
It includes important details such as:

- **👨‍💼 Job titles**  
- **💰 Average salaries**  
- **📍 Job locations**  
- **🛠️ Required skills**

This dataset helped me explore how job roles and locations influence salary ranges within the data analytics field.

---

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries – Bar Chart

<img width="1336" height="867" alt="1_Salary_Dashboard_Chart1" src="https://github.com/user-attachments/assets/27e22321-4c0a-46ef-9080-d901a0e69596" />

- 🛠️ **Excel Features:** Used bar charts with formatted salary values and an optimized layout.  
- 🎨 **Design Choice:** Horizontal bars were used for better visual comparison between roles.  
- 📉 **Data Organization:** Job titles were sorted by descending salary.  
- 💡 **Insights Gained:** It’s clear that senior and engineering positions offer higher median salaries than analyst-level roles.

#### 🗺️ Country Median Salaries – Map Chart

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/fab61d8a-8fba-4f6c-a3cf-020bb8b3a119)

- 🛠️ **Excel Features:** Used Excel’s map chart to display salary data across countries.  
- 🎨 **Design Choice:** Color gradients help visualize salary differences geographically.  
- 💡 **Insights Gained:** Some regions show significantly higher median salaries, emphasizing global inequality in compensation.

---

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Purpose:** Returns the median salary for a specific job title, country, and work type.  
- 📊 **Logic:** Combines `MEDIAN()` and `IF()` for multi-criteria filtering.  
- 🎯 **Result:** Delivers precise salary insights filtered by key dimensions.

🍽️ **Background Table**

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/d8b0062f-28f8-45ac-9477-9f32eb0b4f09" />

📉 **Dashboard Implementation**

<img width="1148" height="1214" alt="1_Salary_Dashboard_Job_Title" src="https://github.com/user-attachments/assets/71a116a9-7a60-4f4f-bf1b-47f6a92b262a" />

---

#### ⏰ Count of Job Schedule Type

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Purpose:** Creates a clean list of unique job schedule types.  
- 🧩 **Excel Feature:** Uses `FILTER()` to remove unwanted values and duplicates.  

🍽️ **Background Table**

<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/2272f573-d078-4dad-b57b-1649465f035b" />

📉 **Dashboard Implementation**

<img width="942" height="1212" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/c0827d96-82e8-4043-90b2-28f235b54858" />

---

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 Implemented data validation to ensure only correct options can be selected under `Job Title`, `Country`, and `Type`.  
- 🎯 Helps maintain consistent user input.  
- 👥 Improves overall usability and prevents errors in filtering.

![1_Salary_Dashboard_Data_Validation](https://github.com/user-attachments/assets/9053f05c-10a4-42da-957a-8bb8693598f6)

---

## Conclusion

This project reflects my growth as a **data analytics student**, using Excel as a professional tool to explore and present insights.  
Through this dashboard, I learned how to connect datasets, automate calculations, and transform data into meaningful visual stories.  

My goal is to continue developing projects that combine **data, finance, and analytics** — helping people make better, data-driven decisions.
