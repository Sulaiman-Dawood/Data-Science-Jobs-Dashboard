# 📊 Data Science Jobs Dashboard

This dashboard provides a detailed analysis of data science job salaries, offering insights into compensation trends across different experience levels.

![Salary Analysis by Experience Level](Images/Screenshot%202025-08-02%20162455.png)

A comprehensive Power BI dashboard analyzing data science job market trends, salaries, and employment patterns.

## 📝 Overview

This Power BI project provides insights into the data science job market, featuring interactive visualizations and analytics on job titles, salaries, experience levels, company sizes, and geographic distributions. The dashboard helps job seekers, recruiters, and industry professionals understand current market trends in data science roles.

## ✨ Features

- **Salary Analysis**: Compare salaries across different experience levels, job titles, and geographic locations
- **Job Market Trends**: Track employment patterns over time
- **Geographic Insights**: Visualize job distribution and salary variations by country
- **Experience Level Breakdown**: Analyze opportunities across different career stages
- **Employment Type Analysis**: Compare full-time, part-time, contract, and freelance opportunities

## 💾 Data Source

The data for this dashboard was sourced from Kaggle: [Latest Data Science Job Salaries 2024](https://www.kaggle.com/datasets/saurabhbadole/latest-data-science-job-salaries-2024). The original dataset was cleaned and processed to ensure data quality and consistency before being imported into Power BI. The cleaned dataset includes:

- Job postings from various years
- Salary information in multiple currencies
- Geographic distribution across different countries
- Various experience levels and company sizes
- Different employment and work arrangements

## 🛠️ Tools and Technologies Used

This project was developed using a combination of Python for data preprocessing, Excel for data handling, and Power BI for creating the interactive dashboard.

### 🐍 Data Cleaning with Python

The `pycountry` library in Python was used to standardize country names by converting two-letter country codes (EG, US, UK) into their full names (Egypt, United States, United Kingdom). This ensured consistency for geographic analysis.

```python
import pandas as pd
import pycountry

# Function to convert country codes to full names
def code_to_country(code):
    try:
        return pycountry.countries.get(alpha_2=code.upper()).name
    except:
        return "Unknown"
```

### ⚡ Data Transformation with Power Query

Power Query was used within Power BI to transform and clean the data. For example, the `remote_ratio` column was converted into a more descriptive `work_type` column, as shown below:

**Before Transformation:**

| remote_ratio |
|--------------|
| 100          |
| 50           |
| 0            |

**After Transformation:**

| work_type |
|-----------|
| Remote    |
| Hybrid    |
| On-site   |

## 💡 Key Insights

This dashboard can help answer questions such as:

- What are the average salaries for different data science roles?
- How do salaries vary by experience level and geographic location?
- What's the distribution of remote vs. on-site work opportunities?
- Which companies and locations offer the highest compensation?
- How has the job market evolved over time?
- What are the most in-demand data science job titles?

## 📧 Contact

For questions or suggestions regarding this dashboard, please refer to the project documentation or create an issue in the repository.

---

*Last updated: August 2, 2025*
