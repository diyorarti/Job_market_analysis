# 📊 Job Market Analysis

## 📌 Project Overview

As a job seeker, I have always been interested in identifying patterns in the job market, particularly in understanding which skills top employers demand and how these skills relate to high-paying roles. This project aims to analyze job market data to uncover insights that can help job seekers make informed career decisions.


### 🎯 Questions

To analyze trends in the job market, this project focuses on the following questions:

1. Is there a correlation between the number of required skills and salary levels?
2. How do salaries differ across regions?
3. Which top 10 skills are associated with the highest pay?
 

## 🧠 Skills Set

- 📊 **Pivot Tables**
- 📈 **Pivot Charts**
- 🧮 **DAX (Data Analysis Expressions)**
- 🔄 **Power Query**
- 🧩 **Power Pivot**

## 📂 Dataset

This [dataset](/dataset/original_dataset.csv), sourced from Kaggle, consists of **50,000 job postings** spanning multiple industries.  
🔗 [AI-Powered Job Recommendations Dataset](https://www.kaggle.com/datasets/samayashar/ai-powered-job-recommendations)

## 1️⃣ 💰 Should having more skills lead to better pay?

### 🧹 Skill: Power Query (ETL)

#### 📥 Extract

- Power Query was used to extract the original dataset (`original_dataset.csv`) and create two queries:
    - 🗃️ One query containing all job-related information.
    - 🔧 A second query listing the required skills for each job ID.

#### 🔄 Transform

- Both queries were transformed by indexing columns, removing unnecessary fields, and cleaning the skills column.

    - 📊 job_recommendation_dataset  

    ![job_recommendation_dataset_transformation.png](/assets/job_recommendation_dataset_transformation.png)

    - 🛠️ job_skills  

    ![job_skills.png](/assets/job_skills.png)

#### 📤 Load

- The transformed queries were loaded into the Excel workbook.

    - 📊 job_recommendation_dataset  

    ![job_recommendation_data_load.png](/assets/job_recommendation_data_load.png)

    - 🛠️ job_skills  

    ![job_skills_load.png](/assets/job_skills_load.png)

### 🔍 Analysis

#### 💡 Insights

- Jobs requiring a higher number of skills tend to offer higher salaries.
- Specialized roles can achieve high pay with fewer but highly specific skills.
- Skill quantity and skill specialization both influence compensation.

![Salary_vs_skill_chart.png](/assets/Salary_vs_skill_chart.png)


