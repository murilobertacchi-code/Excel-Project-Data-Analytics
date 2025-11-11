# 📊 Project 2 – Data Jobs Analysis

## 👋 Introduction

Hey everyone! I’m Murilo — a student passionate about data analytics and Excel.  
This project is part of my learning journey to explore **how data can tell real stories** about the job market.

I decided to dive into real data to answer a simple question:  
💭 *“What actually makes a data job pay more — and what skills are behind it?”*

---

### 🎯 Questions I Wanted to Answer

To understand the data science job market, I focused on four main questions:

1. **💡 Do more skills get you better pay?**  
2. **🌍 What’s the salary for data jobs in different regions?**  
3. **🧠 What are the top skills of data professionals?**  
4. **💰 What’s the pay for the top 10 skills?**

---

### 🧮 Excel Skills Used

During this project, I practiced some of Excel’s most powerful data tools:

- **📊 Pivot Tables**  
- **📈 Pivot Charts**  
- **🧮 DAX (Data Analysis Expressions)**  
- **🔍 Power Query**  
- **💪 Power Pivot**

---

### 🗂️ Dataset Overview

The dataset used for this analysis contains **real-world data from 2023** focused on data-related jobs.  
It includes information such as:

- **👨‍💼 Job titles**  
- **💰 Salaries**  
- **📍 Locations**  
- **🛠️ Skills**

This helped me understand what top employers are really looking for and how specific skills impact salary.

---

## 1️⃣ Do more skills get you better pay?

### 🔍 Skill Used: Power Query (ETL)

#### 📥 Extract

- I started by using **Power Query** to extract the original data (`data_salary_all.xlsx`) and created two queries:
  - 🗃️ One with all job data  
  - 🔧 Another listing the skills for each job ID

#### 🔄 Transform

- I cleaned and organized the data by changing column types, removing unnecessary columns, and trimming text — keeping everything consistent and analysis-ready.  

  - 📊 data_jobs_all  

    <img width="244" height="312" alt="2_Project_Analysis_Screenshot1" src="https://github.com/user-attachments/assets/70a7ebe3-cb28-4608-8818-d7d3a6f62abe" />

  - 🛠️ data_job_skills  

    <img width="243" height="328" alt="2_Project_Analysis_Screenshot2" src="https://github.com/user-attachments/assets/1596f89e-43c9-4e5b-8660-421e06d23aa0" />

#### 🔗 Load

- Finally, I loaded both queries back into Excel to build the foundation for all my analysis.  

  - 📊 data_jobs_all  

    <img width="1916" height="649" alt="2_Project_Analysis_Screenshot3" src="https://github.com/user-attachments/assets/b5a9bc62-4ff7-483a-a1ee-565840158d72" />

  - 🛠️ data_job_skills  

    <img width="1914" height="702" alt="2_Project_Analysis_Screenshot4" src="https://github.com/user-attachments/assets/8a7ef6b3-920b-4f84-8a86-5f9dbc72398b" />

---

### 📊 Analysis & Insights

- 📈 The more skills a job required, the higher the salary tended to be — especially for roles like **Senior Data Engineer** and **Data Scientist**.  
- 💼 Roles that demanded fewer skills, such as **Business Analyst**, generally offered lower salaries.  

  <img width="874" height="537" alt="2_Project_Analysis_Chart1" src="https://github.com/user-attachments/assets/416d1b77-3822-402b-aa42-1331fe08f919" />

🧠 **So What:**  
This clearly shows the importance of continuously learning — more relevant skills can literally translate into higher pay.

---

## 2️⃣ What’s the salary for data jobs in different regions?

### 🧮 Skills Used: PivotTables & DAX

#### 📈 Pivot Table

- I created a PivotTable from my **Power Pivot Data Model** to calculate median salaries by job title.  
- Then I added a new DAX measure to calculate the **median salary specifically for the United States**:

```excel
=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States")
```

#### 🧮 DAX Measure

