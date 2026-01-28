# 📊 Job Market Analysis

## 📌 Project Overview

As a job seeker, I have always been interested in identifying patterns in the job market, particularly in understanding which skills top employers demand and how these skills relate to high-paying roles. This project aims to analyze job market data to uncover insights that can help job seekers make informed career decisions.


### 🎯 Questions

To analyze trends in the job market, this project focuses on the following questions:

1. Is there a correlation between the number of required skills and salary levels?
2. How do salaries differ across regions?
3. What are the top skils ? 
4. Which top 10 skills are associated with the highest pay?
 

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

## 2️⃣ 🌍 How do salaries differ across regions?

### 🧮 Skills: PivotTables & DAX

#### 📈Pivot Table

- A Pivot Table was created using the data model built with **Power Pivot**.
- The `Job_Title` field was placed in the **Rows** area, while `Salary` was added to the **Values** area.
- Median salary metrics were calculated to compare compensation across different regions.
    ```
    =CALCULATE(job_recommendation_dataset[Salary], 
               job_recommendation_dataset[Location]="London")
    ```

#### 🧮 DAX

- DAX was used to calculate the overall median salary across all regions:
    ```
    Median Salary := MEDIAN(job_recommendation_dataset[Salary])
    ```

### 📊 Analysis

#### 💡 Insights
- London-based roles consistently offer higher median salaries compared to non-London regions. Across all listed job roles, the overall median salary in London is $127,000, while non-London roles average $95,000, highlighting a significant regional pay gap.
- The salary premium in London applies across diverse job categories, including administrative, technical, creative, and engineering roles. This suggests that location has a strong influence on compensation, often outweighing job type in determining salary levels.

    ![Salary_analysis.png](/assets/Salary_analysis.png)

## 3️⃣ What are the top skills ?

### 🧩 Skill: Power Pivot

#### 💪 Power Pivot

- I created a Data Model by integrating the `job_recommendation_dataset` and `job_skills` tables into one model.
- Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.

#### 🗄️ Data Model

- I created a relationship between my two tables using the `Job_id` column.

    ![Data_model_ERD.png](/assets/Data_model_ERD.png)

#### ⚙️ Power Pivot Menu

- The Power Pivot menu was used to refine the data model, manage table relationships, and efficiently create DAX measures.

    ![Power_Pivot_Menu.png](/assets/Power_Pivot_Menu.png)

### 📊Analysis

#### 📌 Insights

- Technical skills dominate demand across regions, with Python and SQL ranking as the most frequently requested skills, highlighting the strong demand for data and software-related expertise across industries.
- Operational and business skills remain highly relevant, as skills such as Production Planning, Quality Control, Supply Chain, Sales, and Customer Service also show high demand, indicating that employers value a balance between technical and business-oriented capabilities.

    ![Skill_and_Job_analysis.png](/assets/Skill_and_Job_analysis.png)

## 4️⃣ Which top 10 skills are associated with the highest pay?

### 📈 Skill: Advanced Charts (Pivot Chart)

#### 📊 Pivot Chart

- I created a combo PivotChart to plot medial salary and skill count from my PivotTable.
    -  **Primary Axis:** Median Salary (as a Clustered Column)
    -  **Secondary Axis:** Skill Count (as a Line with Markers)

### 📊 Analysis

#### 💡Insights

- Technical skills lead the top-paying roles, with SQL and Python showing the highest median salaries among the top 10 skills, indicating strong demand and high compensation for data and programming expertise.
- High salary does not always correlate with high demand, as some skills with relatively lower job counts (e.g., Quality Control or EdTech) still offer competitive median salaries, suggesting that specialization can drive pay even when demand is moderate.

    ![Top_paying_10skills.png](/assets/Top_paying_10skills.png)

## ✅ Conclusion

## ✅ Conclusion

This analysis demonstrates that both the **number of skills** and **skill specialization** play a crucial role in determining salary levels in the job market. Roles requiring broader skill sets and strong technical expertise, particularly in areas such as **Python and SQL**, tend to offer higher compensation. Additionally, **location significantly impacts salary**, with London-based roles consistently earning more than non-London positions across job categories. Overall, the findings highlight the importance of strategic skill development and geographic considerations for job seekers aiming to maximize their earning potential.
