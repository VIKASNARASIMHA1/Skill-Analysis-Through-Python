# Overview

Welcome to my analysis of the data job market, focusing on data analyst roles in India. This project was created out of a desire to navigate and understand the job market for data analyst in India more effectively. It delves into the top-paying and in-demand skills to help find optimal job opportunities for data analysts in India.

The data sourced from (https://lukebarousse.com/python) which provides a foundation for my analysis, containing detailed information on job titles, salaries, locations, and essential skills. Through a series of Python scripts, I explore key questions such as the most demanded skills, salary trends, and the intersection of demand and salary in data analytics.

# The Questions

Below are the questions I want to answer in my project:

1. What are the skills most in demand for the top 3 most popular data roles in India?
2. How are in-demand skills trending for Data Analysts?
3. How well do jobs and skills pay for Data Analysts in India?
4. What are the optimal skills for data analysts to learn in India? (High Demand AND High Paying) 

# Tools I Used

For my deep dive into the data analyst job market, I harnessed the power of several key tools:

- **Python:** The backbone of my analysis, allowing me to analyze the data and find critical insights.I also used the following Python libraries:
    - **Pandas Library:** This was used to analyze the data. 
    - **Matplotlib Library:** I visualized the data.
    - **Seaborn Library:** Helped me create more advanced visuals. 
- **Jupyter Notebooks:** The tool I used to run my Python scripts which let me easily include my notes and analysis.
- **Visual Studio Code:** My go-to for executing my Python scripts.

**Git & GitHub:** Essential for version control and sharing my Python code and analysis, ensuring collaboration and project tracking.

# Data Preparation and Cleanup

This section outlines the steps taken to prepare the data for analysis, ensuring accuracy and usability.

## Import & Clean Up Data

I start by importing necessary libraries and loading the dataset, followed by initial data cleaning tasks to ensure data quality.

```python

import ast
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
dataset = pd.read_csv('data_jobs.csv')
df['job_posted_date'] = pd.to_datetime(df['job_posted_date'])
df['job_skills'] = df['job_skills'].apply(lambda x: ast.literal_eval(x) if pd.notna(x) else x)

```

## Filter Indian Jobs
To focus my analysis on the indian job market, I apply filters to the dataset, narrowing down to roles based in India.

```python
df_india = (dataset['job_country']=='India') & (dataset['job_title']=='Data Analyst')

```
# The Analysis

Each Jupyter notebook for this project aimed at investigating specific aspects of the data job market. Here’s how I approached each question:

## 1. What are the most demanded skills for the top 3 most popular data roles in India?

View my notebook with detailed steps here: [Skill_Demand](SkillDemand.ipynb).

## 2. How are in-demand skills trending for Data Analysts?

View my notebook with detailed steps here: [Skill_Trends](SkillTrends.ipynb).

## 3. How well do jobs and skills pay for Data Analysts in India?

View my notebook with detailed steps here: [Salary_Analysis](SalaryAnalysis.ipynb).

## 4. What are the most optimal skills to learn for Data in India?

View my notebook with detailed steps here: [Optimal_Skills](OptimalSkills.ipynb).

# Conclusion

This exploration into the data analyst job market has been incredibly informative, highlighting the critical skills and trends that shape this evolving field. The insights I got enhance my understanding and provide actionable guidance for anyone looking to advance their career in data analytics. As the market continues to change, ongoing analysis will be essential to stay ahead in data analytics. This project is a good foundation for future explorations and underscores the importance of continuous learning and adaptation in the data field.



