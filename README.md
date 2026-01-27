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

## 1️ 💰 should I have more skills to get better pay?

### 🧹 Skill: Power Query (ETL)

#### 📥 Extract

- I used Power Query to extract the original data (original_dataset.csv) and create two questies:
    - 🗃️ First one with all the data jobs information.
    - 🔧 The second listing the skills for each job ID.

#### 🔄 Transform

- I transformed each query by indexing, removing unnecessary columns, clearning skills column. 

    - 📊 job_recommendation_dataset

    ![job_recommendation_dataset_transformation.png](/assets/job_recommendation_dataset_transformation.png)

    - 🛠️ job_skills

    ![job_skills.png](/assets/job_skills.png)

#### 📤 Load

- I loaded both transformed queries into the workbook.

    - 📊 job_recommendation_dataset

    ![job_recommendation_data_load.png](/assets/job_recommendation_data_load.png)

    - 🛠️ job_skills

    ![job_skills_load.png](/assets/job_skills_load.png)