To calculate the general median salary:

```excel
Median Salary := MEDIAN(data_jobs_all[salary_year_avg])
```

---

### 📊 Analysis & Insights

- 💼 High-level roles like **Data Scientist** and **Senior Data Engineer** had strong median salaries both in the U.S. and internationally.  
- 💰 The difference between **U.S. and Non-U.S. salaries** was striking — showing the U.S. tech market’s strong pull.

  <img width="1776" height="738" alt="2_Project_Analysis_Chart2" src="https://github.com/user-attachments/assets/df4297e5-2532-4ef0-b374-f3297ed835d6" />

🧠 **So What:**  
These insights can help professionals negotiate fair salaries and understand how location affects compensation in the tech world.

---

## 3️⃣ What are the top skills of data professionals?

### 🔧 Skill Used: Power Pivot

#### 💪 Power Pivot

- I created a **Data Model** by linking my two tables: `data_jobs_all` and `data_jobs_skills`.  
- Thanks to the earlier data cleaning in Power Query, Power Pivot automatically built the relationship using `job_id`.

  <img width="1788" height="1264" alt="2_Project_Analysis_Screenshot5" src="https://github.com/user-attachments/assets/a2576c51-ebab-4ba5-bf10-d4b9160b849d" />

#### 🧩 Power Pivot Menu

- The Power Pivot menu allowed me to manage relationships and create measures easily for later use in charts.

  <img width="1918" height="742" alt="2_Project_Analysis_Screenshot6" src="https://github.com/user-attachments/assets/9cdf546e-f622-4b65-b9a8-2a3aff71f4fc" />

---

### 📊 Analysis & Insights

- 💻 **SQL** and **Python** appeared as the most in-demand skills — no surprise here, they’re essential for almost every data-related role.  
- ☁️ **AWS** and **Azure** are also gaining strong presence, reflecting the rise of cloud technologies.

  <img width="759" height="513" alt="2_Project_Analysis_Chart3" src="https://github.com/user-attachments/assets/310727f5-a754-451d-9cad-b26f2b148858" />

🧠 **So What:**  
Knowing which skills dominate the market helps guide what to study next and where to focus professional development.

---

## 4️⃣ What’s the pay of the top 10 skills?

### 📊 Skill Used: Advanced Charts (Pivot Chart)

#### 📈 PivotChart

- I built a combo PivotChart plotting **Median Salary** (bars) and **Skill Likelihood** (line) to compare pay vs. popularity:  
  - 🪙 **Primary Axis:** Median Salary (Clustered Column)  
  - 👍 **Secondary Axis:** Skill Likelihood (Line with Markers)  
- I customized the look by adjusting titles, removing unnecessary lines, and using diamond markers.

---

### 📊 Analysis & Insights

- 💰 Skills like **Python**, **Oracle**, and **SQL** stand out with the **highest median salaries**.  
- 📉 Tools like **PowerPoint** and **Word** appear at the bottom, showing lower demand for analytical roles.

  <img width="862" height="452" alt="2_Project_Analysis_Chart4" src="https://github.com/user-attachments/assets/c6df63b6-5e3f-4498-bac1-ba21b2a2853d" />

🧠 **So What:**  
If your goal is to earn more in data-related jobs, focus on **technical and high-value skills** like Python, SQL, and Cloud computing — they clearly pay off.

---

## 🚀 Conclusion

As a student and data enthusiast, this project helped me grow my analytical thinking and Excel skills to a new level.  
Through Power Query, DAX, and Pivot Charts, I turned raw job market data into clear, actionable insights.

I learned that **more skills often mean more opportunities and better pay** — and that’s exactly the mindset I’ll carry as I keep building my path in data analytics.  

📂 You can check out the full project file here:  
[📈 Project-2 Analysis.xlsx](https://github.com/murilobertacchi-code/Excel-Project-Data-Analytics/blob/main/Project%202-Analysis/Project-2%20Analysis.xlsx)

