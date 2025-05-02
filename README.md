# Excel Analysis Project

## Introduction  

Completing my self learning of Excel and exploring job opportunities, I delve into the data science market to identify optimal job roles and essential skills. My goal is to understand the key skills that top employers are seeking, as well as strategies to secure higher paying positions in this field.  

### Questions to Analyze  

To understand the data science job market, I asked the following:

1.**Do more skills get you better pay?**  
2.**What's the salary for data jobs in different regions?**  
3.**What are the top skills for data professionals?**  
4. **What's the pay for the top skills?**  

### Excel Skills Used  

The following Excel skills were utilized for analysis:  

-**Pivot Tables**  
-**Pivot Charts**  
-**DAX (Data Analysis Expressions)** 
-**Power Query**  
-**Power Pivot**  

### Data Jobs Dataset  

The dataset used for this project contains real world data science job information from 2023. The dataset is available via my github  

It includes detailed information on:  

-**Job titles**  
-**Salaries**  
-**Locations**  
-**Skills**  

## 1️⃣ Do more skills get better pay?  

### Skill: Power Query (ETL)  

### Extract  

- I first used Power Query to extract the original data (’data salary all.xslx’) and create two queries:
  - First with all the data job information.
  - Second, list the skills for each job ID.

### Transform  

- Then, i transformed each query by changing column types,eliminating unnecessary columns, cleaning up texts to eliminate specific words, and trimming excess whitespace.

  - Data Job Salary

    ![Screenshot 2025-04-28 061847](https://github.com/user-attachments/assets/7d927844-4248-4635-9c62-9f57fa65f501)
  

  - Data Job Skills 

   ![Screenshot 2025-04-28 062152](https://github.com/user-attachments/assets/885d56ef-6bb1-4b71-ad5f-bba8293699f5)
 
### Load  
- Finally, I loaded both transformed queries into the workbook, setting the foundation for my subsequent analysis.  
  
  - Data Job Salary

   ![Screenshot 2025-04-28 062223](https://github.com/user-attachments/assets/c3e39e1e-be43-4336-a7d4-76134fb5f5d1)  

   
   - Data Job Skills

   ![Screenshot 2025-04-28 062239](https://github.com/user-attachments/assets/2ed5cf30-87c8-4d9b-96b9-3eaa7aff340d)


### Analysis  

### Insights  

- There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Data Scientist and Senior Data Engineer.
- Roles that requires fewer skills Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.

  ![Screenshot 2025-04-28 062429](https://github.com/user-attachments/assets/62f368ef-07d0-453d-9e53-d5ea419bf9b7)


### Finding  

-This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher paying roles.  

## 2️⃣ What's the salary for data jobs in  different regions?  

### Skills: Pivot Table and DAX  

### Pivot Table  

- I created a Pivot Table using the Data Model I created with Power Pivot.
- I moved the ‘job_title_short’ to the row area and ‘salary_year_avg’ into the values area.
- Then I added a new measure to calculate the median salary for United States jobs.
   
```
  =CALCULATE(MEDIAN(data_job_all[salary_year_avg]), data_jobs_all[job_country] = “United States”)
```

#### DAX 





